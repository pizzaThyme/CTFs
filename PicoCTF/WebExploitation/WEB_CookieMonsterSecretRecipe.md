Alright, we just need to get the "secret recipe."

<img width="773" height="657" alt="Pasted image 20260207035424" src="https://github.com/user-attachments/assets/0a200407-3589-4c5f-b923-90d420557a3b" />

So my immediate thought is to go to burpsuite and try manipilating the cookie field. 

I also try just a basic test authentication and get an Access Denied.

I go over to Burp and try sending the cookie field back to the site, but I'm still getting denied.

<img width="1275" height="807" alt="Pasted image 20260207035500" src="https://github.com/user-attachments/assets/daf414d7-ef66-46dc-86b0-1f8c204bf75a" />

Taking a closer look at the cookie field though, we can see that it *is* the secret-recipe. Okay, that makes things simpler. I thought that sending or manipulating the cookie would provide us with the secret recipe, but all we need to do now is decode it.

And it wouldn't be a recipe without our friend CyberChef!

<img width="1005" height="739" alt="Pasted image 20260207035526" src="https://github.com/user-attachments/assets/3bd023fa-9faa-4e59-9ef8-759bc4d9e33e" />

Head on over and we can try to decode the cookie. It should be pretty obvious based on the ending that this is a URL encoding. Looking at it further it also looks to end with two strings of "%3D".

This is the encoding for the equal sign (hint hint). Once you are able to create the recipe to decode, submit and you're done! picoCTF{REDACTED}
