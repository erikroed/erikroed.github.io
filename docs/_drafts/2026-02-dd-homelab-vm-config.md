---
layout: post
title: Homelab VM Config
date: 2026-02-12 18:00:00 +0100
tags:
  - automation
  - ansible
  - homelab
  - config
  - proxmox
  - vm
---
For a long time, my home lab have been in the loop of restarting the things I'm working on. Like my dev environment (incoming post about this later), I'm usually starting on something until I'm taking a break and when I'm getting back to it I'm having a quick look and concludes that it's best to just start all over to get the latest and greatest. This also applies to my home lab and all the stuff I have on my "I'm going to have \<insert something here> in my home lab, and it's going to be fully automated and soooo easy to use when it is finished". 
This time I have started with an empty repo and decided that instead of striving for perfection, I will just start out by configuring my devices with the following:
* Update packages
* Create a user
* Copy my public ssh key
* Install tools for k8s - kubectl and k9s
For this I will utilize ansible to create a playbook that I can use on my current devices including my existing VM's on the proxmox server and potentially future VM's. 
