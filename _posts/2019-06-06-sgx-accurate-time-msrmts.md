---
title: 'On Performing Accurate Time Measurements of SGX Enclave Instructions'
date: 2019-06-06
permalink: /posts/2019/06/bachelor-thesis/
tags:
  - thesis
  - SGX enclaves
  - side-channel
  - timing
---


For my Bachelor's thesis I investigated instruction time measurements with the [System Security Group](https://syssec.ethz.ch/) at ETH Zurich. Our findings led to various improvements over existing measurement tools and the discovery of a new side-channel attack, the [Frontal Attack](/publication/2021/08/frontal-attack).

## Short Summary
SGX enclaves allow to securely execute a program on hardware owned by an untrusted entity. Since precise timestamps are not available inside enclaves and not even the OS can manipulate their computations, it is difficult to measure the timings of instructions executing inside enclaves.

This thesis serves as a reference on how to obtain accurate timings in general and especially in connection with SGX enclaves. We built on top of [SGX-Step](https://github.com/jovanbulck/sgx-step), a practical attack framework for precise enclave execution control. [Nemesis](https://github.com/jovanbulck/nemesis) goes in the same direction as our work and also modifies SGX-Step to do time measurements. However, our project further improves the observation accuracy and runs more in-depth test cases.
We describe the following improvements over SGX-Step (with references to the corresponding sections in the [thesis](/files/)):
1. We noted that different enclaves have varying enclave entry and exit times, which makes it hard to compare instruction timings of different enclaves. We added the measurement of multiple test cases inside the same enclave as well as automated plotting. (4.1)
2. Better instruction serialization barriers before and after the measurement to reduce noise. (3.2.1, 3.3.3)
3. Reduced cache pollution due to (almost) constant time measurement code and delayed instruction filtering and logging. (4.3, 4.4)
4. Multiple consistency checks to detect imprecise APIC timers, misconfigured tests and instructions that can execute in two parts. (4.5, 4.6)
5. Support for more complex test cases. (3.3.1, 4.8, 4.9, 5.1)

Furthermore, we discuss the following enhancements and new features:
1. New plot types to gain more insights about measurements. (3.4.2, 3.4.3, 3.4.4, 5.1)
2. Alternative measurement options that all share the same test case specifications:
    1. Measure timings outside the enclave to see differences to instructions inside the enclave. (3.3.2)
    2. Counter method to cross validate results of SGX-Step (although they have lower precision). (3.3.4)
3. Filtering noise and especialy outliers at page boundaries to get a meaningful variance and compact plots. (3.4, 4.2, 4.10)

By improving the instruction granular time measurements of SGX enclaves, we show that even more detailed information about the enclave’s execution state can be leaked than previously assumed. We describe the discovery of the phenomenon that led to the [Frontal Attack paper](/publication/2021/08/frontal-attack).

The complete thesis is available [here](/files/2019_Miro_Haller_SGX_Accurate_Time_Measurements.pdf).

## Frontal Attack

My advisors continued this project and made it into a USENIX Security paper called [Frontal Attack: Leaking Control-Flow in SGX via the CPU Frontend](/publication/2021/08/frontal-attack).

The source code of a proof of concept implementation of the Frontal attack is published [here](https://github.com/dn0sar/frontal_poc) and includes part of the code of this thesis.

Here is Ivan Puddu's presentation of the paper:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/ti58SJ1ie3A?si=2DAWOEStDNSEjlBu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Acknowledgement

I would like to thank [Ivan Puddu](https://syssec.ethz.ch/people/puddui.html) and [Moritz Schneider](https://syssec.ethz.ch/people/scmoritz.html) for their extraordinary support and countless discussions and inputs. Moreover, I thank [Prof. Dr. Srdjan Capkun](https://syssec.ethz.ch/people/capkun.html) for making this project possible.
