Alright, now we have to do some searching through a file to find the flag. Download the server.log file and open it. 

It's 2300 lines, so I'm not wasting my time scrolling through that. 

<img width="1055" height="643" alt="Pasted image 20260125065310" src="https://github.com/user-attachments/assets/246c90e7-d9ef-4a5c-8f26-7f6bc84ad0c9" />

When you do open the file though, you can identify certain log entries that relate to the flag. It's just a fragmented portion of the flag.

The name of the log type is "INFO FLAGPART", so let's use a simple grep command to search through the log and only pull these logs. 

<img width="568" height="442" alt="Pasted image 20260125065018" src="https://github.com/user-attachments/assets/ade58ce6-cd80-482c-99b0-40d5ed6bc2f6" />

Now you'll have to use your noggin and piece together the flag parts based on previous flags, but that's it! picoCTF{REDACTED}
