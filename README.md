SOPlanning v1.52.00 Admin 'xajax_server.php' CSRF (Account Takeover)

Features: Changes the admin password and email to your set desired choice.

Description: SOPlanning v1.52.00 is vulnerable to CSRF via 'xajax_server.php' a remote unautheticated attacker can hijack the admin account. The remote attacker can force the admins browser to make requests by sending them to an external page and update the admins password and email therefore taking over the admin panel.

Instructions: Host the exploit code included and have the admin visit the CSRF exploit page while logged in. It will be noticed that the password and email for the main admin have been changed to the specified email and password.

By: Liquidsky ^^ @ Specialized Security Services Inc. (S3) | Shout out to the team!
