# Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for POC for integrating your postman test with GitHub Actions. The tests are written in Postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of cron job.

The HTML reports is archived and kept in the artifacts section for the team to download. Along with that, they can view the report directly from the github page - https://shoaib175.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP

## About Me ##

Hi! My name is Shoaib Shaikh. I have 4+ years of experience in Test Automation. My skillset includes UI Automation using Selenium Webdriver, Playwright, Cypress and for API Testing I use Rest Assured & Postman.
You can connect me over: (https://www.linkedin.com/in/shaikhshoaib175/)

## Test Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Node.js (v22.0)
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self-hosted github runner

## Github Pages ##
You can directly view the latest test report of the postman test at the Github page link: https://shoaib175.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the newman folder

![Postman Report](https://raw.githubusercontent.com/Shoaib175/Phoenix-Inwarranty-Flow/static-content/newman-report-html.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ In-WarrantyFlow-Data-Driven.postman_collection # Collection file
├─ QA.postman_environment.json # Environment File
└─ testdata.csv # Test Data File

```

## How to run the Project? ##
You can run the project on your local system - 
1. Clone the project on the local system - https://github.com/Shoaib175/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
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

