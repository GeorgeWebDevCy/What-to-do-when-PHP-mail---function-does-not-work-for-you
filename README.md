# What to do when PHP mail() function does not work for you
-----------------------------------------------------------

When using WordPress
----------------------
Simply install a plugin called WP Mail SMTP by WPForms from https://wordpress.org/plugins/wp-mail-smtp/

When your SMTP does require authentication
==========================================
Goto your php.ini file and look for the mail function section. 
In this section you might see something like
SMTP = localhost
You should change it to something like what is shown below. Make sure you use the same setting like you use in outlook for example for that same domain/account
SMTP = smtp.example.com
smtp_port = 25
username = info@example.com
password = yourmailpassword
sendmail_from = info@example.com

When your SMTP does NOT require authentication
==============================================
Goto your php.ini file and look for the mail function section. 
In this section you might see something like
SMTP = localhost
You should change it to something like what is shown below. Make sure you use the same setting like you use in outlook for example for that same domain/account
SMTP = smtp.example.com
smtp_port = 25


related blog post is here: https://www.georgenicolaou.me/php-mail-function-doesnt-work/