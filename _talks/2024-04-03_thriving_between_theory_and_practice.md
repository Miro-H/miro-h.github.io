---
title: "Thriving in between theory and practice: How applied cryptography bridges the gap"
collection: talks
type: "Talk"
permalink: /talks/2024/04/thriving-between-theory-and-practice
venues: "Crypto Reading Club at NIST;;Zurich Information Security & Privacy Center at ETH Zurich"
date: 2024-04-03
location: "NIST"
---

Matilda Backendal and I were invited to give this talk at the NIST CRClub on where the gap between theory and practice occurs.

## Abstract
Our abstract from the [talk announcement](https://csrc.nist.gov/presentations/2024/crclub-2024-04-03):

> The focus of applied cryptography is the security of cryptographic systems used in practice. This includes analyzing cryptographic protocols and primitives used in the wild, and designing and deploying secure systems. Unfortunately, this is a challenging task. Cryptography is highly brittle and small design or implementation mistakes can have devastating effects on a system level. Additionally, the many interacting parts of a large system makes analyzing its security complex. Even defining an appropriate threat model can be difficult, and the most secure cryptographic designs sometimes break when faced with real-world use that differs from the usage intended by the designers.
>
> In this talk, we discuss some of these challenges. In particular, we draw on our experiences from recent work on analyzing and constructing cryptography for practice and try to condense the lessons learnt, including: Where (and why) does the gap between theory and practice arise? How can applied cryptography help bridge the gap? And why should you, too, do applied cryptography?

The presentation slides are available [here](/files/2024-04-03_thriving_between_theory_and_practice.pdf).

## Readings

This talk was based on insights from our work in this space:
- [E2EE Cloud Storage](https://static.cryptanalysis.fun/papers/e2ee-cloud-storage.pdf) (a IEEE SP magazine article)
- [MEGA: Malleable Encryption Goes Awry](https://ia.cr/2022/959)
- [When Messages are Keys: Is HMAC a dual-PRF?](https://eprint.iacr.org/2023/861)

## Further Resources

We organize the [Cryptographic Applications Workshop](https://caw.cryptanalysis.fun/) at Eurocrypt 2024. This workshop is in the same spirit as this talk and focuses on the construction and analysis of cryptography built for practice.
It aims to provide a forum for cryptographers in academia and industry to exchange ideas and insights, bridging the gap between research and real-world applications.
