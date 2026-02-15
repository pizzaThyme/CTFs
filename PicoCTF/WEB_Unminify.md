We begin this challenge and are told that the code has been squished so that the site loads faster.

<img width="2557" height="1242" alt="Pasted image 20260215063251" src="https://github.com/user-attachments/assets/fe0db912-de5a-4a69-a929-8772cff8f77a" />

Navigating to the page, we can see that there's not much here to click or navigate through. 

The site does mention that, "If you're reading this, your browser has successfully received the flag."

My first thought is that we received a cookie, so let's start by inspecting the page. 

<img width="1369" height="573" alt="Pasted image 20260215063425" src="https://github.com/user-attachments/assets/59d3a619-64c2-4a3f-8e26-ac42c5defddc" />

Once we do inspect the site, we can immediately find the flag format in the code of the site. 

At this point, you could continue to open all of the variables in the inspector tool, hit Ctrl+U, or add "view-source:" to the beginning of the URL to view the source code. 

Once we do, we can see a long line of code. From here you can edit the page to wrap long lines of code.

<img width="2549" height="278" alt="Pasted image 20260215064149" src="https://github.com/user-attachments/assets/9ede2b5e-8b1e-4c11-9925-323dce6eacc3" />

Once we wrap the page, the flag should stick out like a sore thumb. picoCTF{REDACTED}
