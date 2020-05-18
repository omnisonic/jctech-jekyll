---
layout: post
title:  "Add SSH acces keys to Raspberry Pi"
date:   2020-05-18 12:04:51 -0700
categories: raspberypi
---



By this command, in your terminal, you can copy your ssh key to your clipboard:
pbcopy < ~/.ssh/id_rsa.pub

https://www.raspberrypi.org/documentation/remote-access/ssh/passwordless.md

https://pimylifeup.com/raspberry-pi-ssh-keys/


once you have copied your key use this code on the local machine to copy the key to the remote machine:

ssh-copy-id -i ~/.ssh/id_rsa user@ADDRESS


if you get ECDSA hose key warning:
https://dalanzg.github.io/tips-tutorials/posts/2016/06/03/how-to-fix-warning-about-ecdsa-host-key-when-ssh-connection/

remove the ip address from local machin using:


ssh-keygen -R 192.168.56.101
