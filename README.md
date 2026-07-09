# 🚨 IDS Evaluation & Application Security Recommendations

> Comparative NIDS/NIPS evaluation and OWASP-based web app remediation plan, built as part of SNHU CYB-220 & CYB-240 (Cyber Defense / Application Security).

## 📋 Overview

Two related deliverables combined into one project: (1) an evaluation of Network Intrusion Detection Systems (NIDS) vs. Network Intrusion Prevention Systems (NIPS) for a small organization applying least-privilege principles, and (2) an OWASP Top 10-based vulnerability assessment of a healthcare web application, identifying Sensitive Data Exposure and Broken Authentication issues.

## 🎯 Objective

Recommend an appropriate intrusion detection/prevention approach for a small organization's network, and separately, assess a healthcare web application for common web vulnerabilities with remediation guidance mapped to industry frameworks.

## 🧰 Tools & Concepts

- NIDS vs. NIPS comparison
- Least-privilege design principles
- OWASP Top 10
- HTTPS/TLS
- Role-Based Access Control (RBAC)
- MITRE ATT&CK framework

## 🔍 Methodology

### Part 1 — IDS/IPS Evaluation
1. Compared detection-only (NIDS) vs. inline prevention (NIPS) architectures for a small organization's threat model.
2. Applied least-privilege principles to determine where automated blocking (NIPS) was appropriate versus where analyst review (NIDS) was preferred.
3. Recommended a hybrid approach balancing automated response with human oversight.

### Part 2 — Web Application Security Review
1. Assessed a healthcare web application scenario against the OWASP Top 10, where data was transmitted over unencrypted HTTP between the web server and transaction server.
2. Identified **Sensitive Data Exposure** — unencrypted HTTP transmission of patient records and credentials, vulnerable to network sniffing and MITM attacks — and mapped it to the **Fail-Safe Defaults** and **Complete Mediation** security design principles.
3. Identified **Broken Authentication** — client-side login logic that could be bypassed or manipulated, plus a transaction server holding full administrative access to the MySQL database — and mapped it to the **Least Privilege** and **Separation of Privilege** principles.
4. Recommended remediations: HTTPS/TLS encryption and token-based authentication for data in transit; server-side authentication with MFA and bcrypt password hashing; restricting database admin access; and role-based access control (RBAC) with layered verification.

## ✅ Key Outcomes

- Recommended NIDS (over NIPS) for a small IT team, balancing detection effectiveness against the operational risk of automated blocking
- Identified two OWASP Top 10 vulnerabilities (Sensitive Data Exposure, Broken Authentication) in a healthcare application scenario
- Tied each finding to specific Saltzer & Schroeder security design principles (Fail-Safe Defaults, Complete Mediation, Least Privilege, Separation of Privilege)
- Produced remediation guidance grounded in HTTPS/TLS, MFA, RBAC, and centralized/server-side authentication

## 🧠 Skills Demonstrated

`NIDS/NIPS` `OWASP Top 10` `HTTPS/TLS` `RBAC` `MITRE ATT&CK` `Web Application Security` `Least Privilege`

## 📁 Files

- [`docs/7-2_Project_Three__Evaluation_of_Network_Protection_Technologies.docx`](docs/7-2_Project_Three__Evaluation_of_Network_Protection_Technologies.docx) — NIDS vs. NIPS evaluation and deployment plan (CYB-220)
- [`docs/7-2_Project_Two__Recommendations_Report.docx`](docs/7-2_Project_Two__Recommendations_Report.docx) — OWASP-based findings and remediation for Sensitive Data Exposure & Broken Authentication (CYB-240, Scenario One)
- [`docs/CYB_220_Module_Four_Activity_Student_File.pkt`](docs/CYB_220_Module_Four_Activity_Student_File.pkt) — supporting Packet Tracer lab file (CYB-220, Module Four)
- [`docs/CYB_220_Project_Two_Scenario_1_Student_Packet_Tracer_File.pkt`](docs/CYB_220_Project_Two_Scenario_1_Student_Packet_Tracer_File.pkt) — supporting Packet Tracer lab file (CYB-220, Project Two Scenario One)

---
🔗 Part of my [cybersecurity portfolio](https://samuelroulstone.com) · [Back to profile](https://github.com/samuelroulstone)
