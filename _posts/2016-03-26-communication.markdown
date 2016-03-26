---
published: true
code: 1
title: Communication
layout: post
category: computing
tags: CS3.9
summary: Computers communicate in many different ways, and there are a lot of factors that contribute to this.
---

# Communication methods
**Data Communication** is the transfer of data from one device to another through binary. Data can be sent through the following:

  * Copper cables
  * Fibre optics
  * Microwaves
  * Satellite (e.g. GPS, FreeSat TV)
  * Radio (e.g. Freeview TV, Wi-Fi)

Binary values have to be converted to electrical signals in order to be transmitted through electrical wires. Normally, 1 is a high voltage (>0v) and 0 is a low voltage (0v). The receiver must sample the signal at the same rate as the transmitter in order to recreate the correct binary value.

Data can be sent through electrical wires in either  **serial** or **parallel**.


**Synchronous data transmission** is occurring at the same time with the same speed. It is vital that communicating devices transmit and receive data at the same speed, so the computer sending it uses the system clock to control it. If they are not synchronised then data may be lost during transmission. This is used for high speed data transmission.

**Asynchronous data transmission** is when the transmitter and receiver are not synchronised, so they are synchronised for the brief duration of the transmission. The devices must also have the same baud rate. Parts of a transmission:

  * The **start bit** temporarily synchronises the sender with the receiver.
  * The **data** is sent.
  * The **stop bit(s)** give the receiver time to process the character being received and the start bit of the next character can be detected. This has to have a different value than the start bit.
  * The **parity bit** is used to ensure the data was sent correctly by checking that the number of ones in the data is an even number. An **even parity** is when the number of ones is even and has a value of **1**, while an **odd parity** is when the number of ones is odd and has a value of **0**.


## Serial
**Serial** is when the data is sent bit-by-bit through a single wire. USBs and SATA storage devices use this mode. This is the most widely used and is generally more efficient than parallel. It has many advantages:

* Connectors are smaller and simpler, thus serial is cheaper to manufacture.
* They are more reliable over long distances.
* High data transfer speeds are possible due to the lack of interference at high frequencies.

## Parallel
**Parallel** is when the data is sent multiple bits at a time through multiple wires. Old printer cables and internal computer buses cam use this mode. There can be skew in this mode as different wires have slight differences in their properties, leading to bits reaching the receiver at different times than they should. It has many disadvantages:

* It uses more wires, so it is more expensive to manufacture.
* Making the signal repeat with hardware is complicated.
* Cross-talk can occur between wires, corrupting data.

# Communication basics

**Bandwidth** is the amount of data that can be transmitted in a fixed amount of time, and is measured in Hertz (Hz) as it is a measure of frequency.

**Bit rate** is bits per second in a serial connection. This is proportional to bandwidth, and can be calculated using:

\`bit rate = baud rate * number of bits per signal\`

**Baud rate** is the rate at which data can be transmitted, where one baud is one electronic state change per second. If only 2 different values are transmitted, the baud and bit rate will be the same. This can be calculated with the following:

\`baud rate = bit rate / number of bits per signal\`

**Latency** is the delay between when something is initiated (usually some kind of event) and when its effects are first felt - basically, the equivalent of reflex time for computers. In regards to data communications, latency is the time delay between when a signal is sent and when it is received. Fibre-optics provide a lower latency compared to copper cable.

A **protocol** is a set of standardised signals, codes and rules used for data exchange between computers. These are combined when communication is taking place. There are many protocols used commonly:

  * TCP / IP (typical socket protocol)
  * HTTP (hypertext transfer protocol)
  * FTP (file transfer protocol)
  * HTTPS (hyper-text transfer protocol securererer edition with encryption between client and server)
  * Bit-torrent (for peer-to-peer file transfer)

Protocols handle the following:

  * Translation of data values into electrical signals.
  * Purpose of different wires in a cable.
  * How messages are formatted.
  * Special control messages (such as 'ready' and 'over') and how these can be represented.
  * Dealing with errors.
  * Keeping communications secure.
