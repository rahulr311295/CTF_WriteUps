
# RootersCTF



|TEAM : V3N0M| Score :385 |
|-------------|--|
|      Position :       |12  |


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


Challenge :**Indecipherable**

Category :  Crypto

File : [HERE](http://rootersctf.in/files/057c225412a9e78c87f4299f378fea8e/cipher_text.zip)

Solution : After downloading the password protected zip file and cracking the password with fcrackzip we got the password as fsociety

![password](https://i.imgur.com/6nIQBdq.png)

Cipher Text:`zpwj{ym_apzv_io_l_oqajhqu_dm_fllmdlqg}`
The encryption was some sort of Substitution Cipher and finally we fixed on **Vigenere Cipher** but we need a key trying the zip password gave us the wrong result then my team mate found the key "*Sometimes what we are looking for is right in front of us.*" as the challenge description says it was **Indecipherable**

Flag : **rctf{we_live_in_a_kingdom_of_bullshit}**


Challenge : **Tap-tap-tap**

Category : Reverse

File : [HERE](https://drive.google.com/file/d/13ZLVtVakm6NKR5MXhliqu59nzY_3jYZY/view?usp=sharing)


Solution:
The drive link downloads an apk file after decompiling it with apktool and using the grep command to search the flag reveals the hidden flag in the MainActivity.smali

Flag:`RCTF{andr01d_1s_all_ab0ut_$weet$}`


Challenge:**Admin, who me??**

Category: PWN

The Challenge is currently not available so wont be able to submit the flag .

File : [HERE](http://rootersctf.in/files/d35eb83dcbf4a7b4b2d879df60746fd5/admin)

Solution:
When we run the executable it asks for a username and password upon submitting the correct username and password it gives us the flag 

![enter image description here](https://i.imgur.com/b1osj7s.png)

I tried 250 A's as the username just as a wild guess to see if there is a BOF and BOOM (Lucky Me)

![enter image description here](https://i.imgur.com/OjzL1gl.png)

The following is not the flag I made that up


Challenge:**Prisoners of the Sun**

Category: PWN

Solution : We have a netcat connection and when connecting  we have a python console something like this
![enter image description here](https://i.imgur.com/RiYW0Pl.png)

A python console sounds good but entering any thing closes the connection after sometime I tried this 

    exec('print(flag)')
and I got the flag

Challenge: **50 Shades of Stegano**

Category: Stegano

File: [HERE](http://rootersctf.in/files/664735619596fbbb0da3b8a440ce4a78/hidden.png)

Solution : As the name says 50 shades which can only mean one thing stegsolve

![enter image description here](https://i.imgur.com/f0RiBvV.png)

Flag : **RCTF{COLORBL1ND}**

Challenge:**M4SS4CR3**

Category:Stegano

File:[HERE](http://rootersctf.in/files/922faa7e0f727e833ba3b7df7b9506ad/image.png)

Solution: 

> First of all I have to admit the fact that this is one fucked up
> challenge that only 14 teams solved it

Alright running strings on the image gives a url.txt file by extracting it with binwalk I had this https://www.mobilefish.com/services/steganography/steganography.php 
What was the next step the URL was an online steg solver but it required a password we tried everything nothing gets even close after a while I got a hint to check on reddit so I googled "*Elliot's Password*" as the challenge description had a reference to Elliot.
Which led to this reddit post https://www.reddit.com/r/MrRobot/comments/7cvui5/elliot_password/ and the last comment is **M4ss4cr30fth3b0urg3o1s1e** which is the password upon decoding the message with the stegsolve url we got the flag.

Flag:**RCTF{wubba_lubba_dub_dub}**
![enter image description here](https://nomansskymods.com/wp-content/uploads/cmdm/162825/1471369626_960.jpg)

Challenge:**Easy One**

Category: Web

Description: Have you read the [rules](https://www.rootersctf.in/rules) carefully?

Solution : Visiting the rules page and viewing the source code gives out the flag 

Flag:**RCTF{an_3asy_0n3}**

Challenge:**Paste in RecycleBin**

Category: Misc

Description:I found this is in recycle bin. Can you help me?  
**"YkmwWUSS"**

Solution : The first thing that came to my mind was pastebin and it was correct https://pastebin.com/YkmwWUSS

Flag:**RCTF{Th1S_1S_Strang3}**

Challenge:**Is This Is a Spam**

Category: Misc

File: [HERE](http://rootersctf.in/files/43ce03b08e4dca6c7ea3bad95e34dc4a/is_this_is_a_spam.txt)

Solution : I didn't knew much about this challenge or the string but after googling a bit I found a site that can decode such spam text http://www.spammimic.com/decode.cgi

Flag : **RCTF{This_is_4_S3cr3t}**

Challenge:**Save Me**

Category: Misc

Description:

    `Harry enters in a real game just like Jumanji and lands in the **city 2**. 
    His task is to save the Jumanji from Van Pelt terror in order to do this he has to open a magical box which is in the **city 67** and there
    is only one path and hence one flag. Help him find the path and you will have your precious flag.
    
    `Put the flag in RCTF{}``
Solution : This was nuts  So I had to seek help to a friend of mine who is good in these kinds of stuff after a while he said this is a path finding problem where 2 is the starting position with the character e and the next position as 73 by traversing through the path we can get the flag I still dont know how he did that

Flag : **RCTF{e*#JoyfY6%rU}**

