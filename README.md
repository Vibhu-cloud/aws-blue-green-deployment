# aws-blue-green-deployment
Aws Blue-Green Deployment using EC2, Target Groups, and application load balancer.


# AWS Blue-Green Deployment on AWS

## Project Overview

This project demonstrates a Blue-Green Deployment strategy on AWS using Amazon EC2, Application Load Balancer (ALB), and Target Groups. The objective is to deploy a new application version with minimal downtime by switching traffic between Blue and Green environments.

---

## AWS Services Used

- Amazon EC2
- Application Load Balancer (ALB)
- Target Groups
- Amazon VPC
- Security Groups
- Apache HTTP Server (httpd)

---

## Project Architecture

```
                Users
                  |
                  v
      Application Load Balancer
                  |
        -----------------------
        |                     |
        v                     v
 Blue Target Group     Green Target Group
        |                     |
   Blue EC2 Servers     Green EC2 Servers
```

---

## Deployment Workflow

1. Created two EC2 instances for the Blue environment.
2. Installed and configured Apache HTTP Server.
3. Created the Blue Target Group and registered Blue instances.
4. Created an Application Load Balancer and configured the listener.
5. Verified the Blue application through the ALB DNS.
6. Launched two EC2 instances for the Green environment.
7. Created the Green Target Group and registered Green instances.
8. Updated the ALB listener rule to forward traffic from the Blue Target Group to the Green Target Group.
9. Verified that the application was successfully served from the Green environment.

---

## Project Screenshots

### 1. Blue Environment - EC2 Instances

![](screenshots/Screenshot%20(175).png)

### 2. Blue Environment Output

![](screenshots/Screenshot%20(176).png)

### 3. Blue Target Group

![](screenshots/Screenshot%20(177).png)

### 4. Application Load Balancer (Active)

![](screenshots/Screenshot%20(178).png)

### 5. Blue Application through Load Balancer

![](screenshots/Screenshot%20(179).png)

### 6. Green Environment - EC2 Instances

![](screenshots/Screenshot%20(180).png)

### 7. Load Balancer Forwarding Traffic to Blue Target Group

![](screenshots/Screenshot%20(181).png)

### 8. Listener Rule Updated - Traffic Shifted to Green Target Group

![](screenshots/Screenshot%20(182).png)

### 9. Green Environment Output

![](screenshots/Screenshot%20(183).png)

### 10. Green Target Group

![](screenshots/Screenshot%20(184).png)

---

## Outcome

- Successfully implemented Blue-Green Deployment on AWS.
- Achieved traffic switching using an Application Load Balancer.
- Demonstrated deployment with minimal downtime.
- Enabled easy rollback capability by changing the ALB listener rule.
- Gained hands-on experience with EC2, Target Groups, Load Balancer, and deployment strategies.

---

## Author

**Vibhu Sharma**

GitHub: **VibuCloud**
