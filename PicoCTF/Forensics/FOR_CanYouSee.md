We have a new forensics challenge to find some information inside the jpg file below.

![ukn_reality](https://github.com/user-attachments/assets/c5539c64-58a6-4414-bf51-dbe3dd75b032)

There are many ways to skin a cat, but I like to always go with the lowest hanging fruit. You can run "cat" (way too much information unless you use "grep" to search the file), "strings" (also good, but you should minimize your search with "grep"), or "head".

This will pull the first 10 lines of the file, which is usually enough for finding magic numbers / metadata. 

<img width="1019" height="275" alt="Pasted image 20260219061502" src="https://github.com/user-attachments/assets/9aa26b3b-2858-473c-a143-11ca9ed6db8e" />

We can see what looks to be an interesting base64 string in the attribution URL.

We can also use https://exif.tools/upload.php if you want some more details on the metadata. 

<img width="1057" height="1008" alt="Pasted image 20260219061601" src="https://github.com/user-attachments/assets/f186cf03-7c01-4d57-a5a9-42c3953581a2" />

You can even use CyberChef to upload the file! This is probably the easiest if you know what you're looking for. Just upload, snag the base64, and decode that as well!

<img width="1016" height="894" alt="Pasted image 20260219061707" src="https://github.com/user-attachments/assets/b4e51a4d-f6f3-4b8c-b660-2f0618ed6d5f" />

Just decode the base64 in CyberChef now and you're golden! picoCTF{REDACTED}
