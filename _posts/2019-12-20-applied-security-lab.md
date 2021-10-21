---
title: 'Applied Security Lab'
date: 2019-12-20
permalink: /posts/2019/12/Applied-Security-Lab/
tags:
  - risk analysis
  - certificates
  - automation
  - pentesting
---

In this course, our task was to implement a typical IT system based on a set of functional and security requirements in a team of four people. For this purpose, we needed to design a certificate authority for a fictional company while analyzing the security and take appropriate measures. Furthermore, we needed to introduce two backdoors in the system. In the middle of the semester, we switched to analyze another team's system and assess their security. This, of course, included finding their backdoors as well as any other vulnerabilities.

## System Overview

![](/images/applied_security_lab_system_overview.png)

This figure gives an overview of our system. The core of this infrastructure consists of a triangle of three servers: web server, database server, and core CA. The web server manages authentication as well as authorization of the users. The database stores user information, which can be updated over the web server, as well as public certificates and encrypted private keys of users. The core CA is responsible for issuing and revoking certificates as well as generating the Certificate Revocation List (CRL). It provides an API to the web server and updates sensitive data in the database (passwords, certificates and encrypted private keys). This triangle is mirrored completely redundant with another three identically configured servers. Our load balancer distributes traffic between those two infrastructures, while monitoring their state and switches to the healthy one in case of failures.

In order to be able to configure such a complex and redundant environment, we automated the configuration of all machines with [Ansible](https://www.ansible.com/). Moreover, as our local setup used virtual machines, we automated their setup as well with [Vagrant](https://www.vagrantup.com/).

Many more details and a security analysis are in the full [system description](https://github.com/Liblor/applied_sec_lab/tree/master/description/Applied_Security_Lab_group_1_System_Description_incl_backdoors.pdf).

## Further Resources

- The source code of this project is available [here](https://github.com/Liblor/applied_sec_lab).
- The full system description is can be downloaded [here](https://github.com/Liblor/applied_sec_lab/tree/master/description/Applied_Security_Lab_group_1_System_Description_incl_backdoors.pdf).
