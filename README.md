# Password Cracking & Security Awareness Lab

## Overview
This project demonstrates the security risks of weak passwords using a controlled, ethical lab environment.  
Test passwords were hashed and analyzed using John the Ripper to show how easily common passwords can be compromised through dictionary attacks.

**Ethical Notice:**  
All passwords used in this lab were self-created test passwords.  
No real user credentials, systems, or production environments were involved.


## Objective
- Demonstrate how weak passwords can be cracked quickly
- Understand how attackers exploit poor password hygiene
- Highlight best practices for password security and SOC monitoring


## Tools & Technologies
- Kali Linux
- John the Ripper
- MD5 hashing (for demonstration only)
- RockYou wordlist
- Linux Terminal

### Test Passwords Used
The following passwords were tested:
- password
- 1234567890
- admin
- ohiozoje

> Note: `ohiozoje` was not cracked using the default dictionary attack.  
> This does not mean it is secure — it is a personal name and could be cracked with a targeted/custom wordlist.

## Lab Demonstration (Visual Evidence)

The screenshot below shows the complete end-to-end workflow on a single page:
- Original weak passwords
- Generated MD5 hashes
- Successful password cracking using John the Ripper

[![Password Cracking Workflow](Password%20Cracking%20Workflow.png)](https://github.com/Zoje-stack/Password-Cracking-and-Security-Awareness-/blob/2c94a20e94eb7121679b87a135fb123fce94b81c/Password%20Cracking%20Workflow.png)

### Hash Generation
Passwords were hashed using MD5 to demonstrate weak hashing.  
Hashes were saved in `clean_hashes.txt`.



## Password Cracking Process
- A dictionary attack was performed using John the Ripper
- RockYou wordlist was used to simulate a real-world attack
- Cracked passwords were displayed using `john --show`

## Dictionary Attack Simulation (RockYou Wordlist)

To simulate a real-world attack scenario, the widely used RockYou wordlist was employed.

[![RockYou Wordlist](RockYou%20Wordlist.png)](https://github.com/Zoje-stack/Password-Cracking-and-Security-Awareness-/blob/2c94a20e94eb7121679b87a135fb123fce94b81c/RockYou%20Wordlist.png)

The RockYou wordlist contains millions of real leaked passwords, making it a realistic tool attackers use to exploit weak credentials.

## Results Summary

| Password     | Status       | Explanation                                    |
|-------------|-------------|-----------------------------------------------|
| password    | Cracked     | Common dictionary password                     |
| 1234567890  | Cracked     | Predictable numeric pattern                    |
| admin       | Cracked     | Default administrative password                |
| ohiozoje    | Not Cracked | Personal name; weak but not in the wordlist   |

**Result:**  
> 3 out of 4 passwords were cracked using a basic dictionary attack.


## Key Findings
- Dictionary attacks quickly crack common and predictable passwords
- Passwords based on personal information (names, usernames) are still weak
- Absence of cracking does not equal security
- Security depends on entropy, complexity, and unpredictability
- SOC teams need to monitor password practices and detect weak password patterns


## Security Recommendations
- Avoid passwords based on:
  - Names
  - Usernames
  - Birthdays
  - Personal identifiers
- Use long passphrases with unrelated words
- Protect credentials with:
  - Strong hashing (bcrypt, Argon2)
  - Multi-Factor Authentication (MFA)
- Apply password spraying detection in SOC environments
- Educate users on strong password hygiene



## Conclusion
Three weak passwords were cracked almost instantly using a dictionary attack.  
The password `ohiozoje` was not cracked, but this does not mean it is secure — personal names remain vulnerable to targeted attacks.  

This lab demonstrates that weak passwords are the easiest security gap and emphasizes the need for:
- Strong password policies  
- User education  
- Monitoring and SOC enforcement


