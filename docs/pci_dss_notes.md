# PCI DSS Compliant User Management for NoShow

Please be aware to handle your user management in a PCI DSS compliant way. PCI DSS requires certain user and
password policies. Below you will find all necessary information for a PCI DSS compliant user management in a
nutshell. A more detailed version on PCI DSS user management can be found in the official PCI DSS 3.0 document
which can be downloaded under Section 1, Supporting Developer Manuals.

## Unique User IDs
Every single user having access to the No-Show.jsp needs to have a unique user login to be clearly identified.
Shared user logins are not allowed.

## Password Policy
In general, the following password rules have to be observed:

* Passwords must be changed at least every 90 days.  
* The password must have a minimum length of 8 characters.
* The password must contain upper and lower case letters, numbers and at least one special character.
* When changing the password none of the last four passwords can be used.
* After 6 failed login attempts a user account is locked. It can only be unlocked by the administrator.
* After 15 minutes of inactivity, the password must be entered to reactivate the terminal / session.
* The maximum session time after which the user must log in again must not exceed 200 minutes.
* The duty of care for handling of “identifying imprint” should be handed over to the merchant about the general conditions of contract.

## No-Show usage Logging
All activity related to the No-Show.jsp has to be logged to provide documentary evidence. Logs must record every
time someone accesses regulated data (including cardholder data and log data) to enable a “who-did-what-and-
when” audit trail.