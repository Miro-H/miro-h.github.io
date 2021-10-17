---
title: "Frontal Attack: Leaking Control-​Flow in SGX via the CPU Frontend"
collection: publications
permalink: /publication/2021-08_frontal-attack
excerpt: 'This paper is about the number 1. The number 2 is left for future work.'
date: 2021-08
venue: 'USENIX Security'
paperurl: 'https://www.usenix.org/system/files/sec21-puddu.pdf'
citation: 'Ivan Puddu, Moritz Schneider, Miro Haller, Srdjan Čapkun. (2021). &quot;Frontal Attack: Leaking Control-​Flow in SGX via the CPU Frontend&quot; <i>USENIX Security 2021</i>.'
---

Abstract:
> We introduce a new timing side-channel attack on Intel CPU processors. Our Frontal attack exploits timing differences that arise from how the CPU frontend fetches and processes instructions while being interrupted. In particular, we observe that in modern Intel CPUs, some instructions’ execution times will depend on which operations precede and succeed them, and on their virtual addresses. Unlike previous attacks that could only profile branches if they contained different code or had known branch targets, the Frontal attack allows the adversary to distinguish between instruction-wise identical branches. As the attack requires OS capabilities to set the interrupts, we use it to exploit SGX enclaves. Our attack further demonstrates that secret-dependent branches should not be used even alongside defenses to current controlled- channel attacks. We show that the adversary can use the Frontal attack to extract a secret from an SGX enclave if that secret was used as a branching condition for two instruction- wise identical branches. We successfully tested the attack on all the available Intel CPUs with SGX (until 10th gen) and used it to leak information from two commonly used cryptographic libraries.

[Full paper](https://www.usenix.org/system/files/sec21-puddu.pdf)
