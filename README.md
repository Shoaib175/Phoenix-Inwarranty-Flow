# 🚀 Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for POC for integrating your postman test with GitHub Actions. The tests are written in Postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of cron job.

The HTML reports is archived and kept in the artifacts section for the team to download. Along with that, they can view the report directly from the github page - https://shoaib175.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP

## 👤 Author

**Shoaib Shaikh**  
SDET with **4.5+ years of experience** designing and implementing scalable, CI/CD-driven automation frameworks for web and API platforms.

### Core Expertise
- UI Automation: Selenium WebDriver, Playwright, Cypress  
- API Automation: Postman, Rest Assured  
- CI/CD & DevOps: GitHub Actions, Jenkins  
- Automation Strategy, Test Architecture, Reporting & Metrics  

🔗 **LinkedIn:** https://www.linkedin.com/in/shaikhshoaib175/

## ✨ Key Highlights

- 🔁 CI/CD-driven API automation on every push to `main`
- ⏱ Scheduled regression runs via cron
- 📊 Rich HTML reports with historical traceability
- 🌐 Live report hosting using GitHub Pages
- 📧 Automated email notifications with latest execution results
- 🔐 Secure secrets management using GitHub Secrets
- ⚙️ Self-hosted GitHub runner on AWS EC2

## 🧪 Test Coverage

- ✅ Happy-path & business-critical flows  
- ❌ Negative and edge-case validation  
- 🔐 Token lifecycle & authorization checks  
- 📊 Data-driven testing using CSV  
- 📐 Schema & contract validation  
- 🔑 Secrets management with GitHub Secrets

## 🏗 Architecture Overview

> **Execution Flow**
1. Code is pushed to the `main` branch  
2. GitHub Actions triggers the workflow  
3. APIs execute via Newman on AWS EC2 self-hosted runner  
4. HTML report is generated and archived  
5. Report is published to GitHub Pages  
6. Latest execution summary is emailed to stakeholders  

## 🛠 Tech Stack

| Layer | Tools |
|------|------|
| API Testing | Postman |
| Runtime | Node.js (v22) |
| Test Runner | Newman |
| Reporting | newman-reporter-htmlextra |
| CI/CD | GitHub Actions |
| Infrastructure | AWS EC2 (Self-hosted Runner) |
| Notifications | Gmail SMTP |
| Reporting Portal | GitHub Pages |
| Test Data | CSV |

## 📊 Live Test Report

🔗 **Latest Report via Github Pages**  
You can directly view the latest test report of the postman Test at the Github pages :
https://shoaib175.github.io/Phoenix-Inwarranty-Flow/

![Postman Report](https://raw.githubusercontent.com/Shoaib175/Phoenix-Inwarranty-Flow/static-content/newman-report-html.png)

## 📁 Project Structure

```text
Phoenix-Inwarranty-Flow
├─ In-WarrantyFlow-Data-Driven.postman_collection
├─ QA.postman_environment.json
├─ testdata.csv
└─ newman/
   └─ index.html
```

## How to run the Project locally? ##
You can run the project on your local system - 
1. Clone the project on the local system - ```git clone https://github.com/Shoaib175/Phoenix-Inwarranty-Flow.git```
2. Install Nodejs and NPM from https://nodejs.org/en using - ```sudo apt install nodejs```
3. Install Newman using ```npm install -g newman```
4. Install newman-reporter-htmlextra using ```npm install -g newman-reporter-htmlextra```
5. Run the newman command:
```
newman run In-WarrantyFlow-Data-Driven.postman_collection \
-e QA.postman_environment.json \
-d testdata.csv \
-r cli,htmlextra \
--reporter-htmlextra-export ./newman/index.html  
```
