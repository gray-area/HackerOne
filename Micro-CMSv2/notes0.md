## Flag 0

## Authentication Bypass

For my method, you will need 2 tools. Both of these tools come pre-installed on Kali, so if you are not using Kali, you will need to install them first.

* BurpSuite
* BurpSuite Proxy for you web browser

BurpSuite will be used to create the SQL Injection payload. 

First, open up the web browser to the login page.

![Alt Text]()

Second, make sure that your proxy is configured in your web browser to point to BurpSuite.

![Alt Text]()

Third, open BurpSuite and make sure that intercept is on.

![Alt Text]()

Now we are ready to bypass authentication!

In the username field, type ``user`` and click the login button.

![Alt Text]()

Now switch over to BurpSuite, where we can see the request. 

![Alt Text]()

Notice at the bottom where it says username and password. This is where we will send our payload.

![Alt Text]()

Enter the payload as shown below.

``username=user' UNION SELECT "pass" as password FROM admins WHERE '1'='1&password=pass``

What this statement is doing is creating a self cheking statement that returns as true. 
