---
title: "A Formal Treatment of End-to-End Encrypted Cloud Storage"
collection: talks
type: "Talk"
permalink: /talks/2024/08/formalizing-e2ee-cloud-storage
venues: "Crypto 2024;;Berkeley Security Seminar;;Trails of Bits;;UMD Crypto Reading Group"
date: 2024-08-21
location: "Santa Barbara"
---

We present a formal syntax and security notions for end-to-end encrypted cloud storage and design the first, provably secure protocol for this widespread application.

## Paper

This talk is based on our paper at Crypto'24, which I discuss in [this blog post](/posts/2024/08/e2ee-cloud-storage-security-notions).

## Talk Abstract

Users increasingly store their data in the cloud, thereby benefiting from easy access, sharing, and redundancy.
To additionally guarantee security of the outsourced data even against a server compromise, some service providers including iCloud have started to offer end-to-end encrypted (E2EE) cloud storage.
With this cryptographic protection, only legitimate owners can read or modify the data.
Academic work in the cloud storage space has focused on achieving advanced properties such as hiding metadata, searching encrypted data, puncturing keys to achieve forward security, or the temporary self-revocation of access.
However, recent attacks on Mega and other large E2EE providers have highlighted the lack of solid foundations for even the basic confidentiality and integrity guarantees of this emerging type of service.

In this talk, Matilda Backendal and I present joint work with Hannah Davis, Felix Günther, and Kenny Paterson that initiates the formal study of E2EE cloud storage.
We will present our formal syntax to express the core functionality of a cloud storage system, capturing the real-world complexity of such a system's constituent interactive protocols. 
Then, we define our game-based security notions for confidentiality and integrity of a cloud storage system against a fully malicious server with both selective and fully adaptive client compromises. 
Finally, we present an E2EE cloud storage system that provides all core functionalities and that is both efficient and provably secure with respect to our selective security notions. 
Along the way, we will point out challenges on the path towards bringing the security of cloud storage up to par with other end-to-end primitives, such as secure messaging and TLS, and avenues for future work.

## Talk Recording

<iframe width="560" height="315" src="https://www.youtube.com/embed/epiON1Kjr8o?si=VIaXXZBng7gYdXFq&amp;start=1106" title="A Formal Treatment of End-to-End Encrypted Cloud Storage" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Talk Slides

Here are different versions of our slides:
- [Crypto 2024](/files/2024_09_formalizing-e2ee-cloud-storage-crypto.pdf) (co-presented with Matilda Backendal)
- [Berkeley Security Seminar](/files/2024_09_formalizing-e2ee-cloud-storage-Berkeley.pdf)
