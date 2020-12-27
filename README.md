# IMF-_CTF

## A vulnhub lab IMF
----------------------------------Basic Enumeration----------------------
Nmap scan:

PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: IMF - Homepage



Gobuster Scan:

/images (Status: 301)
/css (Status: 301)

/js (Status: 301)
/fonts (Status: 301)
/less (Status: 301)
/server-status (Status: 403)


-----------------------------------------------------------------------


-------------------------------------- all flags ----------------------

flag-1: flag1{YWxsdGhlZmlsZXM=}
YWxsdGhlZmlsZXM=(base64 encoded):allfiles

/////////////////////////////////////////
this part in the source code look supicious

  <script src="js/ZmxhZzJ7YVcxbVl.js"></script>
        <script src="js/XUnRhVzVwYzNS.js"></script>
        <script src="js/eVlYUnZjZz09fQ==.min.js"></script>
///////////////////////////////////////////////

combining all the three we get a base64 encoded text
ZmxhZzJ7YVcxbVlXUnRhVzVwYzNSeVlYUnZjZz09fQ==

flag-2: flag2{aW1mYWRtaW5pc3RyYXRvcg==}
Hint after decoding the base64:imfadministrator

flag-5 at <ip>/imfadministrator/uploadr942.php


------------------------------------------------------------------------
