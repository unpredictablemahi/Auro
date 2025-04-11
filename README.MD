3DOS Auto Registration Bot

This script automates the registration process for the 3DOS Dashboard, including email verification using FirstMail.ru IMAP.

Features

Uses email:password from emails.txt

Uses mail.firstmail.ru IMAP server (no proxy required)

Supports proxy rotation for registration requests

Generates a secure random password for each account

Stores successful accounts in success.txt

Handles email verification automatically



---

Prerequisites

1. Python 3

Ensure Python 3 is installed:

python3 --version

2. Install Dependencies

Install required packages:

pip install requests colorama

3. Files Required

emails.txt

Format: email:password

Example:

test1@firstmail.ru:pass1234
test2@firstmail.ru:mysecurepassword


proxy.txt

Format:

http://123.45.67.89:8080
http://user:pass@98.76.54.32:1080


success.txt

Will be automatically generated. Stores successfully registered accounts:

test1@firstmail.ru:generatedpassword1



---

Usage

Run the script with:

python3 your_script_name.py

You will be prompted to enter:

The number of accounts to register

A referral code (optional)


The script will:

1. Rotate proxies for each registration request.


2. Access the inbox via IMAP (no proxy) to verify the email.


3. Store all successful email:generated_password combos in success.txt.




---

Notes

Make sure all emails.txt entries are valid and IMAP-enabled.

The script sleeps briefly to allow verification emails to arrive.

Avoid running too many instances simultaneously to prevent IP blocks.



---

License

This project is for educational and automation purposes only.
