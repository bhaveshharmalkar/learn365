<h3>Day 8 : Solve 3 authentication labs on the portswigger lab </h2>

</br>

#### 1. [Username enumeration via different responses](https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses)
```
> In this lab, the vulnerability is that the application shows exactly what is incorrect, meaning that if the username is 
  incorrect, application will show "Invalid username" or if the password is incorrect, it will show "Incorrect password." 

> Here we can bruteforce the username using the "sniper" attack in Burp Suite, and when we got the valid username, we then
  bruteforced the password using the same method.
```

#### 2. [Username enumeration via subtly different responses](https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-subtly-different-responses)
```
> This lab is an updated but buggy version of the previous lab. In this lab, if we enter an incorrect username or password, 
  then it will show "Invalid username or password."
  
> But when we try to brute-force the username and try to match the response error message, it gives a slightly different error 
  message. i.e., when the username is incorrect, it will show "Invalid username or password." as we previously mentioned, and 
  if the username is correct, then it will show "Invalid username or password" 
  
> We got a username, then simply brute-forced the password for the "302 found" response.  

```


#### 3. [Username enumeration via response timing](https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-response-timing)
```
> In this lab, they implemented one extra level of security. i.e., when we perform the brute-force attack after 5 requests, it 
will block our IP. It can be simply bypassed using the "X-Forwarded-For" request header.

> In the "Intruder" tab of the Burp Suite, set the payload for the request header "X-Forwarded-For: $1$" and set "Numbers" 1-100  
and second payload for username using pitchfork attack method.

> When the attack finishes, at the top of the dialog, add some columns, i.e., Response received and Response completed. Notice 
the one response is significantly longer than others. 

> After that, using that username, brute-force the password.
```
