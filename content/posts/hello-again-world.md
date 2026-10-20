+++
title = "Hello again, World!"
date = 2026-10-20
+++

About four years ago, I wrote my [first post](@/posts/hello-world.md) on a Ghost blog running in a Proxmox container. A lot has changed since then: the blog, the server, and even the operating system on every machine I own. Here's how things are going in my Linux and Self-Hosting journey.
<!--more-->

# The blog, then and now

The old blog ran on [Ghost](https://ghost.org/) on my Proxmox server, inside an LXC container. The stack went like this:

`Proxmox server > LXC container > nginx > Cloudflare Tunnel > Ghost Blog`

Ghost served me well, but it's a full web application, with a database, an admin panel and a Node.js server, all of which need updates, backups and attention. And all I really wanted was to write some posts in Markdown.

So the new blog is a **static website**, built with [Zola](https://www.getzola.org/). Every post is just a Markdown file in a [Git repository](https://github.com/Zerodya/zerodya.net), which I write in VSCode (err, [VSCodium](https://github.com/VSCodium/vscodium)... I don't want any of that [MicroSlop](https://knowyourmeme.com/memes/microslop)). 

After I push my commits to Github, I simply update the blog channel in my NixOS config and start a remote rebuild from my desktop. My server then builds the website into plain HTML files, and that's it. No database, no admin panel, no server-side code to keep updated, and most importantly: **nothing to hack**.

This is the stack now:

`Markdown on GitHub > Nix builds the static site > nginx > Cloudflare Tunnel > this blog`

Some things are the same, just simpler:

- **The comments** still use [giscus](https://giscus.app/), and all the old comments came along with the posts.
- **Syntax highlighting and the table of contents** used to need JavaScript libraries (Prism.js and Tocbot). Now Zola generates both when it builds the site, so the browser doesn't have to do anything.
- **The theme** is my own custom version of [Hacker](https://github.com/en9inerd/zola-hacker).
- **The old links still work.** Every post from the Ghost blog redirects to its new address.

In the first post I promised I would always keep this website as light and simple as possible, and I think this is the lightest and simplest it has ever been.

# From Proxmox to NixOS

The biggest change isn't the blog, though. It's what runs it.

My old Proxmox server was a collection of LXC containers, each configured by hand. The problem was that I kept configuring things and then forgetting what I did, and how I did it. So I started documenting my changes, but keeping the documentation up to date as a single person was a battle I kept losing.

Then I found [NixOS](https://nixos.org/) a few years ago, and I couldn't believe it. I could build the entire operating system from a declarative configuration, share the common parts between all the machines I own, keep track of *all* the different os settings I change, have rollbacks when things go wrong, and orchestrate all of this from a single git repo? Sounded too good to be true, yet it is.

With NixOS **the code *is* the documentation**, and it's the only source of truth: if something isn't in the config, it doesn't exist on the machine. If something breaks, I roll back to the previous version. If a disk dies, the same config rebuilds the same system. I have way less worries now and I might have finally achieved peace of mind.

My NixOS journey started on my desktop in early 2024, and although the initial learning curve was steep, I'm glad I made this choice and I've slowly tried to move every machine I own to NixOS, so here we are.

## The machines

Every machine hostname is inpired by **Evangelion**, just in case anyone thought NixOS alone wasn't nerdy enough.

<p align="center">
    <img src="/content/images/2026/10/magi.png" alt="Magi" width="350"/>
</p>

### The EVA units
- **EVA-01** and **EVA-02**: My desktop and laptop.

### The MAGI supercomputers
- **Melchior**: my main server, a Lenovo ThinkCentre M720q
- **Casper**: a Raspberry Pi 4 that will become the second MAGI for redundant Pi-Hole DNS and other services.
- **Balthasar**: Currently nothing, because my bills are high enough right now.

### The NERV scientists
- **Ritsuko**: a recovery USB that lets me SSH into my machines with all the tools I need to fix them when something goes wrong.

## Meet Melchior
My homelab has evolved a lot through the years, and honestly, at some point it just became a mess. That's why I decided to start fresh and try to keep things clean and tidy now, just like what I'm trying to do with NixOS.

<p align="center">
    <img src="/content/images/2026/10/melchior.jpg" alt="Melchior" width="800"/>
</p>

> Melchior on the left. My router in the center, on top of a cheap laptop cooling pad for hot seasons. A switch on the right.

# What's next?

In my first post I said this blog would focus on CyberSecurity and Self-Hosting. That hasn't changed, but these topics will probably be mostly explored through NixOS colored lenses from now on.

Future posts will talk about the security aspects of NixOS, more self-hosted stacks, and other useful Nix shenanigans I discover.

------------------------------------------------------------------------

Thanks for stopping by, again!
