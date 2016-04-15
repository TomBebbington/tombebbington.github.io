---
published: true
category: computing
---

**Encryption** is scrambling data so others cannot view it unless they know what method you used to encrypt it and what key you used.

**Decryption** is turning this scrambled data back into plaintext.

**Plaintext** is a human-readable form of data.

**Ciphertext** is encrypted data.

Encryption is used in a lot of scenarios:

+ Websites that use **HTTPS** security (with **SSL** encryption) which use digital certificates to make sure your personal information can't be read while the data is being transmitted over the network.
    + Online banking
    + Authentication on online shops
    + Authentication of e-mails
    + Submitting examination results

# Encryption methods

## Caesar Cipher
This is named after a Roman emporer, and is where letters are shifted a set number of places left / right by a certain number of places to encrypt, then to decrypt they are simply shifted in the opposite direction. This can easily be cracked using **frequency analysis** or **brute force**.

## Vernam Cipher
This was invented to enforce data security between telex machines during World War 1. This is known as a **one-time pad** as the key used to encrypt / decrypt a message is discarded after one use. This is completely mathematically secure and is to this day unbreakable. This uses a random sequence of letters and symbols with a length at least the length of the text to encrypt, that must be truly random. Because the sender and receiver both need the key to encrypt / decrypt data.


### Encryption
The algorithm is as follows for each character (where X is the character, K is the key, and Y is the result):

$$ Y = (X + K) \mod 26 $$

### Decryption

To decrypt:

$$ X = (Y - K) \mod 26 $$

# Forceful decryption methods
## Frequency analysis
This only works for substitution ciphers, and is where you record how many times each letter occurs in the encrypted text, then use this to make educated guesses on what each letter corresponds to based on their frequency in English in general. It's basically computer hangman. The letter 'e' appears most frequently in English according to a number of records.

## Brute force
This is where you encrypt every possible combination of text in order to find the one that is the same as the encrypted value you want to decrypt. This takes a very long time as it runs for so long.
