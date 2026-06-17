# Admin Dashboard 2
I started by registering a new user account through the provided registration form. After successfully registering, I logged into the application.Once logged in,
I explored the application to understand its features.I tested the note submission feature by creating a new note but but it did not reveal any vulnerabilities .

<img width="437" height="326" alt="image" src="https://github.com/user-attachments/assets/5e436aa2-6754-43a2-af67-5082ed72a1aa" />

I viewed the page source of the main page and found a reference to a file called: impersonate.php which it might be part of admin functionality.  
I knew that Impersonate can allow one user to impersonate another.

<img width="890" height="175" alt="image" src="https://github.com/user-attachments/assets/e731d32a-04de-4736-b736-c676d9303949" />

Then, I select impersonate for admin role.  It also changed the role successfully in dashboard.
<img width="887" height="40" alt="image" src="https://github.com/user-attachments/assets/06397901-c4b8-4b45-98d0-33b3af7833e7" />

Finally ,   the flag was displayed in note section.
<img width="922" height="280" alt="image" src="https://github.com/user-attachments/assets/ead20f4e-0174-49ca-b14e-e187de569b42" />
