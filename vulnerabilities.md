Web Vulnerabilities

1. SQL Injection (SQLi)

What is it?

SQL Injection occurs when an attacker inserts malicious SQL commands into user input.

How does it occur?

Applications directly concatenate user input into SQL queries without validation.

Example:

SELECT * FROM users WHERE username='admin' AND password='1234';

An attacker enters:

' OR '1'='1

The query becomes true for every user.

Prevention

- Prepared Statements
- Parameterized Queries
- Input Validation
- Least Privilege Database Accounts

---

2. Cross-Site Scripting (XSS)

What is it?

XSS allows attackers to inject malicious JavaScript into webpages.

How does it occur?

Applications display user input without sanitizing it.

Example:

<script>alert("XSS")</script>

Prevention

- Escape output
- Validate input
- Content Security Policy (CSP)

---

3. Broken Access Control

What is it?

Users access resources beyond their permissions.

How does it occur?

Applications fail to verify user authorization.

Example:

Changing

/user/profile/1

to

/user/profile/2

to access another user's information.

### Prevention

- Server-side authorization
- Role-Based Access Control
- Deny by default
- Regular security testing
