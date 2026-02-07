Alright, so this endpoint is going to expose a file containing a flag. It's a simple blog site, but it also has an article about API docs. 

So we can browse the site as normal, but I really want to see what the API documentation is going to show us. We can browse there using one of the posts on the landing page. 

<img width="1280" height="1142" alt="Pasted image 20260207022426" src="https://github.com/user-attachments/assets/7b214a40-daa2-4af3-b941-c394e5ab5683" />

So! We now have some options to explore this with. You can go the route of using Bruno or Postman to send API get or post requests to determine the responses from the site.

But, one of these APIs is not like the other.

I highly suggest you check out Micah's talk at Defcon33 if you haven't already. SignalGate!

https://youtu.be/5VlhsT5Kbsk?si=OeuY7ivNXeXMFRDT

It's a really interesting one concerning a deprecated offshoot of a signal messaging server and how he was able to dump these messages. It led to several law enforcement agencies and government messages to be leaked. 

We don't *really* need either Postman or Bruno to modify the url and download the dump file though.

Once you find the file, use cat and pipe to grep to find the flag within the dump. 

> cat file | grep 'picoCTF{'

And that's it! These types of files should not be accessible without proper authentication and authorization. picoCTF{REDACTED}
