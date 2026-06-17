# Dot-Dot-Slash

In this challenge , I tried clicking through the available features on the site, but most of them were either broken or non-functional.Then I download dotdotslash file and review in that folder. 
In that folder,  I found a setup.sh file and it created a flag.txt file, but the file was empty.

<img width="657" height="270" alt="image" src="https://github.com/user-attachments/assets/fcb8b99c-ecd4-4966-9f45-b68861efae2f" />

Then  I tested adding /assets to the site’s URL  but it shows some information in that error. . In the error , I notice  ‘/assets/assets’ which means current  path is  assets and I know that can do  directory traversal in assets path can tamper.
Firstly , I add ../ but  this redirected me back to the main page with an error. Then I try again by add / flag.txt but there no flag showing there.

<img width="677" height="422" alt="image" src="https://github.com/user-attachments/assets/c3946e71-8b2e-4dd5-9a43-416b93e2788d" />

Next, I tried attempted encoding the / character as %2f to bypass basic input sanitization.This time it not showing an error and shows /../  which indicated that directory traversal was working.

<img width="652" height="165" alt="image" src="https://github.com/user-attachments/assets/c1166956-0826-4a2c-8eba-dde363588ee7" />

Lastly , I tested the final payload: ..%2Fflag.txt in  the url and displayed the flag in the browser

<img width="726" height="137" alt="image" src="https://github.com/user-attachments/assets/c741daaa-be84-4358-9fe6-69829404aa29" />


