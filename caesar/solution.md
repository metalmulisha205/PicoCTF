# PicoCTF Caesar Challenge Writeup
This challenge provides the following encoded message: 
* picoCTF{gvswwmrkxlivyfmgsrhnrisegl}

## The Caesar Cipher
* A caesar cipher is a message where each character has been shifted in the alphabet a set number of times. <br>For example, abc encrypted with a shift of 3 becomes def. 

## Decoding the Caesar Cipher
* This challenge could be solved by testing every number 1-25 as the shift; however, the following website can be used to automatically perform that operation: <br> https://www.dcode.fr/caesar-cipher <br>

* plugging the message (gvswwmrkxlivyfmgsrhnrisegl) into the decryption field of the website returns the following decoded message: <br> <b>crossingtherubicondjneoach</b> <br>

* Entering our decoded message as <b><u>picoCTF{crossingtherubicondjneoach}</b></u> solves the challenge