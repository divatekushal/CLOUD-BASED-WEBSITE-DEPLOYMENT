# AWS Cloud-Based Website Deployment

This project demonstrates the process of setting up a scalable web server infrastructure on AWS. The setup includes deploying a static website on an EC2 instance using IIS, creating an Amazon Machine Image (AMI) for replication, and configuring a load balancer for high availability and scalability.

## Actions Taken

### 1. **EC2 Instance Setup with IIS and Static Website**
- Launched an EC2 instance using the "Microsoft Windows Server 2012 R2 Base" AMI on AWS.
- Automated the installation of IIS (Internet Information Services) using user data scripts during instance initialization.
- Uploaded a static website to the instance’s directory (`C:\inetpub\wwwroot\`).
- Verified the website's functionality using the instance's public IP address.

### 2. **Creation of Amazon Machine Image (AMI)**
- After confirming the static website deployment and IIS configuration, I created an Amazon Machine Image (AMI).
- The AMI captured the exact state of the EC2 instance, including software and settings, allowing for consistent and efficient replication of the web server environment.

### 3. **Launching a New EC2 Instance Using the AMI**
- Utilized the created AMI to launch a new EC2 instance.
- This new instance inherited the exact configuration of IIS and the static website, ensuring consistency across instances.

### 4. **Configuration of Target Group for Load Balancing**
- Created a target group in AWS, adding both the original EC2 instance and the newly launched instance.
- This configuration enabled load balancing, distributing incoming traffic evenly across instances based on defined criteria such as round-robin or least connections.

### 5. **Setup of Application Load Balancer (ALB)**
- Implemented an Application Load Balancer (ALB) for managing incoming HTTP traffic.
- Configured listeners and routing rules to direct traffic efficiently to the EC2 instances in the target group.
- Verified the operational status of the static website through the DNS name associated with the ALB.

## Conclusion

By following this structured approach, I successfully deployed and configured a scalable web server infrastructure on AWS. The project leverages automation for rapid deployment, AMIs for configuration consistency, and load balancing for enhanced performance and fault tolerance. This setup ensures the website operates seamlessly in the cloud environment, capable of handling fluctuating traffic demands effectively.

## Technologies Used

- AWS EC2 (Elastic Compute Cloud)
- IIS (Internet Information Services)
- Amazon Machine Images (AMI)
- AWS Application Load Balancer (ALB)
- Target Group and Load Balancing

