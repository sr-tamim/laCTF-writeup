# terms-and-conditions
108 points

## Description
Welcome to LA CTF 2024! All you have to do is accept the terms and conditions and you get a flag!

terms-and-conditions.chall.lac.tf

## Solution
1. I opened the link and it showed me a simple html page with a button to accept the terms and conditions.
   ![image](https://github.com/sr-tamim/laCTF-writeup/assets/86656406/6fea3c44-dc58-4b24-8445-045bd85a846f)

2. I tried to click the button but it starts moving away from the cursor.
   ![image](https://github.com/sr-tamim/laCTF-writeup/assets/86656406/d5170c19-c674-43dd-996d-651a3f7ac0c6)

3. So, I opened the developer tools and the body changes and it shows "NO CONSOLE ALLOWED"
   ![image](https://github.com/sr-tamim/laCTF-writeup/assets/86656406/e4f6b476-328a-45cc-b36b-d602ea665187)
4. I started reading the source code and tried to understand how it was detecting the console opening and how it was moving the button away from the cursor.

5. Actually it was saving the innerWidth and innerHeight of the window after page load and then it was checking if the window was resized or not. If the window was resized then it shows that "NO CONSOLE ALLOWED" message.
   ![image](https://github.com/sr-tamim/laCTF-writeup/assets/86656406/af6c5d6a-c71e-4ff9-a00b-c05ab8bc7c4c)

6. I just kept the console opened and reloaded the page and it couldn't detect the console.
7. Then I simply look for the "I Accept" button in source code and got it's ID.
8. I just wrote `document.getElementById` to get the button and then clicked it.
   ![image](https://github.com/sr-tamim/laCTF-writeup/assets/86656406/a3f6c47d-1f3f-4399-9587-c9721ae7f8f2)

9. It showed me the flag.
   ![image](https://github.com/sr-tamim/laCTF-writeup/assets/86656406/8028223e-dac6-4e42-9bc3-6a4e324f97fd)
