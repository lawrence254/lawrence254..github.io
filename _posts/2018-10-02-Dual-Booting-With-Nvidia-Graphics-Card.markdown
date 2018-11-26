---
layout: post
title: Solving NMI watchdog soft bug lockup error
date: 2018-10-02
description: Solving The NMI watchdog soft bug lockup error wwhen trying to dual boot on laptops with nvidia graphics cards. # Add post description (optional)
img: gr404.jpg
tags: [Editing Grub,Grub,Dual boot,Nvidia]
author: Lawrence Karanja # Add name author (optional)
---

The main reason why most people dual boot is because they want to use another operating system for a specific purpose. The most common dual boot option is Windows+Linux where most people use Windows to perform common tasks(MS Office users...) or for gaming and Linux for programming or more power user usecases e.g server management. Dual booting for the most part is easy, until its not. One particular problem I have faced and which seems to be common for most people is the `NMI Soft bug lock up`. 

The bug occurs as a result of the kernel looping in the kernel mode for more than 20 seconds and not giving other tasks a chance to run. The particular problem occured when I was trying to dual boot Linux Mint alongside Windows on a machine with a dedicated `NVIDIA` graphics card. The point to note here is that this is not entirely an issue with the dual boot process itself than it is an issue with the drivers for NVIDIA not being under `FOSS` which means that Linux Mint doesn't include them in the distribution when it is shipped.

And now to the solution. It quite easy but requires abit of care so as not to mess up with other important settings, remember __"With great power comes great responsibility"__. This will require with tinkering with the Grub bootloader code in order to first ignore trying to load up the graphics card. In order to alter the Grub menu, you can access it at startup or use a live disk to edit the `/etc/default/grub` grub file. In this article we are going to deviate a little and change the grub menu at startup/boot. To do this we start/restart and when the grub menu shows up press the `esc` key followed by `e` in order to get into edit mode. 
While in the edit window, move to the line that begins with `linux` and add `nouveau.modeset=0` to the end. You should now be able to boot into your system. After booting up your next step should be able to download the proprietary linux drivers for your particular graphics card. In order to do this, you first need to add a repository containing these drivers. Open your terminal and type `sudo add-apt-repository ppa:graphics-drivers/ppa` to add the repository. You should get a prompt asking you to accept the repository signing keys, accept and continue installing the PPA.

After the PPA installation, run `sudo apt update` and then `sudo apt install nvidia-387` to install the latest graphics drivers for NVIDIA graphics cards. Reboot your machine after this and go to settings and access `Software & Updates` and find the `Additional Drivers` tab and select the required driver version and click `Apply Changes`. And that's it! You now have your NVIDIA drivers installed on your sparkling new Linux Mint system.

:warning: Fair warning: Editing the Grub file wrongly will render your system unusable :no_entry_sign: or may have undesirable side effects, please only follow the above instructions if you're sure about what you are getting into :alien:

:neckbeard: Lawrence Out!