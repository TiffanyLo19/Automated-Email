import time
import os
import datetime
import smtplib
from email.message import EmailMessage

while True:
    unix = int(time.time())
    time1 = str(datetime.datetime.fromtimestamp(unix).strftime('%I:%M:%S:%p'))

    if time1 == 'hour:minutes:seconds:AM/PM':
        EMAIL_ADDRESS = os.environ.get('EMAIL_USER')
        EMAIL_PASSWORD = os.environ.get('EMAIL_PASS')
        contacts = ['youAreSendingTo@gmail.com']
        msg = EmailMessage()
        msg['Subject'] = 'Type your subject line here'
        msg['From'] = EMAIL_ADDRESS
        msg['To'] = 'youAreSendingTo@gmail.com'
        msg.set_content('Type your body text here')
        with smtplib.SMTP_SSL('smtp.gmail.com', 465) as smtp:
            smtp.login('EMAIL_ADDRESS', 'EMAIL_PASSWORD')
            smtp.send_message(msg)
            print("\n Message Sent")
