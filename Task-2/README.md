Task 2: Detecting & Preventing Data Leaks Using SQL Injection (AWS)

**Overview**

This project builds a secure cloud system that protects against SQL Injection attacks and prevents unauthorized data access.  
It implements encryption, parameterized queries, and multi-layer protection.

**Features**

- Secures user data from SQL injection attacks.
- Uses **AES-256 encryption** for sensitive data.
- Implements **double-layer security protocol**.
- Uses **capability code mechanism** for controlled SQL execution.
- Fully accessible over the internet with HTTPS protection.

**AWS Architecture Used**

- **Amazon RDS (MySQL/Postgres)** – Encrypted relational database.
- **AWS Lambda / EC2** – Backend application server.
- **Amazon API Gateway / ALB** – Public-facing secure access.
- **AWS WAF** – SQL Injection protection rules enabled.
- **AWS Secrets Manager** – Stores DB credentials.
- **AWS KMS** – Encrypts sensitive fields.

**Security Layers Implemented**
**Application-Level Security**
- Parameterized & prepared SQL statements.
- Input validation.
- Predefined capability tokens.

**Infrastructure-Level Security**

- WAF SQL Injection filters.
- RDS encryption at rest (AES-256).
- IAM-based DB access.
- HTTPS-only API Gateway.

**How It Works**

1. User request → API Gateway → Lambda/EC2 backend.
2. WAF filters malicious SQL injection payloads.
3. Backend uses parameterized queries (no inline concatenation).
4. Sensitive fields (password, card info etc.) encrypted using KMS.
5. Encrypted data stored in RDS.
6. Only valid capability tokens can perform certain SQL operations.


