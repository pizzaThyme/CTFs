Another metadata challenge for the image below.

![img](https://github.com/user-attachments/assets/97f061d6-2c28-4aea-81fc-cbaae2b70d4c)

Alright, let's try something different. I learned about steghide, right? Let's see if there's more to this one. 
I open steghide and try to access the metadata, but the file is locked with a password. 

Alright, let's try to use a password list and a simple bash script (you can vibe code here if need be):

for password in $(cat rockyou.txt); do steghide extract -sf img.jpg -p "$password" > /dev/null 2>&1

if [$? -eq 0 ]; then

  echo "Password found: $password"
  
  break

fi 

done

Still not found using this method. Let's try a different route.
Upload to trusty https://exif.tools/upload.php again, and found an interesting comment. (Also, KISS)

<img width="1072" height="1215" alt="Pasted image 20260125063609" src="https://github.com/user-attachments/assets/270d8073-f600-4024-a181-486db5291bf3" />

Back to CyberChef to translate. 

c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9 from Base64 translates to "steghide:cEF6endvcmQ="

So I was on the right track, just skipped a few steps. Let's just try this as is (just in case).

No dice, but we can take the first translation and plug back into cyberchef - cEF6endvcmQ= from Base64 translates to "pAzzword"

Now we move back over to steghide to decrpyt the file using pAzzword. 

Just like that! The flag file was downloaded and you can view the flag. picoCTF{REDACTED}
