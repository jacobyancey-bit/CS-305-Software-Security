# CS 305: Software Security — Portfolio Artifact

## Project Overview: Artemis Financial Security Modernization
This repository contains a security assessment and refactoring project completed for **Artemis Financial**, a financial consulting firm specializing in personalized financial planning. The goal of this project was to identify vulnerabilities in a legacy web application and implement defensive coding practices—specifically secure RESTful web services, transport layer encryption, and data integrity verification—to safeguard sensitive client data and financial transactions.

### Included Artifact
CS_305_Artemis_Financial_Report.docx — Detailed analysis of codebase vulnerabilities and mitigation strategies.

---

## Module Eight Journal Reflection

### 1. Client Summary and Software Requirements
Artemis Financial is a financial consulting firm that required an upgrade to their software's security infrastructure to protect sensitive client data and financial transactions. The primary issue the company wanted addressed was the lack of secure operational practices within their existing web application. Specifically, they needed to implement secure RESTful web services, establish encrypted communications, and ensure data integrity to protect against data interception and tampering.

### 2. Vulnerability Identification and the Value of Security
During the vulnerability assessment, I effectively utilized automated scanning tools alongside manual code reviews to isolate outdated dependencies and unencrypted data pathways. 

* **Importance of Secure Coding:** Writing secure code from the ground up is vastly more efficient than trying to patch a vulnerable architecture after deployment. It ensures that data confidentiality, integrity, and availability are maintained by default.
* **Corporate Well-Being:** Software security directly protects a company’s reputation, preserves user trust, and prevents catastrophic financial liabilities or regulatory non-compliance penalties.

### 3. Challenges and Insights in Vulnerability Assessment
The most challenging yet rewarding part of the vulnerability assessment was interpreting the automated dependency scan reports and mapping those findings to actionable refactoring steps. Dissecting vulnerability technical details to determine whether a specific flaw actually exposed our specific implementation required a deep dive into how our libraries interacted. This process was highly helpful because it shifted my perspective from just making code "work" to understanding how code can be exploited.

### 4. Layering Security and Future Mitigation Strategies
I increased the layers of security by implementing a multi-layered defense strategy:
* **Transport Layer Security:** Configured HTTPS using a digital certificate generated via Java Keytool to encrypt data in transit.
* **Data Integrity Layer:** Integrated a cryptographic checksum verification program using SHA-256 to verify that financial data remains unaltered during processing.

In the future, I will use industry-standard static application security testing (SAST) tools like SonarQube and dependency analyzers like OWASP Dependency-Check to proactively identify vulnerabilities during the continuous integration (CI/CD) pipeline.

### 5. Ensuring Functionality and Verifying Refactored Code
To guarantee the application remained both functional and secure, I ran regression tests and verified API endpoints after every major security insertion. After refactoring the code to include the new security configurations, I performed the following verification steps:
1. Re-ran the dependency analyzer to ensure no new vulnerable libraries were introduced.
2. Validated the SSL/TLS handshake locally to ensure the server accepted secure HTTPS requests.
3. Executed the checksum generation logic against known data inputs to verify that the cryptographic output was accurate and predictable.

### 6. Tools, Resources, and Future Practices
Several key tools and practices utilized in this project will be vital in my future software engineering tasks:
* **Java Keytool:** For managing keystores, certificates, and encryption keys.
* **Cryptographic Libraries:** Utilizing built-in Java security packages (`MessageDigest`) to implement standard hashing algorithms safely.
* **Secure Coding Standards:** Adhering to the OWASP Top 10 guidelines as a baseline checklist during development rather than as an afterthought.

### 7. Showcasing Skills to Future Employers
From this assignment, I can show future employers a concrete example of defensive software engineering. Specifically, I can demonstrate my ability to take a legacy, insecure software artifact and systematically refactor it to meet modern cryptographic and security compliance standards. The repository showcases practical experience with certificate management, data integrity verification, and architectural risk mitigation—skills that transition directly into protecting enterprise-level software systems.
