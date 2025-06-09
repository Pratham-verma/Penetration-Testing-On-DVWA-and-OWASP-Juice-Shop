# 🛡️ Web Application Threat Report: DVWA & OWASP Juice Shop

This repository contains a complete **security assessment and threat mapping report** for two intentionally vulnerable web applications:

- **DVWA (Damn Vulnerable Web Application)**
- **OWASP Juice Shop**

The report simulates **real-world attack scenarios** aligned with the **OWASP Top 10 vulnerabilities** and provides in-depth analysis, proof-of-concepts (PoCs), and mitigation strategies.

---

## 🕵️‍♂️ Identified Vulnerabilities

### 🔐 DVWA Vulnerabilities

| #  | Vulnerability        | Affected URL                   | Severity | Description                                                                 |
|----|----------------------|--------------------------------|----------|-----------------------------------------------------------------------------|
| 1  | SQL Injection        | `/vulnerabilities/sqli/`       | High     | Allows attackers to manipulate database queries and extract sensitive data. |
| 2  | Blind SQL Injection  | `/vulnerabilities/sqli_blind/` | High     | Similar to SQLi but data is inferred through server behavior and timing.    |
| 3  | Stored XSS           | `/vulnerabilities/xss_stored/` | Medium   | Injected scripts persist and execute on other users’ browsers.              |
| 4  | Reflected XSS        | `/vulnerabilities/xss_reflected/` | Medium | Script is reflected off the server and executed in the victim’s browser.    |
| 5  | DOM-based XSS        | `/vulnerabilities/xss_d/`      | Medium   | JavaScript manipulation allows execution of malicious scripts.              |
| 6  | CSRF                 | `/vulnerabilities/csrf/`       | Low-Med  | Forces user to perform actions like password change without consent.        |

---

### 🧃 OWASP Juice Shop Vulnerabilities

| #  | Vulnerability          | Affected URL         | Severity | Description                                                                 |
|----|------------------------|----------------------|----------|-----------------------------------------------------------------------------|
| 1  | Broken Access Control  | `/administration`    | High     | Allows unauthorized access to admin functions.                              |
| 2  | Security Misconfiguration | `/rest/products/` | Medium   | Debug tools or headers leak sensitive configuration data.                   |
| 3  | Sensitive Data Exposure | `/ftp`              | High     | Exposes unencrypted sensitive files or credentials.                         |
| 4  | Broken Authentication  | `/login`             | High     | Brute-force attacks possible due to missing rate-limiting or MFA.           |
| 5  | CAPTCHA Bypass         | `/contact`           | Medium   | CAPTCHA can be bypassed via automation or missing backend validation.       |

---

## 📘 What's Inside the Report?

The PDF report includes:

- ✅ **Executive Summary**
- ✅ **Tools and Testing Methodology**
- ✅ **Technical Breakdown of Each Vulnerability**
- ✅ **Payloads and Proof of Concepts (PoCs)**
- ✅ **Real-World Attacker Thinking**
- ✅ **Risk & Impact Analysis**
- ✅ **Recommendations and Mitigation**
- ✅ **Conclusion and Strategic Advice**
- ✅ **Risk Analysis Diagrams and Tables**

---

## 📥 How to Download the Report

You can download or view the full report using the options below:

### ➤ Clone the Repository

```bash
git clone https://github.com/Pratham-verma/Penetration-Testing-On-DVWA-and-OWASP-Juice-Shop.git
```

---

## 🚀 How to Run DVWA Locally

### Prerequisites

- PHP 7.x or higher  
- MySQL or MariaDB  
- Apache or any web server supporting PHP  

### Clone and Setup

```bash
git clone https://github.com/digininja/DVWA.git
cd DVWA
```
### Configure Database

    Create a database named dvwa in MySQL.
    Edit config/config.inc.php to set your MySQL username and password.

### Set Permissions

```bash
chmod -R 777 hackable/uploads/ dvwa/config/
```

### Launch Web Server

    Point your web server root to the DVWA folder.
    Access http://localhost/DVWA/setup.php in your browser.
    Follow instructions to create tables.

### Login

    Default credentials:
    Username: admin
    Password: password

## 🚀 How to Run OWASP Juice Shop Locally

### Prerequisites

    Node.js (version 12+)
    npm (comes with Node.js)

### Clone and Setup

```bash
git clone https://github.com/juice-shop/juice-shop.git
cd juice-shop
npm install
```

### Run the Application

```bash
npm start
```

### Access the Application

Open your browser and go to:

```bash
http://localhost:3000
```
---

## 🎯 Ideal For

This report is highly beneficial for:

- 🧑‍💻 **Security Researchers**
- 🐞 **Bug Bounty Hunters**
- 🎓 **Cybersecurity Students**
- 🔴🔵 **Red Team / Blue Team Exercises**
- 🛡️ **Security Awareness and Training Programs**

---

## 🤝 Connect

Feel free to connect or reach out for collaboration or questions:

- GitHub: [Pratham-verma](https://github.com/Pratham-verma)
- LinkedIn: [linkedin.com/in/pratham-verma](https://www.linkedin.com/in/pratham-verma-7685b8220/).
