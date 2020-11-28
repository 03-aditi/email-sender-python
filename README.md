# email-sender-python

this script will send emails using smtp module in python 

# import smtplib
-> importing the module required to send emails
# from email.mime.multipart import MIMEMultipart
# from email.mime.text import MIMEText
-> these modules give flexibility to send text, images, attachments in emails

# email_content='hello'
-> header of email

# sender_address=''
# sender_pass=''
# receiver_address=''
-> provide the sender, receiver email address and sender passwd as well 

# message=MIMEMultipart()
-> create object of MIMEMultipart() class function in order to provide headers

# message['From']=sender_address
# message['To']=receiver_address
# message['Subject']='APPLICATION STATUS ALERT!!'
-> required headers inside email

# message.attach(MIMEText(email_content,'plain'))
-> write header in 'plain' format

# session=smtplib.SMTP('smtp.gmail.com',587)
-> create a session with email server 'smtp.gmail.com' working on 587 port

# session.starttls()
# session.login(sender_address,sender_pass)
-> start the session in secured manner using tls ie 'transport layer security'
-> provide sender credentials 

# text=message.as_string()
# session.sendmail(sender_address,receiver_address,text)
-> complete email will be sent after conversion to string 

# session.quit()
-> close the session after use

# print('Mail sent successfully!!')
-> output of the script
