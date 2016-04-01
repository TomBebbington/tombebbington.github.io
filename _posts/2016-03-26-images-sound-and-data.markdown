---
published: true
code: 6
title: Representing images, sound and other data
layout: post
category: computing
tags: CS3.5
summary: Data like images and sound is represented by bits on a computer, but there are different ways of storing them.
---

# Bit patterns

Bit patterns can be used to:

  * Make simple white/black bitmaps, where 0 is black and 1 is white.
  * Make **RGB** colours.

# Analogue and digital

## Analogue data

**Analogue data** is data represented physically so varies smoothly. Examples include: + Sampled audio + Gamepad input

## Digital data

**Digital data** is data represented as discrete and discontinuous, usually with two options for a state being set and a state not being set. It can be stored, sent long distances etc. all without degradation, but it needs more expensive equipment.

# Analogue / digital conversion

An **analogue-to-digital converter** converts a continuous physical quantity, such as voltage, to a digital number representing the size of this quantity. This introduces a small amount of error.

A **digital-to-analogue converter** converts digital data into analogue signal or voltage levels.

To convert analogue sound waves to digital ones the sound waves are recorded at a fixed interval using a microphone device, then every sample is quantised by giving the wave height an integer value and then converting this to binary.

# Bitmapped graphics

**Pixels** are the smallest possible addressable area defined by a solid colour, represented as binary, in an image. 

**Bitmaps** are images stored in memory where there are a set number of pixels making up the image. The **dimensions** of the image are given in the form `width x height`, and the **colour depth** is the number of bits per pixel. The **resolution** of an image is the number of pixels per inch, where 72PPI is the standard and 300PPI is required to print with photographic quality. Generally, storage requirements can be expressed as width x height x colour depth. The majority of image formats have 3 bytes or 4 bytes per pixel, depending on if it has an alpha channel. Most of these use RGB to represent colours where how much red / green / blue makes up a colour is represented by integers. The size of a bitmap can ve calculated by:

$$ width \times height \times colour_depth $$

## Metadata

The metadata of a bitmap contains:

  * A **header** to confirm it is an image of a certain format.
  * Its **width** in pixels. 
  * Its **height** in pixels. 
  * The **image resolution** in PPI. 
  * The **colour depth** (usually 3-byte or 4-byte).

## Vectors

**Vectors** are images stored in memory where it lists each geometric shape, line and object in the image. Only the information needed to render the image is saved, so it often results in a smaller file size for simple images and are completely scalable, so are better for use on webpages. Their individual pixels cannot be edited unlike bitmaps though, so you need seperate programs to edit / create these, such as: 
* Inkscape.
* Adobe Illustrator.
* Adobe Flash MX.

# Digital representation of sound

Sampling is a static representation of the sound at a given time. The closer together the sound waves, the higher the pitch of the sound.

## Sample resolution

The **sample resolution** of audio, also known as the **bit depth**, is the number of bits of information for each sample. Increasing this increases the quality of the audio, but decreasing it decreases the quality of the audio. This is because every point is represented by a unique binary value.

## Sampling rate

The **sampling rate** is the number of samples of sound made per second, in hertz. The higher this is, the smoother the representation. To calculate the size of an audio file, use this, where T is the total size, s is the sample resolution, r is the sampling rate and t is the number of seconds:

$$ T = s \times r \times t $$

## Nyquist theorem

Harry Nyquist discovered in 1928, that in order to produce an accurate recording, the sampling rate must be at lest double the highest frequency is the sample. Basically, where `s` is sampling rate and `f` is frequency, the minimum sampling rate to :

$$ s = 2 \times f $$

# Musical Instrument Digital Interface

This is a set protocol that allows computers to synthesise sounds from a variety of instruments, and to connect to a musical instrument directly. This is to sampled audio as vectors are to bitmaps: you can recreate sampled audio at as high a definition as you want with MIDI, as it just synthesises sounds based on instructions to the MIDI device telling it what instrument to play, how to play it etc.

## Examples

Some examples of where MIDI is used:
* Software sounds
* Mobile ringtones

## How it works

The MIDI file generates music using a timed sequence of instructions,and can send messages to other devices to:

* Synchronise tempo 
* Control pitch 
* Volume changes 
* Vibrato and audio cues

## Metadata

This metadata contains:

* A note's duration 
* The instrument to play a note with 
* Volume 
* Timbre 
* Channel

# Data Compression

There are compelling reasons for compressing data:

  * **More efficient** storage.
  * **Faster transmission** of data.

Some examples of where compression is used:

  * **JPEG** images average out colours in a form of lossy compression.
  * **MP3** music reduces bitrates in a form of lossy compression.

## Lossy compression

This is when unneeded data is not preserved.

## Lossless compression

This is when unneeded data is preserved.

  * **Run-Length Encoding** is where you reduce data to a stream of distinct sequential values and how often they are repeated.
  * **Dictionary-Based Encoding** is where you store each distinct value in a dictionary then reduce the data to keys into this dictionary. This can be done repeatedly with groups of data in order to further compress the data. Its efficiency increases as the file size increases.

# Encryption

**Encryption** is the transformation of plaintext using some ciphertext from one form to another in order to prevent unauthorised third parties from reading it.

**Plaintext data** is the original textual data.

**Ciphertext** is the message after encryption.

**Cipher** is the encryption algorithm, such as RSA.

## Symmetric ciphers

A **symmetric cipher** is one that uses a single key to both encrypt and decrypt data. Examples of this includes the **Caesar** and **Vernam** ciphers.

### Caeser cipher
The **Caesar** cipher is based on substitution, where the values are shifted by a certain value and to be decrypted have to be shifted in the reverse direction. The most common form of this is the *ROT13* function, which shifts a letter by 13 places.

This is easy to crack as there are only so many combinations.
  * The **Vernam** cipher is a one-time pad using the bitwise *XOR* operation with the random key to make it unbreakable.

## Asymmetric ciphers

An **asymmetric cipher** is one that has a public key and a private key. The public key decrypts data while the private key encrypts data.