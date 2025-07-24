---
title: Key Overwriting Attacks
date: 2023-11-30
short_desc: "This talk reflects on recent attacks where a malicious server overwrites encrypted key material outsourced by clients to learn secret information."
venues:
  - name: CSE 207b
    my_presentation: 'yes'
    youtube: https://youtu.be/x21qwMAUscE?feature=shared
    youtube_embed: https://www.youtube.com/embed/x21qwMAUscE?si=qr__mlM-LjLPqy-7
    slides: /files/2023-11-30_CSE207b_Key_Overwriting_Attacks.pdf
  - name: MIT CSAIL
    link: https://www.csail.mit.edu/event/key-overwriting-attacks
    slides: /files/2024-03-20_Key_Overwriting_Attacks.pdf
    my_presentation: 'yes'
collection: talks
type: "Talk"
permalink: /talks/2023/11/cse207b-key-overwriting-attacks
date: 2023-11-30
---

There are two variants of this talk.

### CSE 207b

The first is a guest lecture in the applied cryptography course [CSE 207b](https://cseweb.ucsd.edu/classes/fa23/cse207B-a/) at UCSD, in which I formalize key overwriting attacks.

Here is the recording:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/x21qwMAUscE?si=kjdg-dHsokwy6NXO" title="Key Overwriting Attacks YouTube Player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### MIT CSAIL

For the second talk, I was fortunate to be hosted by Henry Corrigan-Gibbs at MIT CSAIL. This talk focuses more on the research side. The slides are linked below.

Abstract:
> In this talk, I will formally define key overwriting attacks and discuss some recent applications.
>
> After lying dormant for 20 years, a recent series of papers exploited key overwriting attacks to break the security of deployed end-to-end encrypted schemes. More and more, systems aim to protect users even against a malicious or compromised server. Together with complex key hierarchies, this lead to attacks where the adversary can overwrite (part of) the key material of users. By observing the client's operation on such (partially) corrupted key material, some attacks were able to go as far as recovering the key material.
>
> This talk is based on "MEGA: Malleable Encryption Goes Awry" and "Caveat Implementor! Key Recovery Attacks on MEGA" but I will also touch on other key recovery attacks.
