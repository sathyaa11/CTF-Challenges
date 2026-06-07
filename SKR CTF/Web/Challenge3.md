# My First XSS

The challenge page displays a comment section where users can view comments and replies posted by others.

<img width="712" height="356" alt="Screenshot 2026-05-30 235815" src="https://github.com/user-attachments/assets/e9563a8c-d64d-4c62-8412-bd04053a0954" />

Then , I submitted a simple message: “Hi”, it  normally stored  comments section.,I then tested with special HTML characters such as:  <> " ' / \
These were also stored and rendered on the page . Then , I intercept the request and modified the message parameter with the following XSS payload:
<script>alert(“xss”)</script>

<img width="746" height="288" alt="Screenshot 2026-05-30 235815" src="https://github.com/user-attachments/assets/4b5507e3-8e6f-450c-83b5-555f140bd433" />

After forwarding the request, I revisited the page and confirmed that the script executed in the browser.

<img width="772" height="392" alt="Screenshot 2026-05-30 235815" src="https://github.com/user-attachments/assets/4a9c1020-308d-401b-911c-c53762ddeaf9" />
