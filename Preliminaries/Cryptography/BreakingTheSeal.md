# DESCRIPTION

We are provided with a `.pdf` file and is tasked to unlock the password on the `.pdf` file to get the flag.

## MY PROCESS

This was the most funniest challenge I did since it didn't really require complex things (at least for my process). What I did is that, I went to this website `https://www.ilovepdf.com/unlock_pdf` and selected the `.pdf` file given to the challenge. After downloading the decrypted `.pdf` file and opening it, this was the output:

![image](https://github.com/user-attachments/assets/26d43f9f-6f5b-441f-b7d9-b5ef7641b19c)

## ALSO ONE GOOD PROCESS

Hello! Anyways this is also useful as well by using the `john the ripper` tool, specifically `pdf2john`!

All we have to do is to do this command:
`pdf2john <filename.pdf> > hash.txt`

And then using that hash to crack the password by:
`john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt`

Once that is done, you can get the password for the PDF. And opening it will result of getting the flag.

Flag: `TMCTF{C0sm0s}`
