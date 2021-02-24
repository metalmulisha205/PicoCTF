# PicoCTF Client-side-again Challenge Writeup
## Introduction
This challenge provides a link to the login page of a website and challenges the user to break into the website. The hint is "what is obfuscation?" Research on the topic of ofuscation uncovered that obfuscation is intended to make code difficult to read while preserving its function (https://www.preemptive.com/obfuscation#:~:text=Code%20Obfuscation%20is%20the%20process,the%20output%20of%20the%20program.)
## Inspect Element
Upon further inspection of the website using Google Chrome's developer tools an obstrucified script can be found that appears to validate the input for the login: <br>
<img src="obfuscated.png" /> <br>
## Deobstrucification
The following website can be used to deobstrucify the script: https://lelinhtinh.github.io/de4js/
<br> <img src="deobfuscated.png" /> <br>
## Decoding the Flag
The script appears to be checking substrings of the input to determine if they match specified strings. It is important to note that the numbers of the function are in hexadecimal and the function defines a valiable split = 0x4 that it uses to multiply other numbers in several of the if statements. Reconstruction of the string is possible by looking at the if statements to determine where each individual substring belongs: 
* (0 - 8) = picoCTF{
* (7 - 9) = {n
* (8 - 16) = not_this
* (3 - 6) = oCT
* (24 - 32) = f49bf
* (6 - 11) = F{not
* (16 - 24) = _again_e
* (12 - 16) = this

Reconstructing the password based on the substrings above yields the flag: <b>picoCTF{not_this_again_ef49bf}</b>

