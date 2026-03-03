
# 🔐 Python Password Strength Checker

## 📌 Project Overview

This project demonstrates a simple cybersecurity tool written in Python that evaluates password strength based on common security best practices.

The goal is to promote secure password habits and demonstrate basic scripting skills for security automation.

---

## 🛠 How It Works

The script checks if a password:

* Has at least 8 characters
* Contains uppercase letters
* Contains lowercase letters
* Includes numbers
* Includes special characters

Based on these criteria, the password is classified as:

* Weak
* Moderate
* Strong

---

## 🧠 Python Script

```python
import re

def check_password_strength(password):
    score = 0

    if len(password) >= 8:
        score += 1
    if re.search(r"[A-Z]", password):
        score += 1
    if re.search(r"[a-z]", password):
        score += 1
    if re.search(r"[0-9]", password):
        score += 1
    if re.search(r"[!@#$%^&*(),.?\":{}|<>]", password):
        score += 1

    if score <= 2:
        return "Weak Password"
    elif score == 3 or score == 4:
        return "Moderate Password"
    else:
        return "Strong Password"

password = input("Enter your password: ")
result = check_password_strength(password)
print(result)
```

---

## ▶ How to Run

1. Install Python (version 3.x)
2. Save the script as:

```
password_checker.py
```

3. Run:

```
python password_checker.py
```

---

## 🔐 Security Concepts Demonstrated

* Password security best practices
* Input validation
* Regular expressions (regex)
* Basic automation scripting
* Security awareness

---

## 🎯 Why This Project Matters

This project demonstrates:

* Practical Python scripting skills
* Understanding of password security policies
* Ability to build simple security tools
* Foundational automation mindset (important in SOC environments)

---

## 👩‍💻 Author

Cybersecurity professional in training
Google Cybersecurity Certified
Aspiring SOC Analyst (USA 2026)
