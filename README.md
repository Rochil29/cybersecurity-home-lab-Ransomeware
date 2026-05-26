# Python Ransomware Simulation

## ⚠ Disclaimer
This project is for **educational purposes only**.
Do NOT use this on any real system or against anyone without permission.
Only tested in an isolated lab environment (Kali Linux VM).

## Overview
A basic ransomware simulation built in Python using the Fernet 
symmetric encryption library. The project demonstrates how ransomware 
works — encrypting files and requiring a secret phrase to decrypt them.

## Files
- `risk.py` — Encrypts all files in the current directory
- `decrypt.py` — Decrypts files using the saved key + secret phrase

## How It Works

### Encryption (risk.py)
1. Scans the current directory for all files
2. Skips risk.py, decrypt.py and thekey.key
3. Generates a random Fernet encryption key
4. Saves the key to thekey.key
5. Encrypts every file using the key

### Decryption (decrypt.py)
1. Reads the saved key from thekey.key
2. Prompts user for a secret phrase
3. If phrase is correct — decrypts all files
4. If phrase is wrong — access denied

## Requirements
- Python 3
- cryptography library

## Installation
pip install cryptography

## Usage
Run encryptor:
python3 risk.py

Run decryptor:
python3 decrypt.py
Enter secret phrase: coffee

## Lessons Learned
- How Fernet symmetric encryption works
- How ransomware targets and encrypts files
- Importance of excluding key files from encryption
- How secret phrases can gate decryption access

## Tools Used
- Kali Linux
- Python 3
- cryptography (Fernet)
