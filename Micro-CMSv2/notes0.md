## Flag 0 - Authentication Bypass

For my method, you will need 2 tools. Both of these tools come pre-installed on Kali, so if you are not using Kali, you will need to install them first before you
proceed. BurpSuite will be used to create the SQL Injection payload, so you will need both of these tools.

* BurpSuite
* BurpSuite Proxy for your web browser

## Getting Ready

First, open up the web browser to the login page.

![Alt Text]()

Second, make sure that your proxy is configured in your web browser to point to BurpSuite.

![Alt Text]()

Third, open BurpSuite and make sure that intercept is on.

![Alt Text]()


## Bypass Authentication!

In the username field, type ``user`` and click the login button.

![Alt Text]()

Now switch over to BurpSuite, where we can see the request. 

![Alt Text]()

Notice at the bottom where it says username and password. This is where we will send our payload.

![Alt Text]()

Enter the payload as shown below.

``username=user' UNION SELECT "pass" as password FROM admins WHERE '1'='1&password=pass``

![Alt Text]()

What this statement is doing is creating a self cheking statement that returns as true. 
