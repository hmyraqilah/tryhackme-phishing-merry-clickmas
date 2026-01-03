# tryhackme-phishing-merry-clickmas
TryHackMe Phishing – Merry Clickmas write-up (Advent of Cyber 2025).
## 1. Introduction

This write-up documents the completion of the TryHackMe room **“Phishing – Merry Clickmas”**, which is part of the **Advent of Cyber 2025** series. The purpose of this exercise is to understand how phishing attacks are conducted and how attackers use social engineering techniques to trick users into revealing sensitive information.
In this lab, a simulated phishing campaign is performed using a fake login page and a crafted phishing email. The exercise demonstrates how easily users can be deceived by legitimate-looking messages and highlights the importance of cybersecurity awareness and email security.

 ## 2. Tools Used
The following tools and resources were used to complete this TryHackMe lab:

- TryHackMe AttackBox – Used as the attacker machine
- Social-Engineer Toolkit (SET) – Used to create and send a phishing emails
- Firefox Web Browser – Used to test the phishing page
- Phyton Phishing Server - Used to host a fake login page
- Linux Terminal - Used to execute commands and scripts

## 3. Lab Objectives
The objectives of this lab are as follows:

- To understand how phishing attacks are conducted
- To simulate a real-world phishing scenario in a controlled environment
- To host a fake login page used for credential harvesting
- To send a phishing email using social engineering techniques
- To observe how user credentials can be captured through phishing
- To improve awareness of phishing threats and prevention

## 4. Environment Setup
This lab was performed using the TryHackMe online platform. The provided **AttackBox** was used as the attacker machine, while the target system was preconfigured by TryHackMe.
Before starting the exercise, the following steps were completed:

1. The TryHackMe AttackBox was launched.
2. The target machine for the room was started.
3. Network connectivity between the attacker and target machines was verified.
4. The required files for the lab were located in the provided directory.

## 5. Task 1 – Hosting the Phishing Page
The first task in this lab involved hosting a fake login page that would be used to capture user credentials.

The phishing server script was provided by TryHackMe. The script was executed from the lab directory using the following command:
./server.py

![image alt](https://github.com/hmyraqilah/tryhackme-phishing-merry-clickmas/blob/33912c8b6f0d391557b4b65745babb64cb69e93d/Phishing_Server.png)

Once executed, the server started listening on port 8000 and was bound to all available network interfaces (0.0.0.0). This allowed the fake login page to be accessed through the AttackBox IP address.
To verify that the phishing page was working correctly, the following URL was opened in the browser:
http://10.49.79.194:8000

![image alt](https://github.com/hmyraqilah/tryhackme-phishing-merry-clickmas/blob/8e4f3a0ddd813288ede4d6848990f44bc6dd694e/Fake_Login_Page.png)

The page displayed a login interface designed to resemble a legitimate company portal. Any credentials entered into this page would be captured and displayed in the terminal running the phishing server.

## 6. Task 2 – Sending the Phishing Email
In this task, a phishing email was created and sent to the target user using the **Social-Engineer Toolkit (SET)**.
The toolkit was launched from the terminal using the following command:

```bash
setoolkit

The following options were selected within SET:
1. Social-Engineering Attacks
2. Mass Mailer Attack
3. Single Email Address
4. Use own server to open relay

The sender and recipient details were configured to appear legitimate. A realistic subject and message body were used to increase the likelihood of the recipient clicking the phishing link. The link to the fake login page hosted on the AttackBox was included in the email body. Once configured, the phishing email was sent successfully to the target user.

![image alt](set_email.png)

## 7. Task 3 – Capturing Credentials
After the phishing email was sent, the phishing server was monitored for incoming connections. When the target user clicked the link in the email and entered their login details, the credentials were captured by the phishing server and displayed in the terminal. This confirmed that the phishing attack was successful and demonstrated how attackers can obtain sensitive information through social engineering techniques.

![image alt](https://github.com/hmyraqilah/tryhackme-phishing-merry-clickmas/blob/9cb5e1cefc41b616e5be5ca9890eb4363a331a09/Captured_Credentials.png)

## 8. Results
The phishing simulation was completed successfully. The fake login page was hosted without issues, and the phishing email was delivered to the target user.
When the recipient interacted with the phishing link and submitted their credentials, the information was captured by the phishing server. This demonstrates how effective phishing attacks can be when users are unaware or do not verify email authenticity.

## 9. Conclusion
This lab provided hands-on experience with phishing attacks and social engineering techniques. It highlighted how attackers can exploit human behavior rather than technical vulnerabilities to gain unauthorized access to sensitive information.

The exercise emphasizes the importance of cybersecurity awareness, email verification, and user education as key defenses against phishing attacks. Understanding how these attacks work is essential for improving both personal and organizational security.

## 10. References

- TryHackMe. Phishing – Merry Clickmas.  
  https://tryhackme.com/room/phishing-aoc2025-h2tkye9fzU

- TryHackMe. Advent of Cyber 2025.  
  https://tryhackme.com/adventofcyber25

- Youtube. Phishing for Passwords! (Advent of Cyber Day 02)
  https://www.youtube.com/watch?v=w8O8FcRgDXU&t=1025s










