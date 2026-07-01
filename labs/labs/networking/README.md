# VPC Networking with Public & Private Subnets

## 📸 Architecture Diagrams

### VPC Design
![VPC Architecture](Screenshot%20(70).png)

### Connectivity Check
![Connectivity Check](Screenshot%20(71).png)

## 📖 Overview
This project demonstrates a basic AWS networking setup using a Virtual Private Cloud (VPC). I designed a network with both public and private subnets to host a web server and a database following AWS best practices for security.

**The architecture includes:**
- **VPC:** 10.10.0.0/16 (my private network in AWS)
- **Public Subnet:** 10.10.0.0/24 (hosts the web server)
- **Private Subnet:** 10.10.2.0/24 (hosts the database)
- **Internet Gateway:** Allows public subnet to reach the internet
- **Router (Route Table):** Directs traffic between subnets and the internet
- **Security Groups:** Virtual firewalls controlling traffic

**Security Rules Configured:**
- **HTTP (port 80):** Allowed to the web server so users can access it
- **MySQL (port 3306):** Allowed ONLY from the web server to the database

**The connection flow:**
1. User accesses web server via the internet → HTTP (port 80)
2. Web server talks to database → MySQL (port 3306)
3. Database is NOT directly accessible from the internet (secure!)

## 🧠 What I Learned

### AWS Networking Fundamentals
- **VPC (Virtual Private Cloud):** How to create an isolated network in the cloud with custom IP ranges (CIDR blocks)
- **Subnets:** The difference between public (internet-accessible) and private (isolated) subnets
- **Internet Gateway:** How to attach a gateway to enable internet access from your VPC
- **Route Tables:** Configuring routing rules to direct traffic where it needs to go
- **Security Groups:** Using them as stateful firewalls to control inbound/outbound traffic

### Best Practices
- **Defense in depth:** Never expose databases directly to the internet
- **Least privilege:** Only open the ports that are absolutely needed (80 for web, 3306 for MySQL)
- **Separation of concerns:** Keeping web tier and database tier in different subnets

### Real-World Application
This is a **common pattern** used in production environments:
- Frontend web servers in public subnets
- Backend databases in private subnets
- Proper security groups to control traffic flow

## 🔧 AWS Services Used
- Amazon VPC (Virtual Private Cloud)
- Subnets (Public and Private)
- Internet Gateway
- Route Tables
- Security Groups
- EC2 (Web Server - conceptual)
- RDS (Database - conceptual)

## 🏆 Skills Demonstrated
- Cloud architecture design
- Networking concepts in AWS
- Security best practices
- Infrastructure planning
- Hands-on AWS console experience
