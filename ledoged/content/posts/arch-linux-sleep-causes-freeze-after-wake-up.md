+++
date = 2023-02-07T16:00:00Z
images = ""
tags = ["arch"]
title = "Arch Linux sleep causes freeze after wake up."
toc = false

+++
# Arch Linux freezing after sleep.

## The problem

Whenever I do `systemctl suspend`, system sleeps normally. But after pressing the power button and power back on, PC totally freezes. No mouse movement, can't change tty. Doing this without `startx` will result in same thing but tty can change except no response from keyboard at all. 

## Tried solutions

There are multiple posts in the forum discussing this problem with non leading to a actual solution. I used `journalctl` to figure out what errors could have resulted from previous boot. But there was non that was significant. The forum posts mentioned nouveau graphic drivers suck at power management, and I should install Nvidia proprietary drivers instead. But Nvidia drivers for my PC is so ancient its not updated in probably 10 years. Another mentioned how the WIFI driver would also affect the sleep process due to not powering off properly.   

## Conclusions

I am stuck for now. This is extremely annoying as I use sleep almost daily on my Windows installation. This also confirms my that Linux is not that great for older hardware probably due to problems like this that don't exist on Windows. 