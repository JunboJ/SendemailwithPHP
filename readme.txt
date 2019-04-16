1.you need to change the security setting in your gamil to turn on the access of less secure app

2.download sendmail.zip and put all the file in a folder named 'sendmail' in the root folder of your wamp

3.download stunnel and install it

4.Change sendemail.ini:

smtp_server= localhost
smtp_port=25
smtp_ssl=auto
default_domain= gmail.com
auth_username= //here is your email address
auth_password= //here is the password of your email

comment out 
pop3_server=
pop3_username=
pop3_password=


5.change stunnel.conf:
delete every thing and copy paste the code below

[gmail-smtp]
client = yes
accept = 127.0.0.1:25
connect = smtp.gmail.com:465
verifyChain = yes
CAfile = ca-certs.pem
checkHost = smtp.gmail.com
OCSPaia = yes


6.change php.ini:

[mail function]

SMTP =

smtp_port = 25

sendmail_from = movielover.jar@gmail.com

sendmail_path = "C:\wamp64\sendmail\sendmail.exe -t -i"
