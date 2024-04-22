Exploit Title: SOPlanning v1.52.00 'xajax_server.php' CSRF (Account Takeover)
Application: SOPlanning
Version: 1.52.00
Date: 4/22/24
Exploit Author: Joseph McPeters (Liquidsky aka fuzzlove)
Vendor Homepage: https://www.soplanning.org/en/
Software Link: https://sourceforge.net/projects/soplanning/
Tested on: Linux
CVE: Not yet assigned

Description: SOPlanning v1.52.00 is vulnerable to CSRF via 'xajax_server.php' a remote unautheticated attacker can hijack the admin account. The remote attacker can force the admins browser to make requests by sending them to an external page and update the admins password and email therefore taking over the admin panel.

Instructions: Host the exploit code included and have the admin visit the CSRF exploit page while logged in. It will be noticed that the password and email for the main admin have been changed to the specified email and password.

Liquidsky @ Specialized Security Services Inc. (S3) | Shout out to the team!
