<h2>Day 1 : Recon00 - Recon03 exercise on Pentester Lab </h2> 

</br>

#### 1. Check for "/robots.txt" file 
```
The robots.txt file is used to tell web spiders how to crawl a website. To avoid having confidential information indexed and
searchable, webmasters often use this file to tell spiders to avoid specific pages. This is done using the keyword Disallow. 
```

#### 2. Generate a "404 Not Found" error page.
```
Not Found/404 pages can leak information about the web stack used by a company or application. It also allows you to detect 
files that exists when you start bruteforcing directory.
```

#### 3. Examine the "/security.txt" file under the "/.well-known/security.txt" folder, or simply navigate to "/security.txt". 
``` 
The security.txt file is used to tell security researchers how they can disclose vulnerabilities for a website.
```

#### 4. Read the source code of a website to find hidden directory or sensitive information. 
