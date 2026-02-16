Our clue from the challenge description is: "Are overflows just a stack concern?"

I am still pretty rusty at C, but I wanted to give it a try. 

Let's first connect to the challenge and see our options. 

<img width="1282" height="1206" alt="Pasted image 20260216075900" src="https://github.com/user-attachments/assets/45bc9534-3add-4506-9e61-67e474c0052a" />

So my first thought is that when I entered my choice to see the heap state again, the state does not change. That means that there is likely no Address Space Layout Randomization (ASLR).

If there was, the state should change and the address for the buffer and safe_var would have been randomized to help prevent attacks. 

<img width="1271" height="259" alt="Pasted image 20260216075940" src="https://github.com/user-attachments/assets/380b3745-5d34-4c74-ab4f-64819823077b" />

I tried writing 16 "0"s to the data to see if we could force an overflow (should have been 17), but we can see that it is added into the heap data. 

Seeing as how there are a lot of 16 bit and 32 bit architecture, I wanted to see if entering 17 or 33 "0"s would overflow the buffer. 

<img width="1264" height="423" alt="Pasted image 20260216080031" src="https://github.com/user-attachments/assets/3fe54a96-15d1-4c80-90d6-563935d682ca" />

After entering 33 "0"s into the buffer, we can see that the safe_var was changed from "bico" to "0", meaning that we successfully executed a heap overflow!

<img width="1276" height="750" alt="Pasted image 20260216081151" src="https://github.com/user-attachments/assets/377e9f57-066d-4968-bfbe-f036332414fb" />

I wanted to better understand what caused the overflow, and for that we need to look at the addresses of the Heap State. We can look at the difference of the hex using RapidTables.

The actual difference between the two on the stack translates to 32 in decimal. This is why we were able to cause the overflow with 33 characters.

<img width="1256" height="1203" alt="Pasted image 20260216080610" src="https://github.com/user-attachments/assets/362dc936-d283-4a09-9c03-d7c0370ef3f8" />

I also dived into the actual code of the challenge file, and we can see that the "scanf" function was used to take our input data. This looks to be where the code takes out input_data.

Doing some research, this appears to be unsafe compared to other input methods, like "fgets" or "sscanf". 

All in all, this was a really fun challenge! picoCTF{REDACTED}
