Exploit Title: SOPlanning v1.52.00 'xajax_server.php' CSRF (Account Takeover)

Application: SOPlanning

Version: 1.52.00

Date: 4/22/24

Exploit Author: Joseph McPeters (Liquidsky aka fuzzlove)

Vendor Homepage: https://www.soplanning.org/en/

Software Link: https://sourceforge.net/projects/soplanning/

Tested on: Linux

CVE: CVE-2020-9266

Description: SOPlanning v1.52.00 is vulnerable to CSRF via 'xajax_server.php' a remote unautheticated attacker can hijack the admin account. The remote attacker can force the admins browser to make requests by sending them to an external page and update the admins password and email therefore taking over the admin panel.

Instructions: Host the exploit code included and have the admin visit the CSRF exploit page while logged in. It will be noticed that the password and email for the main admin have been changed to the specified email and password.

Liquidsky @ Specialized Security Services Inc. (S3) | Shout out to the team!

_________________________________________________________________________________________

Exploit Title: SOPlanning v1.52.00 'projets.php' (SQLi)

Application: SOPlanning

Version: 1.52.00

Date: 4/22/24

Exploit Author: Joseph McPeters (Liquidsky aka fuzzlove)

Vendor Homepage: https://www.soplanning.org/en/

Software Link: https://sourceforge.net/projects/soplanning/

Tested on: Linux

CVE: CVE-2024-33722

Description: SOPlanning v1.52.00 is vulnerable to Authenticated SQL Injection via the 'projets.php' page.

Instructions: Authenticate to the host, the credentials can be obtained using a CSRF exploit (more info included). Once valid credentials are obtained use either a GET/POST request to send the valid parameters that equal to a valid SQLi.

---------------------------------------------------------------------------------------------

Exploit Title: SOPlanning v1.52.00 'groupe_save.php' XSS (Reflected XSS)

Application: SOPlanning

Version: 1.52.00

Date: 4/22/24

Exploit Author: Joseph McPeters (Liquidsky aka fuzzlove)

Vendor Homepage: https://www.soplanning.org/en/

Software Link: https://sourceforge.net/projects/soplanning/

Tested on: Linux

CVE: CVE-2024-33724

Description: SOPlanning v1.52.00 is vulnerable to XSS via the 'groupe_id' parameters a remote unautheticated attacker can hijack the admin account or other users. The remote attacker can hijack a users session or credentials and perform a takeover of the entire platform.

Example Payload:
"><script>alert('LiQUiDSKY')</script><!--

Reflected XSS Link: /soplanning/www/process/groupe_save.php?saved=1&groupe_id="><script>alert('LiQUiDSKY')</script><!--&nom=Project+New

Analysis: The landing page takes into consideration the user input parameter then redirects to a page where the XSS is shown the payload included in the exploit escapes the variable where it is held and comments out the rest to perform a valid reflected XSS attack against any authenticated user including the admin.
