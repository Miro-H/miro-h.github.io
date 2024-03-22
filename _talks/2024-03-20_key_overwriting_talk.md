---
title: "Key Overwriting Attacks"
collection: talks
type: "Talk"
permalink: /talks/2024/03/key-overwriting-attacks-talk
venues: "MIT CSAIL"
date: 2024-03-20
location: "Boston, MA"
---

I was fortunate to be hosted by Henry Corrigan-Gibbs and held this talk at [MIT CSAIL](https://calendar.csail.mit.edu/events/279180).

## Abstract
Here is the talk abstract:
> In this talk, I will formally define key overwriting attacks and discuss some recent applications.
> 
> After lying dormant for 20 years, a recent series of papers exploited key overwriting attacks to break the security of deployed end-to-end encrypted schemes. More and more, systems aim to protect users even against a malicious or compromised server. Together with complex key hierarchies, this lead to attacks where the adversary can overwrite (part of) the key material of users. By observing the client's operation on such (partially) corrupted key material, some attacks were able to go as far as recovering the key material.
>
> To conclude, we discuss the root causes for key overwriting attacks and my most recent work to fundamentally avoid these and other attacks in end-to-end encrypted cloud storage.
>
> This talk is based on [MEGA: Malleable Encryption Goes Awry](https://eprint.iacr.org/2022/959) and [Caveat Implementor! Key Recovery Attacks on MEGA](https://eprint.iacr.org/2023/329) but I will also touch on other key recovery attack and work-in-progress.

The presentation slides are available [here](/files/2024-03-20_Key_Overwriting_Attacks.pdf).
