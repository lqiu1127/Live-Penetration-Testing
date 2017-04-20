# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection (SQLi)

You can inject the userid lookup (not escaped) with https://35.184.84.47/blue/public/salesperson.php?id=' OR SLEEP(5)=0--'

Vulnerability #2: Session Hijacking/Fixation

Can use the same session ID in red to get into blue.


## Green

Vulnerability #1: Username Enumeration

The programmer bolded the login unsucessful for logins that have the correct username. 
when user doesnt exist, the login unsucessful is in <span class= "failed">. However when the user does exist it is replaced with a <span class= "failure">


Vulnerability #2: Cross-Site Scripting (XSS)


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

/red/public/salesperson.php?id=10 and /red/public/salesperson.php?id=11 are accessible by public through URL manipulation

Vulnerability #2: Cross-Site Request Forgery


## Notes

Describe any challenges encountered while doing the work

