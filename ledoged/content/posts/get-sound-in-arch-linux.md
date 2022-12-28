+++
date = 2022-12-27T05:00:00Z
images = ""
tags = ["arch"]
title = "Get sound in Arch Linux "
toc = true

+++
As a novice/beginner in using Linux, heck even a DIY distribution like [https://archlinux.org/](https://archlinux.org/ "Arch"). I think it's a very painful experience to even get sound in Arch. I figure if I write this down in a blog post so that others and myself can follow along make their own sound work.

Firstly make sure to upgrade Arch and packages.

    sudo pacman -Syu

Alright, now install `pulseaudio` which is like a software front-end which sits on top of `alsa` which is your kernel level sound mixer that directly talks to sound card. 

At the same time install `alsa-utils` for some useful tools.

    pacman -S pulseaudio alsa-utils

`alsa-utils` contain `alsa-mixer` which is good enough if you are a CLI freak. `alsa-mixer` is like a CLI volume control/mixer to control the volume coming out of your sound devices. Or if you don't like that, try to use `pavucontrol`. 

    pacman -S alsamixer pavucontrol

If you are lucky you should have a literal deafening sound when you try to play any application with sound. Try to go on Youtube and play  video and see if you are deaf or not 💀.

Or if you are unlucky like me.. I got no sound because I plugged my earphone into an earphone jack that is in my monitor which is connected through HDMI. If you are using `alsa-mixer` press the hotkey to switch your sound cards to HDMI and see if the volume there is muted or not, in my case it was. 

I am still experimenting with window managers (AwesomeWM) and trying to hotkey volume and get a widget that controls it. Once that's done I'll make another blog post on how to do it.