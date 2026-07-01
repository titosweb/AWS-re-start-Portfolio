# VPC Networking with Public & Private Subnets

## 📸 Screenshot
![VPC Architecture](Screenshot-70.png)
![Connectivity Check](Screenshot-71.png)

## 📖 Overview
Designed and built a custom VPC with both public and private subnets. The public subnet hosts a web server accessible via HTTP (port 80), while the private subnet contains a database that only accepts connections from the web server on port 3306 (MySQL).

## 🧠 What I Learned
- How to create a VPC with CIDR blocks (10.10.0.0/16)
- Difference between public and private subnets
- How to attach an Internet Gateway to enable internet access
- Configuring route tables to direct traffic
- Using Security Groups as virtual firewalls
- Best practice: keeping databases in private subnets for security
- How web servers and databases communicate in AWS

## 🔧 AWS Services Used
- Amazon VPC
- Subnets (Public & Private)
- Internet Gateway
- Route Tables
- Security Groups
- EC2 (Web Server) - conceptual
- RDS (Database) - conceptual
