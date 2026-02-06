Cryptography is fun, let's try and crack some passwords! 

If you're using Kali Linux, I highly suggest you familiarize yourself with hashcat. It is an amazing tool once you learn HOW to use it. 

First let's connect to the service. Okay, no response. Hmmm.

We can try to pipe it to cat? Or redirect it using netcat to a flag.txt file? 

Nope, just a typo. It has been a long day for sure. Okay! Actually connect to the service on the correct port. 

Alright, we are given a password hash to crack, what now? 

> hashcat --identify 'insert hash' (let hashcat do the thinking for you)

> hashcat -a 0 -m 'mode identified' 'hash' /usr/share/wordlists/rockyou.txt (attack mode 0 is a straight attack using a wordlist)

Let him cook. It shouldn't take you long to find the first password.

Alright, here is where I tell you that I'm kind of lazy. You "could" run hashcat, OR you can go to https://crackstation.net/ and insert the hash there. After an annoyingly long CAPTCHA (Am I a bot?), I was able to get the first password. 

This is an online DB of passwords and hashes. It probably won't work for very long or obscure passwords, but it's always a really good resource if you're in a rush for a CTF.

Use whichever method you want to nab the passwords, and you get sent the flag. Happy Hunting! 

<img width="910" height="762" alt="Pasted image 20260206073117" src="https://github.com/user-attachments/assets/3d8960a7-91c6-4d2e-b9fc-d2f9f136ecb1" />

picoCTF{REDACTED}
