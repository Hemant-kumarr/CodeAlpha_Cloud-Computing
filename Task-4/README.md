Task 4: AI Chatbot (AWS Lex / Lambda)

**Overview**

This project develops an AI-powered chatbot that interacts with users on a website.  
It can answer queries, fetch data, and guide users based on predefined or generative patterns.

**Features**

- AI chatbot using **Amazon Lex**.
- Fast responses to user queries.
- Integrates easily with websites and backends.
- Uses predefined patterns + custom responses.
- Optional: Generative AI using **Amazon Bedrock**.
- Fully optimized and tested for accurate replies.

**AWS Architecture Used**

- **Amazon Lex** – Chatbot intelligence.
- **AWS Lambda** – Backend response logic.
- **Amazon DynamoDB** – Chat logs & contextual memory.
- **S3 Static Hosting** – Website + chatbot widget.
- **CloudWatch** – Monitor interactions.

**How It Works**

1. User opens website (S3 + CloudFront).
2. Chat widget loads Lex bot.
3. User types a question → Lex intent matching.
4. For simple queries → Predefined Lex replies.
5. For advanced logic → Lambda is triggered:
   - Fetches data from DynamoDB  
   - Processes logic  
   - Returns dynamic response  
6. Lex sends response back to user.

