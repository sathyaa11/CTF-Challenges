# My First SQL

For this challenge, the login page required an email and password, but no credentials were provided.
I first tried using a common default login like admin@gmail.com : admin, but it failed.

<img width="877" height="528" alt="Screenshot 2026-05-30 235815" src="https://github.com/user-attachments/assets/23d8c18e-048e-4b67-a9e6-7a384475b6eb" />

Next, I tested for SQL injection by submitting just a single quote (') in the email field, which resulted in a "Page Not Found" error. Then, I tried two single quotes (''), and the page loaded but returned "invalid credentials"

<img width="827" height="416" alt="Screenshot 2026-05-30 235815" src="https://github.com/user-attachments/assets/f88309f8-f53f-44a6-9ab1-e93c2b52ec87" />

<img width="662" height="387" alt="image" src="https://github.com/user-attachments/assets/841f1525-29bf-4349-9f2e-30da8b89d4a9" />

This suggested that the input was being processed by an SQL query and that SQL injection might be possible.This behavior hinted at a query structure like:

SELECT * FROM users WHERE email = ''';  → caused the page to break.

SELECT * FROM users WHERE email = ''''; → page loaded, but login failed.


Based on this, I attempted a classic SQL injection payload:
' OR 1=1 #
along with any random password.

This bypassed the authentication and successfully logged me into the admin panel, where I found the flag.

<img width="931" height="433" alt="Screenshot 2026-05-30 235815" src="https://github.com/user-attachments/assets/3afadab1-96a0-4996-a908-a3978ab406a8" />

