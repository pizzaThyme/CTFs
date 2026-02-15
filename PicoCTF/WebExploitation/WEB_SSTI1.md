The description states that "templating is a cool and modular way to build web apps." 

The page that loads is a simple HTML page that announces what you type in. Let's try a few things right off the bat like command injection to see if we can interface with the server. 

<img width="1284" height="524" alt="Pasted image 20260206061457" src="https://github.com/user-attachments/assets/18ed621a-9278-487b-9567-d6b916f05e6b" />

We should be seeing a hello AND a directory for netcat if this worked, so we can (maybe) mark this one off the list. 

I tried other tactics like inserting "'" or "`" to see if we could cause an error in the app. No dice. 

Hmmm, web app exploits are a little fresh for me still, so I took a hint. SSTI stands for "Server Side Template Injection". You can find more info here from BurpSuite / Portswigger.

https://portswigger.net/web-security/server-side-template-injection

We can try some different commands to see if it's vulnerable, like {{7*7}}. 

<img width="1289" height="449" alt="Pasted image 20260206062749" src="https://github.com/user-attachments/assets/514a6770-641c-441b-867f-6ee839d749c2" />

Okay, that makes sense. It's taking that 7 times 7 as input and output 49. 

I tried a couple of commands to see if we can determine what the engine is running the webpage. After a couple tries, it appears to be Jinja2 / Python based on the command below:

{{ self._TemplateReference__context.namespace.__init__.__globals__['os'].popen('cat /etc/passwd').read() }}

Perfect, that worked. Let's just see which directory we are in and look at the files:

{{ self._TemplateReference__context.namespace.__init__.__globals__['os'].popen('ls').read() }}

<img width="1298" height="617" alt="Pasted image 20260206061425" src="https://github.com/user-attachments/assets/3abdd507-e6db-40a2-b72f-11853d6b7109" />

You can probably figure out which file has the flag. Modify the command to read the file and that's it! picoCTF{REDACTED}
