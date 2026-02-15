We connect to the server and find a folder, a decryption script, and a checksum hash of a flag.

Looking into the 'files' folder, we can see that there are 100+ files, so manual checks aren't an option.

<img width="632" height="569" alt="Pasted image 20260214063034" src="https://github.com/user-attachments/assets/01c7c3d0-1161-48ed-b4d4-7163ca05f284" />

From taking GSOC, I know we can use '*sum' to pull a hash for a file (md5sum, sha256sum, sha512sum, etc.)

I attempt to write a quick bash script on the server to grab the hashes:

>for $file in files;
>
>    do sha256sum $file;
>
>done

I know that it has the potential to work, but I was unable to make this work remotely over SSH.

Let's try a more direct approach. 

> cd files
> 
> sha256sum *

<img width="606" height="419" alt="Pasted image 20260214063421" src="https://github.com/user-attachments/assets/1e5bb0d2-ab63-4704-bdca-c12fa54c5c7a" />

We can run sha256sum on each file and send to a text file for easier searching.

> sha256sum * > grepme.txt

Once that's sent, just use grep to find the file and use the script to check the checksum for the flag.

<img width="635" height="181" alt="Pasted image 20260214063708" src="https://github.com/user-attachments/assets/a33df2dc-4cc6-4fc3-b5a8-2075afd4b536" />

Another day, another flag. picoCTF{REDACTED}
