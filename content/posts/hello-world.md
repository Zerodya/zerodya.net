+++
title = "Hello, World!"
date = 2022-06-30
aliases = ["/hello-world/"]
+++

> Edit (October 9, 2026): Please note that the following information is mostly outdated since my server setup has changed since this post.

Welcome friend! This website is self-hosted in my personal homelab! What that means is that it lives inside a server in my house (who would've thought).
<!--more-->

# A website with speed and security in mind

I had some experience with cloud-hosted Wordpress already, but it has far too many issues to be a viable self-hosted solution, both for speed and security reasons.

After a bit of research I eventually chose [Ghost](https://ghost.org/) because of its **performance** and user-friendliness.  
The theme I'm using is a fork of the [Dawn](https://github.com/savyajha/Dawn) theme with jsquery removed to make it even faster, and after a few tweaks I have to say I'm pretty happy with the results.

![](/content/images/2022/06/webdev-score.png)

*Website stats from [web.dev/measure](https://web.dev/measure)*

As for the security part, the things I wanted the most are protection from bots, and hiding my IP address. After some more research I found solutions like [Authelia](https://www.authelia.com/) and [Fail2ban](https://www.fail2ban.org) for authentication and spam protection, but I wasn't fully satisfied yet... until I learned about [Cloudflare Tunnel](https://www.cloudflare.com/products/tunnel/).

In fact, my website stack goes like this: `Proxmox server > LXC container > Nginx Proxy Manager > Cloudflare Tunnel > Ghost Blog`, and Cloudflare Tunnel has probably the most important role in it.

But why is it so great? Well, it makes it really easy to **block bots** and DDoS attacks, it lets you add authentication methods, **hides your IP address** and automatically caches your website to shorten page loads time.  
Not just that, but by installing the [cloudflared](https://github.com/cloudflare/cloudflared) client on the host machine, it also acts as a **Dynamic DNS**, so this makes it a really good solution for self-hosters without a public static IP address.

# Simplicity first

This website is pretty simple right now, and while I will surely upgrade it over the time, I will always keep it as light and simple as possible.

Here are the **main features** of this blog:

- **Comment system** based on GitHub discussions, [giscus](https://giscus.app/)
- **Syntax highlighting** for code snippets using [Prism.js](https://prismjs.com/index.html)
- **Table of contents** with [Tocbot](https://github.com/tscanlin/tocbot)

# What's next?

This blog will mostly focus on **Cybersecurity**, Free Open Source Software, and privacy guides. You can expect **writeups**, guides, advices, and stuff about my personal projects.

Most modern blogs only care about making money off of ads, so they are full of useless text to waste your time before you can reach the actual useful information you were looking for.

Instead I aim to write posts with **less filler text and more actual content**.

------------------------------------------------------------------------

Before you go, remember that you can add my [RSS feed](https://zerodya.net/atom.xml) to your favorite reader app.

Thanks for stopping by!
