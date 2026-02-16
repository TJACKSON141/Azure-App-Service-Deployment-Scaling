# 🚀 Azure App Service Deployment & Scaling

## 📌 Overview
This project demonstrates deploying a web application on Azure App Service, implementing CI/CD with GitHub Actions, using deployment slots for safe releases, configuring autoscaling based on performance metrics, enabling backups for recovery, and monitoring application health with alerts.



## 🏗 Architecture Overview
- Users access a web application hosted on Azure App Service  
- CI/CD deploys code from GitHub to Azure  
- Deployment slots enable safe staging → production swaps  
- Autoscaling adjusts instances based on CPU load  
- Backups provide disaster recovery  
- Azure Monitor tracks performance and triggers alerts  



## 🛠 Technologies Used
- Azure App Service  
- App Service Plan (Basic B1)  
- Deployment Slots  
- GitHub Actions (CI/CD)  
- Azure Monitor  
- Azure Alerts  
- Azure Storage (Backups)  



## 1️⃣ Create an App Service



- Created an App Service with a Basic B1 App Service Plan (lowest tier that supports deployment slots).  
- Selected runtime stack (Node.js/Python/.NET) and deployed to a new resource group.



## 2️⃣ Deploy the Web Application (CI/CD)



- Connected GitHub repository via Deployment Center.  
- Configured GitHub Actions for automated deployments.  
- Verified successful deployment by accessing the App Service URL.



## 3️⃣ Set Up Deployment Slots (Staging → Production)



- Created a `staging` deployment slot.  
- Deployed a new app version to staging.  
- Tested the staging URL.  
- Swapped staging to production for zero-downtime release.



## 4️⃣ Configure Autoscaling



- Enabled autoscaling on the App Service Plan.  
- Configured scale-out rule: +1 instance if CPU > 70% for 10 minutes.  
- Configured scale-in rule: -1 instance if CPU < 30% for 20 minutes.  
- Set max instances = 2 to control costs.



## 5️⃣ Backup and Restore



- Configured backups to an Azure Storage account.  
- Performed a manual backup of the App Service.  
- (Optional) Validated restore to a new App Service for recovery testing.



## 6️⃣ Monitor and Configure Alerts



- Monitored CPU, requests, and response time using Azure Monitor metrics.  
- Created an alert to notify when CPU usage exceeds 70%.



## 🔐 What This Project Demonstrates

### What I Built
- Production-ready Azure App Service deployment  
- CI/CD pipeline using GitHub Actions  
- Blue/Green deployments using deployment slots  
- Autoscaling based on performance metrics  
- Backup and recovery configuration  
- Monitoring and alerting for application health  

### Skills Demonstrated
- Azure App Service management  
- CI/CD pipelines (GitHub Actions)  
- Deployment strategies (staging → production)  
- Autoscaling & performance tuning  
- Backup & disaster recovery  
- Monitoring & alerting  
- AZ-104 application hosting best practices  
