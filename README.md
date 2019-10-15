# BMC Patrol agent privilege escalation

These are Proof-Of-Concepts of two "setuid" vulnerabilities related to the BMC Patrol Agent software that allow to elevate privileges from an arbitrary linux user to root.

- CVE-2019-17043 : privilege escalation through "setuid" file allowing to elevate privileges from any linux user to "patrol" user
- CVE-2019-17044 : privilege escalation through "setuid" file allowing to elevate privileges from "patrol" user to "root" user

Chaining the two vulnerabilities allows to obtain "root" privileges from any other user on the system. 

## Affected versions

PatrolAgent V9.0.10i 

(vulnerability was tested on PatrolAgent V9.0.10i but other versions may be vulnerable as well)  
(according to BMC the CVE-2019-17043 allowing to get "patrol" privileges from normal user does not affect recent versions of Patrol Agent)  

## Disclosure timeline

2019-07-03 - Vulnerability discovered  
2019-07-07 - Vendor contacted  
2019-07-08 - Vendor responded and initial dialog and vulnerability reviewing process is started  
2019-09-14 - Vulnerability disclosed  

## Acknowledgment

The vulnerability was discovered by Jan Kopec (https://twitter.com/blogresponder) and Charles d'Hondt (https://twitter.com/whira_wr) both working at LEXFO.

## Reference

https://docs.bmc.com/docs/PATROLAgent/11302/notification-of-action-required-by-patrol-agent-users-to-apply-the-security-patch-898411558.html  
