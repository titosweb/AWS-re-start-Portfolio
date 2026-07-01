# AWS Lambda Serverless Computing - Sales Analysis Report

## 📸 Architecture & Screenshots

### Lab Overview
![Lab Overview](Screenshot%20(14).png)

### Architecture Diagram
![Architecture Diagram](Screenshot%20(15).png)

### Café Website - Home Page
![Café Home Page](Screenshot%20(20).png)

### Order Confirmation
![Order Confirmation](Screenshot%20(21).png)

## 📖 Lab Overview

In this lab, I deployed and configured an **AWS Lambda-based serverless computing solution**. The Lambda function generates a sales analysis report by pulling data from a database and emailing the results daily.

### Business Scenario
A café wants to automatically generate daily sales reports to track their business performance. The solution needs to:
- Run automatically every day (Monday-Saturday at 8 PM)
- Pull sales data from a database
- Email the report to the admin
- Be cost-effective (serverless)

## 🏗️ Architecture Components

### AWS Services Used
| Service | Purpose |
|---------|---------|
| **AWS Lambda** | Serverless function that runs the sales report code |
| **Amazon CloudWatch Events** | Triggers Lambda daily at 8 PM (Mon-Sat) |
| **Amazon SNS** | Sends email notifications with the report |
| **AWS Systems Manager Parameter Store** | Securely stores database connection details |
| **Amazon EC2 (LAMP)** | Hosts the Cafe database (MariaDB/MySQL) |
| **IAM Roles** | Provides secure permissions between services |
| **VPC** | Isolates the database in a private network |

### Architecture Flow

