# PicoCTF WebNet0 Challenge Writeup
## Introduction
This challenge provides a packet capture and a key and challenges the user to find the flag using these two files. The key contains an RSA private key and the packet capture can be viewed using a tool called wireshark: https://www.wireshark.org/
## Using the RSA Key
The first place to begin is figuring out what the RSA key can be used for in wireshark. A simple web search reveals the following website: https://wiki.wireshark.org/TLS. According to the wireshark wiki, it is possbible to use an RSA key for TLS Decryption. As the wiki instructs, entering the key in <i>Edit-> Preferences-> Protocols->TLS</i> allows for the decryption of the TLS stream. After entering the key in the "(Pre)-Master-Secret log filename" field, HTTP packets are visibile in the capture.
## Retrieving the Flag
Now that HTTP packets are visible in the packet capture, following the HTTP steram reveals the flag as <b>picoCTF{nongshim.shrimp.crackers}</b> <br>
<img src="httpstream.png"/>