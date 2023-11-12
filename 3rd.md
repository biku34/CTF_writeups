![image](https://github.com/biku34/CTF_writeups/assets/117967710/92896073-6078-4a73-857b-4c47c43989fd)

This challenge had an archive folder which on opening had the file 

![image](https://github.com/biku34/CTF_writeups/assets/117967710/91ae87ea-da0f-4f4e-ad7f-32e671e95f5a)

It was a steganography problem so I looked at the hex dump and found 

![image](https://github.com/biku34/CTF_writeups/assets/117967710/e8ccf455-37b1-40ce-acac-b576521972ad)

So I did use the dd command 
dd if=5411333e505440020a1799da6071851b.gif bs=1 skip=78000 of=flag.rar
where "5411333e505440020a1799da6071851b.gif" is the input file and "flag.rar" is the output file , we are skipping "131e0" or "78176" bytes 
and we get "flag.rar" folder which had the image

 ![image](https://github.com/biku34/CTF_writeups/assets/117967710/75a07425-9e4b-4e1c-b2f4-a392d6ec3c99)

