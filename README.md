# IT-PROJECT-
Flowchart 

Comprehensive Keylogger and Phishing Simulation for Cybersecurity Defense
Project Overview
This project demonstrates how a keylogger and a phishing attack can be used together to simulate a real-world cybersecurity threat. The purpose is to help security professionals and students understand how these attacks work, the risks involved, and how to develop appropriate defenses.

Disclaimer
This project is for educational and ethical cybersecurity purposes only. Unauthorized use of keyloggers or phishing techniques is illegal. Use only in controlled environments with proper authorization.

Features
Keylogger:
Keystroke Logging: Captures all keys pressed, including special keys like Enter, Backspace, and Space, and logs them to a text file.
File Archiving: Once the log file reaches 300 bytes, it is moved to an archive for organization and later reference.
Email Exfiltration: Archived logs are automatically sent to a predefined email address for review and analysis.
Silent Operation: Runs in the background without alerting the user, demonstrating the danger of undetected keylogging tools.
Phishing Simulation:
Social Engineering: A phishing email is crafted to convince the recipient to download and run the malicious keylogger, disguised as a legitimate update or software.
Executable File Delivery: The phishing email contains a link to the keylogger executable, tricking the user into executing the program.
Project structure 
/
├── real.py             # Main Python script for keylogging, archiving, and sending logs via email
├── dist/               # Directory where the executable is stored after compilation
├── log_archive/        # Folder where archived log files are saved
│   └── mylog_archive.txt  # Archived log file
└── mylog.txt           # Current log file where keystrokes are captured
Requirements
To run this keylogger, ensure you have the following:

Python  installed.
Install the required Python libraries:
pip install pynput
Access to Gmail SMTP for sending emails: 
Gmail credentials for both sender and recipient.
An App Password if two-factor authentication (2FA) is enabled.
How it works:
1. Keylogging
The script listens for keystrokes using the pynput library.
Every keystroke, including both regular and special characters, is logged in mylog.txt.
For example:
Pressing a is logged as a.
Pressing Space is logged as [SPACE], making the logs more readable.
Pressing Backspace is logged as [BACKSPACE].
2. Log Archiving and Emailing
Once the log file exceeds 300 bytes, it is moved to the archive folder (log_archive/).
The existing archive is overwritten if a new archive is created.
The script automatically sends the archived log to the attacker’s email using Gmail’s SMTP server.
Key Components:
Log File Archival: Automatically archives keystrokes to avoid detection by limiting the size of the log.
3. Email Exfiltration:
The archived log is sent to a pre-configured email address using Gmail’s SMTP server.
The email includes the archived log as an attachment and mentions the machine’s username in the subject line.
The sender’s and recipient’s email addresses and SMTP credentials need to be set in the script.
SMTP Email Exfiltration: Uses secure email transmission to send the captured logs to the attacker.
4.Email Setup
Sender Email: The Gmail account used to send logs.
Recipient Email: The email address where logs are delivered.
FROM_EMAIL_ADDRESS = "your-email@gmail.com"
FROM_EMAIL_PASSWORD = "your-app-password"
TO_EMAIL_ADDRESS = "recipient-email@gmail.com”
5. Phishing Simulation:
A phishing email is crafted to mimic a game update or software patch. It contains a download link to the keylogger executable.
The recipient, thinking it’s a legitimate update, downloads and runs the file, which starts the keylogger.
Creating the Executable
To simulate a real-world phishing attack, the Python script is converted into an executable file.

Steps to Create Executable:
pip install pyinstaller
Convert Script to Executable: Run the following command to bundle the script into a single executable:
pyinstaller --onefile real.py
This command generates an executable in the dist/ folder, which can be distributed as part of a phishing attack.
Advantages of an Executable:
The executable allows the keylogger to run on systems without Python installed.
The phishing attack becomes more convincing, as the user only needs to double-click the executable, making the attack appear seamless.
Phishing Simulation
The phishing email plays a crucial role in convincing the recipient to execute the keylogger. Below is an expanded explanation of how the phishing simulation works.

Phishing Email Crafting
In this simulation, the phishing email is designed to look like a legitimate message from a game or software vendor. The email tricks the recipient into clicking a link that downloads the keylogger executable.

Example Phishing Email:
Subject: Urgent Game Update Available – v2.0 Released

Hi [Username],

We’ve just released the latest update for [Game Name] featuring new levels, bug fixes, and performance enhancements!

Download the update here: [link to the keylogger executable]

Thanks for being part of the community!

Best regards,
The [Game Name] Team
Steps in Phishing Simulation:
Email Design: Use professional language and design to mimic a real software company’s update email.
Executable Link: Host the keylogger executable on a trusted platform (like Google Drive or Dropbox) to avoid suspicion.
Phishing Victim’s Action: When the recipient downloads and runs the executable, the keylogger is silently installed and starts logging keystrokes.
Defense Mechanisms and Ethical Considerations
Why Simulate a Keylogger and Phishing Attack?
Simulating a keylogger with phishing allows cybersecurity professionals to understand the attacker’s mindset and develop strong countermeasures. Some of the key defense tactics include:

Anti-phishing software: Filters and flags potentially harmful emails before they reach users.
Security Awareness Training: Educating users about recognizing phishing emails and suspicious links.
Keylogger Detection: Using anti-malware solutions that can identify keyloggers running in the background.
2FA (Two-Factor Authentication): Adding an extra layer of security for login credentials, mitigating the damage of keyloggers.
Security Best Practices
How to Defend Against Keyloggers and Phishing:
Email Filtering: Use robust email filtering systems to block phishing attempts.
User Training: Continuously educate users to avoid clicking suspicious links or downloading unknown attachments.
Keylogger Detection: Install endpoint protection systems that scan for keylogging activity.
Regular Monitoring: Regularly monitor system processes for suspicious behavior, such as unknown executables running in the background.
Encrypted Communication: Use encryption for sensitive data to protect against interception by keyloggers.
Ethical and Legal Considerations
Legal Compliance: Operating a keylogger without explicit permission is a breach of privacy and illegal in most jurisdictions. Always ensure full compliance with laws such as the GDPR.
Ethical Use: Only use this keylogger in controlled environments such as testing labs, and always obtain prior consent from the participants.
Ethical and Legal Considerations
Legal Compliance: Operating a keylogger without explicit permission is a breach of privacy and illegal in most jurisdictions. Always ensure full compliance with laws such as the GDPR.
Ethical Use: Only use this keylogger in controlled environments such as testing labs, and always obtain prior consent from the participants.

Ethical and Legal Considerations
Legal Compliance: Operating a keylogger without explicit permission is a breach of privacy and illegal in most jurisdictions. Always ensure full compliance with laws such as the GDPR.
Ethical Use: Only use this keylogger in controlled environments such as testing labs, and always obtain prior consent from the participants.
Conclusion
This project provides a deep understanding of how keylogging and phishing attacks work, simulating a scenario that can educate individuals on the importance of cybersecurity defense. The project demonstrates the need for vigilance in recognizing phishing attempts and mitigating keylogger threats.

By combining social engineering (phishing) with malicious software (keylogging), this project emphasizes the role of awareness and proper defense mechanisms in the fight against cyber threats.

Contact Information
Author: Michael (Mikky)
Email: soretireopeyemi113@gmail.com


