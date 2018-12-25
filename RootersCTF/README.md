# RootersCTF

Challenge : **Old is Gold**

Category :  Crypto

Description : 
 

       Decode this: 444-66-333-666-99-7-777-33-7777-7777-444-666-66  
       Put the flag in RCTF{}
Solution:
This was something that I was familiar with because I've used this type of encryption in my teenage to send messages to my Ex (LOL) 
This is like the keypad of an old mobile phone like the Nokia 3310 where 444 means I as we press the 4th key 3 times to get the letter I as in this picture


![enter image description here](https://www.dcode.fr/tools/phone-keypad/images/keypad.png)


After Decoding the message we get the string "**INFOXPRESSION**"

Flag: **RCTF{INFOXPRESSION}**

Challenge : **Francis Secret**

Category :  Crypto

Cipher Text : 

    AAAABAAAAAAAABAABBABABBAAAAABAABAAAABBBAAABBBAABAABAAAAABAAABAAABAABBABAAAAAABAAAAAAABAABA
    Put the flag in RCTF{}
 Solution:
Searching through Google we found that it is **Baconian Cipher**
![BACONCIPHERISGREAT](https://i.imgur.com/CaVEGuK.png)
Flag: **RCTF{BACONCIPHERISGREAT}**

Challenge:**Automate or Die!**

Category :  Crypto

Cipher Text : [HERE](http://rootersctf.in/files/26e32edd4675187ecdb8a0780d86bb76/automate_or_die.txt)

Solution:
This is just base64 encoded multiple times so writing a small python script will do the job

    import base64
    encoded = 'ciphertext_here'
    data = base64.b64decode(encoded)
    print data
    while True:
    	data = base64.b64decode(data)
    	print data
Flag:**RCTF{b@se64_1s_c00l}**




