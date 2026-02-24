This challenge begins with this description, "Someone's commits seems to be preventing the program from working. Who is it?"

If we unzip the challenge files and change directory to the drop-in folder, we can see the message.py script. 

If we look closely at the the script, we can see that it is missing a closing parenthesis.

<img width="410" height="80" alt="Pasted image 20260221062833" src="https://github.com/user-attachments/assets/12b14c6d-6c4a-4ba5-8039-0d9996fed71c" />

The program will no longer print correctly, so we need to identify who made the change. 

Use "ls -la" to see all the files (including the hidden files / folders)

Let's now use "cd .git/logs" to change to the logs folder and determine what change was made.

There is a HEAD file that we can open with "cat", or you can use "head" to see the first 10 lines. 

<img width="573" height="365" alt="Pasted image 20260221062706" src="https://github.com/user-attachments/assets/036c99cf-4796-40d6-af7a-20a7ee32ac46" />

We can see that above all of the "important business work" commits, there is a commit to "optimize the file size of prod code". 

This must be the change to the file as we found our flag! picoCTF{REDACTED}
