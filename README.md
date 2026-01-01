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



### Hash Generation
Passwords were hashed using MD5 to demonstrate weak hashing.  
Hashes were saved in `clean_hashes.txt`.



## Password Cracking Process
- A dictionary attack was performed using John the Ripper
- RockYou wordlist was used to simulate a real-world attack
- Cracked passwords were displayed using `john --show`


## Results Summary

| Password     | Status       | Explanation                                    |
|-------------|-------------|-----------------------------------------------|
| password    | Cracked     | Common dictionary password                     |
| 1234567890  | Cracked     | Predictable numeric pattern                    |
| admin       | Cracked     | Default administrative password                |
| ohiozoje    | Not Cracked | Personal name; weak but not in the wordlist   |

**Result:**  
> 3 out of 4 passwords were cracked using a basic dictionary attack.

---

## Key Findings
- Dictionary attacks quickly crack common and predictable passwords
- Passwords based on personal information (names, usernames) are still weak
- Absence of cracking does not equal security
- Security depends on entropy, complexity, and unpredictability
- SOC teams need to monitor password practices and detect weak password patterns

---

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


