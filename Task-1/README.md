Task 1: Data Redundancy Removal System (AWS-Based)

**Overview**
This project identifies and removes duplicate data before inserting it into the database.  
The goal is to maintain **clean, accurate, and efficient** data storage by preventing redundant or false-positive entries.

**Features**
Detects duplicate or redundant data entries.
Validates incoming data against existing database records.
Inserts only **unique and verified** data.
Improves overall **database performance and accuracy**.
Automates the duplication check using serverless AWS services.

**AWS Architecture Used**
Amazon API Gateway – Receives incoming data.
AWS Lambda (Python) – Applies validation logic.
Amazon DynamoDB – Stores unique data.
Amazon CloudWatch – Logs for monitoring duplicate detection.
IAM Roles – Secure resource access.

**How It Works**
1. User sends data via API Gateway (POST request).
2. API Gateway triggers a Lambda function.
3. Lambda checks DynamoDB to verify if the record already exists:
   - If it exists → `duplicate = true`
   - If not → Inserts the new unique data
4. Lambda returns the result to the user.


