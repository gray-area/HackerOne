# Micro-CMS v2

The first thing that I noticed is that we do not have the ability to edit or create a new page without a login.

In order to login, I tried a couple of easy username and password combinations, but that did not work, so I moved on. 

The next thing that I checked for was SQL injection. I tested for this with a simple `` ' `` in the username field and a blank password. After hitting enter, I saw that 
there was a SQL error that was displayed. 

Its SQL Injection vulnerable!

Now to figure out, how to use SQL Injection to get inforamtion or bypass the authentication...

In order to do this, I launched SQLMap from my Kali machine

`` sqlmap -u [hackeroneurl] --forms --crawl=2 --tables``

![Alt text](https://github.com/gray-area/HackerOne/blob/main/media/capture.PNG)

In the image above we can see the table named `` admins ``.

In order to enumerate this table, we will need to run the following sqlmap:

`` sqlmap -u [hackeroneurl] --forms --crawl=2 --tables -T admins --dump ``

![Alt text](https://github.com/gray-area/HackerOne/blob/main/media/Capture1.PNG)


