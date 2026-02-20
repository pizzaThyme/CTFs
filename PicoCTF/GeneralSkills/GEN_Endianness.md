The description for this challenge asks, "Know of little and big endian?"

Little Endian and Big Endian are a bit new to me, so I had to do a little research prior to undergoing this challenge. 

<img width="694" height="592" alt="Pasted image 20260219052959" src="https://github.com/user-attachments/assets/9ce6dabc-3f41-4aa6-b968-71d21f6a331c" />

So basically, BE stores the Most Significant Byte (MSB) at the smallest address, and LE stores the Least Significant Byte at the smallest address. 

Big Endian is how we natrually read data and text (from left to right) and Little Endian would just be the reverse of that (right to left). 

I'm going to be so totally honest, I was pretty confused about what was being asked by this challenge. 

I did use https://www.freecodecamp.org/news/ascii-table-hex-to-ascii-value-character-code-chart-2/ to help find the hex of these letters pretty quickly. This chart is a nice tool. 

<img width="850" height="449" alt="Pasted image 20260219053230" src="https://github.com/user-attachments/assets/f42c1478-9969-4674-9ccf-15ec1249d044" />

My understanding of MSB and LSB was where the letters were sitting in the alphabet, so I was trying the hex version of "ciluy" as that is how the letters are arranged alphabetically. 

I also tried it backwards, prefexing the hex values with "0x", and adding spaces. No luck. 

After trying this a few times, I took a hint, and realized we just needed to find the hex value of the literal word and reverse the hex values for LE. 

<img width="618" height="184" alt="Pasted image 20260219053257" src="https://github.com/user-attachments/assets/aee4f685-5dd8-4eab-9dd5-94f2b6a6111c" />

Once we submit the correct reverse of the hex values for LE, we just need to take the base hex value of what is shown for BE. 

Once I was finished with this challenge, I realized that you can also use CyberChef to help you find the hex values. This is a much more simple and fast solution!

Perseverance is key to CTFs, and we made it! picoCTF{REDACTED}
