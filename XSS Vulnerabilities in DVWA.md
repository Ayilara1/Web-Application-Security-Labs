#  Session Management and Web Security
## CSRF Protection Laboratory

**Module:**  – Session Management and Web Security  
**Submission Date:** 19 February 2025

---

# Overview

This laboratory focused on **Session Management** and **Cross-Site Request Forgery (CSRF)** protection in web applications. The practical exercises were conducted using **DVWA (Damn Vulnerable Web Application)** to understand how CSRF attacks work, how they can be exploited, and how secure implementations prevent unauthorized requests.

> **Disclaimer**
>
> This project was completed in a controlled cybersecurity laboratory for educational purposes only.

---

# Learning Objectives

- Understand session management principles
- Learn how CSRF attacks work
- Perform CSRF attacks on a vulnerable application
- Understand CSRF tokens
- Test CSRF protection mechanisms
- Analyze secure web application defenses
- Recommend security best practices

---

# Introduction

Session management is responsible for maintaining authenticated user sessions after login while ensuring secure communication between users and web applications.

Effective session management includes:

- Secure session identifiers
- Secure cookies
- Session timeout
- Session invalidation
- Protection against session hijacking
- Protection against session fixation
- Protection against replay attacks

Web security complements session management through:

- Authentication
- Authorization
- HTTPS/TLS
- Input validation
- Secure coding practices
- Regular security assessments

---

# Lab Environment

- Kali Linux
- DVWA (Damn Vulnerable Web Application)
- Apache Web Server
- PHP
- MySQL
- Firefox Browser

---

# Exercise 1 – Understanding CSRF Attacks

## Objective

Demonstrate how a CSRF attack can force an authenticated user to perform unintended actions.

### Observation

A password change request was submitted successfully without verifying whether the request originated from the legitimate application.

### Result

The password was changed successfully.

This confirms that the vulnerable DVWA application was susceptible to Cross-Site Request Forgery attacks.

An attacker could potentially:

- Change account passwords
- Modify account information
- Transfer funds
- Delete user data
- Execute other authenticated actions without user consent

---

## Screenshot

```
images/exercise1-csrf-success.png
```

---

# Importance of CSRF Protection

Proper CSRF protection helps to:

- Prevent unauthorized requests
- Protect sensitive user actions
- Preserve data integrity
- Protect financial transactions
- Improve user trust
- Meet security compliance requirements
- Reduce attack surface

---

# Exercise 2 – Implementing CSRF Protection

## Objective

Understand how CSRF tokens protect sensitive requests.

### CSRF Protection Process

### Step 1

Server generates a unique token.

↓

### Step 2

Token is stored within the user's session.

↓

### Step 3

Token is inserted into every sensitive HTML form.

↓

### Step 4

User submits the form.

↓

### Step 5

Server validates the submitted token.

↓

### Step 6

If valid → Request accepted.

If invalid → Request rejected.

---

## Example HTML

```html
<form action="/update-profile" method="POST">

<input type="hidden"
name="csrf_token"
value="a9f8a7d6c5e4b3a2c1d0">

<input type="text"
name="username">

<input type="submit"
value="Update">

</form>
```

---

## Screenshot

```
images/exercise2-csrf-token.png
```

---

# Exercise 3 – Testing CSRF Protection

## Objective

Verify whether the application validates CSRF tokens.

### Test Performed

The CSRF token was deliberately removed before submitting the form.

### Result

```
CSRF token validation failed
```

The server rejected the request because the required token was missing.

### Conclusion

The application correctly validates CSRF tokens before processing requests.

---

## Screenshot

```
images/exercise3-token-validation.png
```

---

# CSRF Token Removal Test

## Objective

Determine whether the application enforces token validation.

### Procedure

1. Open the vulnerable form
2. Remove the hidden CSRF token
3. Submit the request

### Result

Request rejected.

### Evaluation

The application correctly blocked unauthorized requests.

This demonstrates that CSRF protection is functioning properly.

---

# Reflection

## Limitations of CSRF Tokens

Although CSRF tokens provide strong protection, they still have limitations.

### Token Leakage

If an attacker successfully performs an XSS attack, CSRF tokens may be stolen.

### Weak Token Generation

Predictable tokens reduce security.

### Token Reuse

Static tokens can be replayed.

### Poor Validation

Applications must verify both:

- Presence
- Correctness

of every token.

### User Experience

Frequent token expiration may interrupt user sessions.

---

# Possible CSRF Bypass Techniques

Potential attacker techniques include:

- Cross-Site Scripting (XSS)
- Session Fixation
- Clickjacking
- Weak token generation
- Browser vulnerabilities
- Poor application implementation

---

# Additional Security Controls

Modern applications should combine CSRF tokens with:

- SameSite Cookies
- HTTPS
- Content Security Policy (CSP)
- Multi-Factor Authentication (MFA)
- User verification for sensitive actions
- Secure session management
- X-Frame-Options
- Regular penetration testing
- Security audits
- Secure coding practices

---

# Skills Demonstrated

- Session Management
- CSRF Attack Analysis
- CSRF Protection
- DVWA Testing
- Web Application Security
- Secure Authentication
- Token Validation
- Security Testing

---

# Tools Used

| Tool | Purpose |
|-------|----------|
| DVWA | Vulnerable Web Application |
| Kali Linux | Security Testing |
| Firefox | Browser Testing |
| Apache | Web Server |
| PHP | Backend Application |
| MySQL | Database |

---

# Learning Outcomes

After completing this lab, I was able to:

- Understand session management principles
- Explain how CSRF attacks work
- Demonstrate CSRF exploitation
- Implement CSRF protection
- Validate CSRF tokens
- Identify weaknesses in web applications
- Recommend industry best practices for secure web development

---

# Repository Structure

```
INT308-Session-Management-Web-Security/
│
├── README.md
├── report.pdf
└── images/
    ├── exercise1-csrf-success.png
    ├── exercise2-csrf-token.png
    ├── exercise3-token-validation.png
    └── csrf-workflow.png
```

---

# Security Concepts Covered

- Session Management
- Session Tokens
- Cookies
- CSRF
- SameSite Cookies
- Secure Cookies
- Authentication
- Authorization
- Content Security Policy (CSP)
- HTTPS
- OWASP Top 10
- Secure Web Development

---

# Disclaimer

This project was conducted in an isolated educational laboratory using intentionally vulnerable applications. The techniques demonstrated are intended solely for cybersecurity education, defensive security research, and authorized penetration testing.

---

## Author

**Ayilara Busari Dare**

- Student ID: IDEAS/24/28133
- Module: INT308 – Session Management and Web Security
- Year: 2025
