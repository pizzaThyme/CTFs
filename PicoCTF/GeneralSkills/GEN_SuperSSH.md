<img width="439" height="554" alt="Pasted image 20260217042032" src="https://github.com/user-attachments/assets/2c1abccc-83a0-4833-98ce-f45322ed5245" />

This challenge sees us needing to make a secure connection over SSH. 

We first need to type "ssh" to initiate the connection over port 22. Next we need to specify what port we need to connect to so we can grab the flag using "-p". 

We then put the name of the user we need to connect as (ctf-player), followed by the "@" symbol, and the server to connect to (titan.picoctf.net). 

The final commands should look something like this:

> ssh -p 63435 ctf-player@titan.picoctf.net
>
> yes
>
> 1db87a14

<img width="815" height="457" alt="Pasted image 20260217042152" src="https://github.com/user-attachments/assets/54b773f0-cc68-4706-b1f6-b6ca9e467570" />

I intentionally added in my previous mistake as well to show you that we all make mistakes! If you are reading this, I highly suggest you learn some basic troubleshooting for when you run into issues.

Learn what the errors mean and diagnose your problems from there. You got this! picoCTF{REDACTED}
