Change sendemail.php

smtp_server= localhost
smtp_port=25
smtp_ssl=auto
default_domain= gmail.com
auth_username=movielover.jar@gmail.com
auth_password=jarmovielover!


change stunnel.conf

[gmail-smtp]
client = yes
accept = 127.0.0.1:25
connect = smtp.gmail.com:465
verifyChain = yes
CAfile = ca-certs.pem
checkHost = smtp.gmail.com
OCSPaia = yes