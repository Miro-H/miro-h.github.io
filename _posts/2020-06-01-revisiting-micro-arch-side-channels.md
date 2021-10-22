---
title: 'Revisiting Microarchitectural Side-Channels'
date: 2020-06-01
permalink: /posts/2020/06/Revisiting-Side-Channels/
tags:
  - thesis
  - side-channel
  - timing
  - caches
  - argon2
  - aes
  - openssl
---

This project revisits cache side-channels on contemporary hardware and contributes CacheSC, a tool for L1 and L2 Prime+Probe attacks. Furthermore, we apply it to AES lookup tables, AES key scheduling, and acquire first insights on Argon2.

## Abstract

> Microarchitectural side-channels exploit observations on the internal state of (cryptographic) algorithms obtained by measuring side-effects such as contention on a shared resource. In this project, we focus on cache side-channels, which were among the first practically exploited information leakages. We provide an overview of the extensive research on cache timing attacks and a more in-depth analysis of the wide-spread Prime+Probe technique. We find that due to the empirical approach on cache side-channels, the results are often tailored to specific software and hardware versions. However, we consider it beneficial to revisit cache attacks and adapt them to new environments as the side-channels’ underlying root causes are likely to persist over time and architectures because of their fundamental relation to performance. Therefore, we revisit a classical chosen-plaintext attack, targeting OpenSSL’s AES-CBC implementation, and apply it on contemporary hardware. We explain the challenges of implementing this attack in the presence of out-of-order execution, dynamic frequency scaling, hardware prefetching, line-fill buffers and other optimisations. Furthermore, we especially highlight the importance of an appropriate data structure to cope with the previous challenges while minimising cache side-effects of the measurement itself. Moreover, we contribute CacheSC, a library that implements different variants of Prime+Probe targeting not only on virtually indexed caches but also including two methods to attack physically indexed caches. The first attack requires superuser privileges and translates virtual to physical addresses in user space by parsing the pagemap file. The second approach uses collision detection to build the cache attack data structure without requiring special privileges. Finally, we use CacheSC to conduct an initial review of the AES key scheduling algorithm as well as Argon2 and provide starting points for novel applications of cache side-channels.

Read the full report [here](/files/revisiting-microarchitectural-side-channels.pdf).

## CacheSC

CacheSC is a library for L1 and L2 cache side-channel attacks. It implements Prime+Probe attacks on contemporary hardware. It features:

- Simple interface to abstract low-level complications of performing cache attacks, including precise time measurements in the presence of out-of-order execution.
- Privileged and unprivileged methods to attack physically indexed caches (such as L2 on many devices).
- Handy plotting scripts to visualise side-channel oberservations.

The rationale behind the design of this library, in-depth discussion of the demo applications and cache side-channels in general can be found in our [report](/files/revisiting-microarchitectural-side-channels.pdf).

We released CacheSC on [GitHub](https://github.com/Miro-H/CacheSC) under the GPL-3.0 license.
