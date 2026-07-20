# Port Scan Report

## Scan Information

**Tool Used:** Nmap 7.99

**Command Executed:**

```bash
nmap 127.0.0.1
```

**Target:** Localhost (127.0.0.1)

**Scan Date:** 20 July 2026

## Scan Results

| Port     | State | Service      | Description                                                                                                                                                      |
| -------- | ----- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 135/tcp  | Open  | MSRPC        | Microsoft Remote Procedure Call, used by Windows for communication between applications and services.                                                            |
| 445/tcp  | Open  | Microsoft-DS | Microsoft Directory Services (SMB), commonly used for Windows file and printer sharing.                                                                          |
| 1521/tcp | Open  | Oracle       | Default port used by Oracle Database Listener. Indicates an Oracle database service may be running.                                                              |
| 3000/tcp | Open  | PPP          | Often used by development servers such as React, Node.js, or other local web applications. Nmap labels it as PPP, but many development tools also use this port. |
| 5357/tcp | Open  | WSDAPI       | Web Services for Devices API, used by Windows for discovering network devices such as printers and scanners.                                                     |
| 5560/tcp | Open  | ISQLPLUS     | Associated with Oracle iSQL*Plus or Oracle-related services.                                                                                                     |
| 8080/tcp | Open  | HTTP-Proxy   | Common alternative HTTP port used by web servers, application servers, proxies, or local development environments.                                               |


# Analysis

The scan found **7 open TCP ports** on the localhost system.

* **Port 135 (MSRPC):** Required by Windows for Remote Procedure Call services.
* **Port 445 (Microsoft-DS):** Used for Windows file and printer sharing. If file sharing is not needed, restricting access with a firewall is recommended.
* **Port 1521 (Oracle):** Indicates an Oracle Database service is available.
* **Port 3000:** Commonly used by local web development servers (for example, Node.js or React applications).
* **Port 5357 (WSDAPI):** Used by Windows device discovery services.
* **Port 5560 (ISQLPLUS):** Related to Oracle database services.
* **Port 8080 (HTTP-Proxy):** Often used by web applications or local web servers.


# Security Implications

Open ports allow network communication with the services running on them. While necessary services must remain open, unnecessary open ports can increase the attack surface of a system. Services should be kept updated, and unused services should be disabled or protected using firewall rules.


# Reflection

This assignment demonstrated two important aspects of cybersecurity. First, weak passwords are vulnerable to brute-force and dictionary attacks, making unauthorized access much easier. Using long passwords with uppercase letters, lowercase letters, numbers, and special characters greatly improves security.

Second, open ports reveal which services are running on a computer. Attackers often perform port scans to identify potential targets and search for vulnerable services. Regularly scanning your own system, closing unused ports, enabling firewalls, and keeping software updated are effective practices for reducing security risks.



This report is tailored to the Nmap output shown in your screenshot and is appropriate for your internship submission.
