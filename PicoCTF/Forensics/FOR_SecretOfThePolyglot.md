The Secret of the Polyglot! Sounds like a sequel in "The Mummy" series. :) 

The description for this challenge wants us to "extract all the information from this strange file."

I recently took SANS SEC450, and our professor made mention of these types of files. 

<img width="640" height="535" alt="Pasted image 20260218030047" src="https://github.com/user-attachments/assets/58508837-09b1-4ee6-b450-f35f29767e82" />

A polyglot is essentially a "wolf in sheep's clothing." It may say that it's one thing (and it may very well be), but there could be something malicious (a payload or script) hidden in the file as well.

The file name we see is "flag2of2-final.pdf", so let's go ahead and try to open the file as a PDF.

<img width="471" height="626" alt="Pasted image 20260218025140" src="https://github.com/user-attachments/assets/9ad11b30-c734-417d-a7fc-45ab67ad04eb" />

Right off the bat, we can see what appears to be the last portion of the flag in the PDF.

If we run the "cat" and "file" commands on the file, we'll see something different.

<img width="582" height="354" alt="Pasted image 20260218025459" src="https://github.com/user-attachments/assets/2b3d9136-3d75-4446-b3ee-b1fcd41d1ec0" />

<img width="651" height="70" alt="Pasted image 20260218025519" src="https://github.com/user-attachments/assets/3a1d03f4-83eb-4ba1-af3a-db11702ad740" />

We can even take this a step further using the "xxd" command to look at the hex of the data. 

As mentioned in a previous challenge, we can use the "magic bytes" of the file to help us determine what the type of file is. 

<img width="668" height="1226" alt="Pasted image 20260218025940" src="https://github.com/user-attachments/assets/edca92c8-b087-4756-bb6c-f8e7fc0a862d" />

Above you will see that the PNG bytes are seen first in the file, but farther down you can also see the PDF bytes as well. So this file is *both* a PDF and a PNG file. 

Now all we need to do is change the file format to a PNG, and...

<img width="499" height="956" alt="Pasted image 20260218025307" src="https://github.com/user-attachments/assets/84fb8495-a200-4c46-890f-1e1fadeef96d" />

We find our wolf / first half of the flag! picoCTF{REDACTED}
