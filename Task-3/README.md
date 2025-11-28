Task 3: Cloud-Based Bus Pass System (AWS Serverless)

**Overview**

This project is an online cloud-hosted bus ticket & pass booking system.  
It prevents ticket loss, theft, and incorrect pricing, and provides scalable, high-performance booking for users.

**Features**

- Online ticket/pass booking system.
- Prevents ticket loss, theft & incorrect pricing.
- Automatically scales to handle high traffic.
- Provides high reliability & low latency.
- Secure authentication + QR-based ticket verification.
- Supports dynamic fare calculation.

**AWS Architecture Used**

- **Amazon S3 + CloudFront** – Frontend hosting.
- **Amazon API Gateway** – REST API endpoints.
- **AWS Lambda** – Serverless backend logic.
- **Amazon DynamoDB** – Ticket & user database.
- **Amazon Cognito** – User authentication.
- **CloudWatch** – Monitoring & alerts.

**How It Works**

1. User opens the CloudFront website.
2. User submits booking → API Gateway → Lambda.
3. Lambda calculates fare + checks seat availability.
4. Unique ticket ID / QR generated → stored in DynamoDB.
5. User can view/download ticket any time.
6. Conductor can verify ticket using a scan endpoint.

