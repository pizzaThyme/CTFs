Okay, just need to find the flag in this zip file, no problem. 

Let's go ahead and extract that to the desktop. 

<img width="1269" height="496" alt="Pasted image 20260205052749" src="https://github.com/user-attachments/assets/12fb94fc-1788-47e1-b1cf-fa47913b7160" />

We can see it's definitely a disk file. Tried running "strings" on this and the output is wayyyyy too much.

Change it to an .iso file and open with disk image mounter. Open the volume. Wow, there's still a lot of data to go through. 

I searched for a file named flag within the folder, but they didn't make it that easy.

I also tried the "grep" command in the new folder, but it was taking a long time. 

Hint says to use strings, so let's go back to the top and rename it to a .dd file and try grep from here:

> strings disko-1.dd -n 8 | grep 'picoCTF{' 

It seems so simple in retrospect, but the with the grep and strings command you'll find the flag in no time. picoCTF{REDACTED}
