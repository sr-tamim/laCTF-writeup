# terms-and-conditions
108 points

## Description
Welcome to LA CTF 2024! All you have to do is accept the terms and conditions and you get a flag!

terms-and-conditions.chall.lac.tf

## Solution
1. I opened the link and it showed me a simple html page with a button to accept the terms and conditions.
2. I tried to click the button but it starts moving away from the cursor.
3. So, I opened the developer tools and the body changes and it shows "NO CONSOLE ALLOWED"
4. I started reading the source code and tried to understand how it was detecting the console opening and how it was moving the button away from the cursor.
5. Actually it was saving the innerWidth and innerHeight of the window after page load and then it was checking if the window was resized or not. If the window was resized then it shows that "NO CONSOLE ALLOWED" message.
6. I just kept the console opened and reloaded the page and it couldn't detect the console.
7. Then I simply look for the "I Accept" button in source code and got it's ID.
8. I just wrote `document.getElementById` to get the button and then clicked it.
9. It showed me the flag.