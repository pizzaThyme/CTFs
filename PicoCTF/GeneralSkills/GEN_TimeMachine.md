We first need to download and unzip the challenge files. Use "ls" to list the files and you will find a single message.txt file. 

<img width="613" height="34" alt="Pasted image 20260217040713" src="https://github.com/user-attachments/assets/1cac9761-c67a-4b47-91b0-cfc8265a9983" />

There are no other machines to connect to, so let's see if the folder has anything more for us. 

> ls -la

This will list all of the files in the folder, including the hidden files and folders like you see below!

<img width="292" height="70" alt="Pasted image 20260217040749" src="https://github.com/user-attachments/assets/ff44ab8b-6f67-485a-89b1-77783b14f8fd" />

Because commit history was mentioned, let's change the directory to the .git folder. 

> cd .git
>
> ls -la

We can now see a lot of new files and folders in the .git directory. 

<img width="322" height="200" alt="Pasted image 20260217040827" src="https://github.com/user-attachments/assets/2b493c2e-4fb5-4935-8990-71b79064d761" />

> cat COMMIT_EDITMSG

Use the cat command to read the file and find your flag! picoCTF{REDACTED}
