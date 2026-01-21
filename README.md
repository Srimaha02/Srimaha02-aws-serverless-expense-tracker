# AWS Serverless Expense Tracker 💸

A beginner-friendly **serverless cloud project** built using AWS.  
This project demonstrates how to design a backend system **without managing servers**, using AWS managed services.

---

## 🚀 Project Overview

The **Serverless Expense Tracker** allows users to add daily expenses through an HTTP API.  
Each expense is processed by AWS Lambda and securely stored in DynamoDB.

The system is:
- Fully serverless
- Auto-scalable
- Cost-efficient
- AWS Free Tier safe

---

## 🛠️ AWS Services Used

- **AWS Lambda** – Backend business logic  
- **Amazon API Gateway** – Public HTTP endpoint  
- **Amazon DynamoDB** – NoSQL database for storing expenses  
- **AWS IAM** – Secure permissions between services  

---

## 🔁 Architecture Flow

Client (Thunder Client / App / Website)
|
v
Amazon API Gateway (POST /add-expense)
|
v
AWS Lambda (ExpenseHandler)
|
v
Amazon DynamoDB (Expenses Table)

yaml
Copy code

---

## 📌 API Details

### Endpoint
POST /add-expense

bash
Copy code

### Sample Request Body
```json
{
  "date": "2026-01-22",
  "category": "Food",
  "amount": 120
}
Sample Response
json
Copy code
{
  "message": "Expense added successfully"
}
🧠 How It Works (Simple Explanation)
The client sends expense details using a POST request.

API Gateway receives the request and forwards it to Lambda.

Lambda function:

Generates a unique expense ID

Processes the data

Stores it in DynamoDB

DynamoDB saves the expense permanently.

A success response is returned to the client.

🔒 Security & Cost Safety
No EC2 or servers used

No hard-coded credentials

IAM roles used for secure access

Uses only AWS Free Tier eligible services

No running resources when idle

🧪 Testing
The API was tested using Thunder Client in VS Code by sending POST requests with JSON data.
Each request stores a new expense record in DynamoDB.


💡 Key Learnings
Serverless architecture concepts

Event-driven backend design

AWS Lambda execution model

API Gateway routing

DynamoDB NoSQL data storage

IAM role-based security


👩‍💻 Author
Sri Mahalakshmi.R
B.Tech Information Technology
Cloud Computing Enthusiast

⭐ If you like this project, feel free to star the repository!
