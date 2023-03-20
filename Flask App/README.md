# Flask App

This is a simple web application that asks for login credientials. 

![login](./Screenshot_1.png "login").


In the web app following are common places to look.

/robots.txt <br>
/sitemap.xml<br>
/crossdomain.xml<br>
/clientaccesspolicy.xml<br>
/.well-known/<br>
/.github/<br>

## Looking at Robots.txt
Looking at robots.txt we see the message directory.

![robots](./Screenshot_2.png "robots").

## Looking at /message
At message we see it says we need to put a messageid parameter.
![message](./Screenshot_3.png "message").

## Putting the parameter
After putting the parameter we get a link to a github repo where we know that the mail credientials are used for login from the message.
![message](./Screenshot_4.png "message").

## Finding creds
I have used simple search query to find the creds.
![creds](./Screenshot_5.png "creds").

Scrolling down a bit we can found the creds.
![creds](./Screenshot_6.png "creds").

## Logging in
Now by using these creds we can login into the app
![login](./Screenshot_7.png "login").

## After logging in
After loggin in we can see the following screen.
![secret](./Screenshot_8.png "secret").

## Looking at the cookies
We know that it is a flask app. if you google a bit you would come to know that the first part is base64 and contains the payload while the other part is of secret that is used to sign this cookie.

![secret](./Screenshot_10.png "secret").

## Looking at payload of cookie
At cyber chef if we do base64 decode we can see the user as john.

![payload](./Screenshot_11.png "payload").

## How to get secret
If you google about the hacking of flask cookie there are many tools & tricks. However, am gonna openup first link in my results.

![get secret](./Screenshot_12.png "get secret").

## Selecting tool
At that link i found a flask-unsign tool that could be used to find the secret from the given cookie. 
![tool](./Screenshot_13.png "tool").

## Found the Secret
Now using that tool I have found the secret.
![found_Secret](./Screenshot_14.png "found_Secret").

## Getting flag
Now after inputting that secret we can get the flag.
![found_Secret](./Screenshot_15.png "found_Secret").