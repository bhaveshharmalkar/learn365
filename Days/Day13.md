<h2> Solve 4 access control labs on the portswigger lab and read blogs </h2>

</br>

### 1. Access Control Labs

#### [<ul><li>Unprotected admin functionality</li></ul>](https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality)
```
-> In this lab admin panel is in unprotected path i.e, /robots.txt. After navigating to /robots.txt we saw the admin panel 
   directory.
```

#### [<ul><li>Unprotected admin functionality with unpredictable URL</li></ul>](https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality-with-unpredictable-url)
```
-> In this lab admin panel URL are disclosed in the source code. After ctrl+u we saw that URL in the javascript function.
```

#### [<ul><li>User role controlled by request parameter</li></ul>](https://portswigger.net/web-security/access-control/lab-user-role-controlled-by-request-parameter)
```
-> In this lab user role are controlled by the request parameter i.e, When we try to access the /admin panel we saw that request
   parameter 'Admin=false' when we 'Admin=true' then we can access the /admin panel.
```

#### [<ul><li>User role can be modified in user profile</li></ul>](https://portswigger.net/web-security/access-control/lab-user-role-can-be-modified-in-user-profile)
```
-> In this lab, when users login with their credentials, there is a 'change-email' functionality. When we enter some value in it 
   and send this request to the burp repeater, then we see the '200 OK' response with 'roleid=1'. Then we can simply add 'roleid=2'
   in the '/change-email' request.     
```

### 2. Read Blog

#### [<ul><li>Bypassing authorization in Google Cloud Workstations</li></ul>](https://blog.stazot.com/auth-bypass-in-google-cloud-workstations/)
