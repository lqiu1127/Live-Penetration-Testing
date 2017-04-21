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

<img src='http://i.imgur.com/jdcFb2V.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

Vulnerability #2: Session Hijacking/Fixation

Can use the same session ID in red to get into blue, does not refresh its own session ID regularly and does not check for session ID validaty. 

<img src='http://i.imgur.com/9EQMDEw.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />


## Green

Vulnerability #1: Username Enumeration

The programmer bolded the login unsucessful for logins that have the correct username. 
when user doesnt exist, the login unsucessful is in <span class= "failed">. However when the user does exist it is replaced with a <span class= "failure">

<img src='http://i.imgur.com/l6rJR4i.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

Vulnerability #2: Cross-Site Scripting (XSS)

The feedback is not properly protected against XSS, so scripts can easily be injected for admins to see.

<img src='http://i.imgur.com/CUJxBuM.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

/red/public/salesperson.php?id=10 and /red/public/salesperson.php?id=11 are accessible by public through URL manipulation

<img src='http://i.imgur.com/MkZKIRs.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

Vulnerability #2: Cross-Site Request Forgery

User can edit sales person information without a valid CSRF token, which is a big problem. Other site has a safety CSRF token check that this website does not have.

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2017] [Tianhao Qiu]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

