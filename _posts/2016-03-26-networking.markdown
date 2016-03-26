---
published: true
title: Networking
layout: post
code: 2
category: computing
tags: CS3.9
summary: Computers have so many ways of connecting to each other in networks that lots of protocols and kinds of these networks have been created.
---

# Network topology

A **local area network** is a small interconnected area. It typically consists of several clients, a server and a router.

A **router**, which can be software or hardware, does the following:

  * Processes packets by seeing where to send them from their headers.
  * Acts as a bridge between the LAN and the internet.
  * Acts as a modem, which translates digital signals (0s and 1s) to analog signals.
  * Can have a firewall to block specific ports.
  * Provides a WAP.

A **wireless access point** provides a 'Wi-Fi' signal which is done over radio. There are several protocols that they can use, such as *WPA* and *WEP*, which have various advantages and disadvantages.

A **switch** is used to connect two devices in a network.

A **wide area network** is spread over a wide area. The world-wide web is by far the most used WAN.

A **media access code** is the unique physical address of a machine connected to a network.

A **network interface card** is what a computer uses to connect to a network - the type of this dictates the speed of transmission. This will have a unique MAC address.

A **topology** is a logical network layout, where the network can be LAN or WAN. There are several kind of topologies.

## Bus topology

A **bus topology** is one where a backbone cable connects all the devices and has terminators to absorb reflected signals. **Coaxial cables** are used for the backbone and to connect computers to the backbone. Data is transmitted along the backbone to every single workstation but only the workstation whose MAC address it is intended for will accept and process this message. Therefore, each station has equal transmission priority.

They use a **CSMA / CD protocol** to avoid and manage data collisions - devices transmitting at the same time are forced to pause for a random amount of time before trying to transmit data again.

Advantages:

* Installation is cheap.
* Easy to add devices.
* Less cabling needed.
* Works well for small networks.

Disadvantages:

* Depends on the backbone.
* There's a limit on how many devices can connect.
* Problems are hard to isolate.
* Response rate can be slowed because of shared cable.

## Physical star topology

A **physical star topology** is one that is connected by Ethernet cables. A **hub** broadcasts to every connected workstation whereas a **switch** broadcasts only to the relevant workstation.
Advantages:

* One cable going down does not bring down the whole network.
* Tracking down device and cable problems is easy.
* Can be upgraded to higher speeds.
* Has lots of support as it is the most popular.
* Hubs provide a centralised management.

Disadvantages:

* Required more cabling than bus networks.
* If the central hub fails, the whole network goes down.
* Costs are higher than most bus networks.
* More expensive to maintain as specialist knowledge is needed.

# Types of networking

## Peer-to-peer networking
**Peer-to-peer networking** is when devices communicate directly to each other without any in-between devices, as a result devices are self-organising and distribute control. However, it is vulnerable to the following:

  * A **Distributed Denial of Service** attack.
  * The network being **poisoned** / given bogus data.
  * Your IP address could be leaked and lots of things can happen as a result. If P2P file sharing is taking place, your password can be brute forced and files found.
  * **Unfairness** in sharing.
  * This can be outright blocked.

## Client-server networking
**Client-server networking** is when devices fall into one of these categories:

  * **Servers** provide services to clients, such as web services and e-mail.
  * **Clients** use services provided by servers, such as in a web browser, and an e-mail client.
