# DOT DOT SLASH 2

In this challenge , I  download dotdotslash file and review in that folder. In that folder,  I found a setup.sh file and it created a flag.txt file, but the file was empty.
<img width="660" height="271" alt="image" src="https://github.com/user-attachments/assets/469701f0-d5a0-4f94-a7ed-9f6b4151d06b" />


Then  I tested adding ….to the site’s URL  but it shows some information in that error. . In the error , I notice  ‘/assets/….’ which means current  path is  assets and I know that can do  directory traversal in assets path can tamper.
When I add ../ but  this redirected me back to the main page with an error.Then I try again by add ../ flag.txt with encode url  but still it go to main page.
<img width="472" height="296" alt="image" src="https://github.com/user-attachments/assets/dd020bcd-4242-4869-92ef-7c13e37b80df" />


Then try …./…/flag.txt it rejected , then remove / , it works , then I realize it block ../ .Then, I try encode /  to %252 it works like / flag.txt 
<img width="800" height="32" alt="image" src="https://github.com/user-attachments/assets/12535211-acbf-4154-94fc-5d797738023a" />

Lastly , I tested the final payload: …./%252fflag.txt in  the url and displayed the flag in the browser

<img width="867" height="117" alt="image" src="https://github.com/user-attachments/assets/28d48360-1c3c-4edb-8130-48cd5648922c" />
