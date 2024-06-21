---
title: 'A Formal Treatment of End-to-End Encrypted Cloud Storage'
date: 2024-08-18
permalink: /posts/2024/08/e2ee-cloud-storage-security-notions
tags:
  - security
  - cloud storage
  - game-based proofs
---

We designed an E2EE cloud storage protocol and prove it secure in novel game-based confidentiality and integrity notions that capture real-world complexities and malicious servers.

## Overview

This is joint work with [Matilda Backendal (ETH Zurich)](https://mbackendal.github.io/), [Hannah Davis (Seagate)](https://cseweb.ucsd.edu/~h3davis/), [Felix Günther (IBM Research &mdash; Zurich)](https://www.felixguenther.info/), and [Kenny Paterson (ETH Zurich)](https://appliedcrypto.ethz.ch/people/person-detail.MjU0MDM1.TGlzdC8zMzE4LC0yODgzMDgzMDc=.html).
This post only contains some of the highlights, please read the full version of our paper on [eprint](https://eprint.iacr.org/2024/989).

Users increasingly store their data in the cloud for easy access, sharing, and redundancy. E2EE should protect the data even against server compromise. However, recent research from myself and others has discovered attacks against widely deployed systems. For example, we showed MEGA (300 million users) can decrypt user files ([here](https://mega-awry.io/) and [their patches for our attacks were broken](https://mega-caveat.github.io/)). Others in Kenny's Applied Crypto Group showed that Nextcloud could [exploit the sharing feature](https://eprint.iacr.org/2024/546) to learn user files.

In other words, we realized that the security of E2EE cloud storage is behind the one of other E2EE applications like secure messaging. There is no rigorous foundation, no security notions, and no provably secure protocols.
Instead, deployed E2EE cloud storage protocols are custom designs that attempt to solve many complex cryptographic challenges including password-based key management and file sharing, Despite this complexity, there's no formal guarantees to back up their security claims.

In this paper, we initiate the formal study of E2EE cloud storage and make four main contributions toward understanding the security of E2EE cloud storage and bringing it up to par with other E2EE applications:
1. We give a formal syntax capturing the core functionality of E2EE cloud storage while honoring the real-world complexity of such systems and supporting interactive protocols and out-of-band channels.
2. We define game-based security notions for confidentiality and integrity of E2EE cloud storage against a fully malicious server, treating both selective and fully adaptive client compromises.
3. We put our model to the test and use it to formally capture some of the recent attacks on MEGA, showing our framework is rich enough to model deployed systems and capture practical attacks.
4. We present an E2EE cloud storage system that supports all core functionality, is efficient and is provably secure with respect to our selective security notions.

We discuss many challenges on the path towards bringing the security of cloud storage up to par with other end-to-end primitives, which are interesting for future research.
To only mention a few, one is analysing whether our protocol achieves adaptive security, or if this can be achieved efficiently by another protocol that is based on standard cryptographic assumptions.
Another interesting question is to achieve advanced security properties that other E2EE primitives offer, such as forward secrecy and post-compromise security, in the cloud storage setting. 

We hope that users will eventually enjoy the benefits of a single, well-analyzed scheme with provable security guarantees, akin to E2EE communication today. Standardization of such a scheme would resolve the long-standing issues that untrusted cloud providers need to be trusted with the design of a secure system and serving benign client code. A standardized scheme could have independent client implementations (i.e., not under the control of the potentially malicious provider) and even lead to interoperability between cloud storage providers. Our work is a first step towards bringing modern cryptographic guarantees to cloud storage.

You can find interesting open problems, our provably secure E2EE cloud storage protocol, game-based security notions that are surprisingly compact for being even more complex than key exchange notions, and pages of beautiful proofs in our paper: [https://eprint.iacr.org/2024/989](https://eprint.iacr.org/2024/989).

## Abstract

> Users increasingly store their data in the cloud, thereby benefiting from easy access, sharing, and redundancy. To additionally guarantee security of the outsourced data even against a server compromise, some service providers have started to offer end-to-end encrypted (E2EE) cloud storage. With this cryptographic protection, only legitimate owners can read or modify the data. However, recent attacks on the largest E2EE providers have highlighted the lack of solid foundations for this emerging type of service.
>
> In this paper, we address this shortcoming by initiating the formal study of E2EE cloud storage. We give a formal syntax to capture the core functionality of a cloud storage system, capturing the real-world complexity of such a system’s constituent interactive protocols. We then define game-based security notions for confidentiality and integrity of a cloud storage system against a fully malicious server. We treat both selective and fully adaptive client compromises. Our notions are informed by recent attacks on E2EE cloud storage providers. In particular we show that our syntax is rich enough to capture the core functionality of MEGA and that recent attacks on it arise as violations of our security notions. Finally, we present an E2EE cloud storage system that provides all core functionalities and that is both efficient and provably secure with respect to our selective security notions. Along the way, we discuss challenges on the path towards bringing the security of cloud storage up to par with other end-to-end primitives, such as secure messaging and TLS.

## Acknowledgements

This paper took us more than 2.5 years to finalize.
It was probably the most challenging project I worked on so far.
The sheer complexity of the models and the infinite design space made it very hard to carve out a well-defined, solvable problem and arrive at satisfying definitions. 
This would never have been possible without the amazing support that I received.

First of all, I would like to thank my co-authors for all their amazing work, their input and feedback on dozens of iterations of the security game. 
My thanks goes to: 
Matilda, for driving the project together with me and doing amazing work on the diligent proof of our protocol;
Felix, for helping us with his experience from Key Exchange protocols to cope with the complexity and teaching me how to be concise;
Kenny, for guiding us with his decades of experience and unbeatable intuition.
Hannah, for writing an amazing section to justify our choice of game-based proofs over UC.

Moreover, I would like to thank Mihir Bellare for his guidance in the early stages of this project and his feedback on my first drafts of the game.
I would also like to thank my advisor, Nadia Heninger, for never objecting that I spent considerable time on this project that started before my Ph.D. with her at UCSD, and for her help to write and apply for a grant to fund my work.

Finally, my deepest gratitude goes to Alisha, who supported me in every way possible, from giving feedback on my writing to ensuring I stay sane and healthy around deadlines.

My research was supported by an Amazon Research Award Fall 2023. Any opinions, findings, and conclusions or recommendations expressed in this material are those of the authors and do not reflect the views of Amazon.


