# Forgot Password 2

In this challenge, it required to find user’s  username and password to login .Then , I began to view source code , it  shows“static/login.js" which  simple js login to validate a static username/password.

<img width="777" height="230" alt="Screenshot 2026-06-07 165041" src="https://github.com/user-attachments/assets/7f5f126c-e1e6-437f-bfa9-86afd307dbae" />

I logged in using a username and an MD5-hashed password, but it said "wrong credentials" when I tried to log in. Then, I visited the hint page, which mentioned password hashing. 
I realized that I needed to decode the MD5 hash to get the actual password.

<img width="858" height="226" alt="Screenshot 2026-06-07 165041" src="https://github.com/user-attachments/assets/f0e7a6a4-2198-45a3-8bd2-fbb8ab70cd0f" />

Then , I try decode the md5 value in https://www.dcode.fr/md5-hash and it also show covert to plain-text value which is user’s password.

<img width="927" height="270" alt="Screenshot 2026-06-07 165041" src="https://github.com/user-attachments/assets/98e400a9-c621-4394-80ea-6e541db82c7c" />

Finally ,  The login was successful, and the page displayed the flag.

<img width="968" height="181" alt="image" src="https://github.com/user-attachments/assets/0b1c313c-e0e9-4e9f-b394-cddf9e1c027d" />

