## Flag 0

## Authentication Bypass

In order to do this, I used BurpSuite to create the payload. 

First, open up the web browser to the login page.

Second, make sure that your proxy is configured in your web browser to point to BurpSuite.

Third, open BurpSuite and make sure that intercept is on.

Now we are ready to bypass authentication!

In the username field, type ``user`` and click the login button.

Now switch over to BurpSuite, where we can see the request. 

Notice at the bottom where it says username and password. This is where we will send our payload.

``username=user' UNION SELECT "pass" as password FROM admins WHERE '1'='1&password=pass``
