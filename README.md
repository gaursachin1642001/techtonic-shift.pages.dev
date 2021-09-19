# wordpress1
cheetsheet for wordpress

Version and theme detection using http-wordpress-info script

nmap -sV --script http-wordpress-info

* Password selection by dictionaries

nmap -p80 --script http-wordpress-brute --script-args 'userdb=users.txt,passdb=passwords.txt' example.com

Metasploit:
* Module for determining the version
auxiliary/scanner/http/wordpress_scanner

* Module for defining username
auxiliary/scanner/http/wordpress_login_enum
WPScan:

* Listing the installed plugins:
wpscan --url www.exmple.com --enumerate p;

* Enumeration of the installed themes
wpscan --url www.exmple.com --enumerate t:;

* Transfer set timthumbs:
wpscan --url www.example.com --enumerate tt;

* Defining username
wpscan --url www.example.com --enumerate u:;

* Password guessing dictionary for user admin:
wpscan --url www.example.com --wordlist wordlist.txt --username admin;

* Selection of the password using the username ligament / password with the number of streams of 50:
wpscan --url www.example.com --wordlist wordlist.txt --threads 50
