Alright, so we need to log into this site, as ctf-player@picoctf.org is hiding something on this site.

We're led to believe the developer left us a way in though. Thanks pal.

<img width="1273" height="1221" alt="Pasted image 20260205034300" src="https://github.com/user-attachments/assets/3a7ad698-8be7-4133-b0e5-1624c20929ab" />

Let's try sending a bad pass and see what happens. Invalid password, okay.

Let's try the page source then. We can see comments stating the below:

\<!-- ABGR: Wnpx - grzcbenel olcnff: hfr urnqre "K-Qri-Npprff: lrf" -->
\<!-- Remove before pushing to production! -->

Shall we jump to CyberChef? It doesn't immediately scream base64, but it could be just a basic rotation since I'm not seeing any odd characters. 

<img width="1039" height="874" alt="Pasted image 20260205034619" src="https://github.com/user-attachments/assets/3b605357-e065-4b97-ad36-15d41663368c" />

ROT13 should do the trick. And bingo, we now have a header to pass.

This can be passed from the browser, or if you're more comfortable, you can also use BurpSuite or ZAP. 

Intercept the page using the Burp proxy and add in the header and field to send.

<img width="1555" height="1043" alt="Pasted image 20260205035444" src="https://github.com/user-attachments/assets/084520f2-9b72-4cde-8a79-fb9e8edebd13" />

Voila, we are met with the flag! picoCTF{REDACTED}
