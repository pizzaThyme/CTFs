So we start this off with a .pcap and determine how an intruder infiltrated the system.

There's also a clue about "time" in the description, so keep that in mind.

The first thing I notice when I'm looking through Wireshark is the payload info. Some of the packets have base64 encoded in the payload of the packets. 

We can also see that a lot of these packets are 48 frames in length. Looking through these doesn't provide much useful information. Let's filter those out. 

> !(frame.len == 48)

Now we should be seeing 7 packets that are different lengths than normal with base64 tcp.payloads.

<img width="1219" height="465" alt="Pasted image 20260213042732" src="https://github.com/user-attachments/assets/5bb55a59-3905-4d9e-8048-9f845891916d" />

I was able to export the data from Wireshark, and you can do this and grep through the output, but I wasn't able to export JUST the payload for these packets.

I used tshark to export just what we need for the task:

> tshark -r "myNetworkTraffic.pcap" -Y "!(frame.len == 48)" -T fields -e tcp.payload  -E occurrence=first > output.txt

Now that we've got the payload, we can head over to CyberChef decode the data.

<img width="992" height="474" alt="Pasted image 20260213041546" src="https://github.com/user-attachments/assets/55faf82b-1d13-449b-b527-ebadcd7e64e3" />

Now that you have the base64, you can decode this into the flag. I found it easier to decode each line separately from https://www.base64decode.org/.

<img width="807" height="556" alt="Pasted image 20260213042428" src="https://github.com/user-attachments/assets/1b0bfc44-3b50-41ed-9f19-af16b35695e5" />

At this point, just take the data and unscramble it to create the flag! picoCTF{REDACTED}
