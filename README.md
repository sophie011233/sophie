import smtplib
from email.mime.text import MIMEText

# 设置电子邮件内容
msg = MIMEText('Hello, world!')
msg['Subject'] = 'Test email'
msg['From'] = 'sender@example.com'
msg['To'] = 'recipient@example.com'

# 发送电子邮件
 = smtplib.SMTP('smtp.gmail.com', 587)
s.starttls()
s.login('sender@example.com', 'password')
s.sendmail('sender@example.com', ['recipient@example.com'], msg.as_string())
s.quit()
