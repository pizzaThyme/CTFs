<img width="128" height="128" alt="red" src="https://github.com/user-attachments/assets/2876cf8a-e54c-452b-8d2c-a3941f3641c0" />

Not much to start with, so let's try:
> strings RED.png | grep 'picoCTF{'

That would have been too easy, what about just strings?

<img width="302" height="245" alt="Pasted image 20260207042526" src="https://github.com/user-attachments/assets/76f74d5a-7037-497d-a8f9-0f9d35eee15d" />

I'm pretty proud of this one. I was trying to decipher what this poem meant when I realized. 

<img width="302" height="245" alt="Pasted image 20260207042609" src="https://github.com/user-attachments/assets/4a0c7d65-4ca5-4bdd-b8fb-8416a8a80702" />

In steganography, LSB refers to the "Least Significant Bit." It basically means that you can change the last few bits of binary throughout the file to decode a messge. It makes changes to the file so insignificant that the human eye can't detect it. 

This was a good resource to help me learn more about it! https://www.lenovo.com/us/en/glossary/least-significant-bit/ 

I tried using "xxd -b" to look at the binary of the file, but again, it's a bit difficult to decipher with the human eye.

I learned that zsteg was a great tool for retrieving many different types of data hidden using steganography. 

<img width="1269" height="913" alt="Pasted image 20260207045507" src="https://github.com/user-attachments/assets/6c8a666c-431f-40dd-9636-c258f06d011d" />

Just running zsteg on the file extracted the LSB as seen in this first line of text. Decipher the base64 and you're done! picoCTF{REDACTED}

I also found https://www.aperisolve.com/ as an online tool if you don't have zsteg downloaded, and it was also able to retrieve the data quickly!
