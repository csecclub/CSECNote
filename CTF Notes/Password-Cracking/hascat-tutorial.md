# Hashcat Basics

> Hashcat is a password "recovery tool" but is CSEC we use it more for brute forcing. It's open source and can be used to perform various types of attacks 

<Badge type="info" text="For more info on hashcat click here the wiki!" /> 
<a href="https://hashcat.net/wiki/#specific_attacks">Hashcat Wiki</a> 

A simple and common way to use hashcat is by running this command which checks the rockyou.txt wordlist thats already inside kali linux or just downloading it here: (rockyou.txt)[https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt]

## Basic examples

running ```hashcat -h```
provides you with lots of options on how to use hashcat.

```
- [ Basic Examples ] -

  Attack-          | Hash- |
  Mode             | Type  | Example command
 ==================+=======+==================================================================
  Wordlist         | $P$   | hashcat -a 0 -m 400 example400.hash example.dict
  Wordlist + Rules | MD5   | hashcat -a 0 -m 0 example0.hash example.dict -r rules/best64.rule
  Brute-Force      | MD5   | hashcat -a 3 -m 0 example0.hash ?a?a?a?a?a?a
  Combinator       | MD5   | hashcat -a 1 -m 0 example0.hash example.dict example.dict
  Association      | $1$   | hashcat -a 9 -m 500 example500.hash 1word.dict -r rules/best64.rule
```

### trying out commands

given this ciphertext: 68a96446a5afb4ab69a2d15091771e39, find the plaintext using the rockyou breach wordlist

> to figure this out we would follow the wordlist + Rules attack mode

1. first enter your hash into a file (since its a string you can end it w/ .txt and it works)
2. run the command
``` hashcat -a 0 -m 0 hash.txt rockyou.txt ```
3. get the resulted output!

Answer: emilybffl

#### Online tools

* if you don't have time (in a ctf comp) and its an easy password cracking use this site!
* https://www.cmd5.org/