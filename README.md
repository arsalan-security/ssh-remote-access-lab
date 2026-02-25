SSH Remote Access Lab

## Overview

In this lab, I set up remote SSH access between a Kali Linux machine and an Ubuntu machine in my home environment. The goal was to understand how remote login works and how services are exposed over a network.

## What Went Wrong

At first, I tried to connect from Kali using SSH, but the connection failed.

When I scanned the Ubuntu machine using Nmap, all ports appeared filtered and port 22 was not open. I initially did not understand why this was happening.

My mistake was assuming that SSH was already installed and running on Ubuntu. I also confused local terminal access with remote access. I did not yet understand that a service must be installed and actively listening on a port to accept remote connections.


How I Fixed It

I installed the OpenSSH server on Ubuntu and started the SSH service. After that, I verified that the service was running and scanned the machine again using Nmap. This time, port 22 was open.

I then could successfully connect from Kali using: ssh username@target-ip

and gained remote terminal access.


What I Learned

- The difference between local access and remote services  
- What it means for a service to be "listening" on a port  
- How to verify open ports using Nmap  
- Why SSH must be installed and running before remote access is possible  

This lab helped me understand basic networking concepts and remote authentication in a practical way.
