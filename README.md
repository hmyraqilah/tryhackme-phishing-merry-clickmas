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

![image alt]()









