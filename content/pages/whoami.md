+++
title = "About"
path = "whoami"

[extra]
no_page_info = true
+++

Welcome to my personal blog! The main topics here are cybersecurity, Free Open Source Software and self-hosting.

## The site

This website is built with [Zola](https://www.getzola.org) (a static website engine) and self-hosted on my homelab, a ThinkCentre M720q running [NixOS](https://nixos.org). The website source code lives inside a [Github repo](github.com/Zerodya/zerodya.net).

The stack works like this: Website repo on GitHub \> Nix builds the static site \> Nginx \> Cloudflare Tunnel \> This webpage.

## About me

Hi, my name is Nicola, but I like to go by "Zerodya" online.  
I am a hacker, not for skills (I still have a long way to go), but because I try to understand how things work, and I tinker with something until I find a way to improve it based on what I want it to do, whether it is an operating system, a program or an object that I use everyday.

<p align="center">
    <img src="/content/images/2022/06/portrait-ccit.jpg" alt="cyberchallenge t-shirt" width="400"/>
</p>

> Picture of me wearing the [CyberChallenge.IT](https://cyberchallenge.it) t-shirt.

### Studies

- **Now** - I am studing for the Cisco [CCNA](https://www.cisco.com/site/us/en/learn/training-certifications/certifications/enterprise/ccna/index.html) and INE [eJPT] certifications.

- **2026** - I graduated at the Parthenope University of Naples as a **Cybersecurity Engineer** in 2026.

- **2022** - I was admitted to [CyberChallenge.IT](https://cyberchallenge.it/), an exclusive italian training program to teach young students about cybersecurity in a gamified way, with both Jeopardy and Attack/Defense CTFs.  
It was a great opportunity to get hands-on experience and learn about a lot of different attack vectors and techniques that I didn't know about.

<p align="center">
    <img src="/content/images/2022/06/ccit-cert-1.webp" alt="cyberchallenge t-shirt" width="600"/>
</p>

> My CyberChallenge.IT certificate

### Hobbies

In my free time I like to play CTFs and learn about new software and technologies in my personal homelab. I especially like self-hosting, tinkering with linux, and optimizing and automating everything to the extreme.

Beside the computer stuff, I spend my time learning new songs and improvising on my electric guitar, hitting the gym, and finding new albums to listen to.

I run [NixOS](https://nixos.org) on all my machines: desktop, laptop and home server, all managed from a single [flake](https://github.com/Zerodya/nix-config). Every machine is described in code and versioned in git, so I can rebuild any of them from scratch.  
Before that I daily drove [Arch](https://archlinux.org/) (btw), which introduced me to the KISS principle. Together with the Unix philosophy, it opened my eyes about how important it is to have modular, simple code as opposed to monolithic systems.

<details>
<summary><strong>KISS principle</strong> - <em>from Wikipedia</em></summary>

**KISS**, an acronym for **keep it simple, stupid**, is a design principle noted by the U.S. Navy in 1960. The KISS principle states that most systems work best if they are kept simple rather than made complicated; therefore, simplicity should be a key goal in design, and unnecessary complexity should be avoided.

</details>

<details>
<summary><strong>Unix philosophy</strong> - <em>from Wikipedia</em></summary>

The Unix philosophy emphasizes building simple, short, clear, modular, and extensible code that can be easily maintained and repurposed by developers other than its creators.

</details>

I’m also a strong supporter of Free Open Source Software. While having the code open to anyone might look like a security risk at first, I believe it is often more secure than closed source software actually is.  
FOSS ensures that the community is able to find and report potential security issues so that the developers are able to patch them right away ([XZ backdoor](https://en.wikipedia.org/wiki/XZ_Utils_backdoor) comes to mind).
This is also why I think it's very important to always update your software and systems to the latest version available.
