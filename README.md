# Postman API Automation Integration with Github Actions #
This repository is a demonstration for Proof of concept for integrating postman test with github actions. The Test are written in Postman and they are excuted on the VM with help of newman and newman-reporter-htmlextra.
Github Action will trigger the poject execution on every push to the main branch. you can also execute the project manually using workflow_dispatch. The Projects runs on a sheduled time with the help of the cron job.

The HTML reports is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page: https://github.com/HeenaSk18/Phoenix-Inwarranty-Flow/new/
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi, My name HEENA SHAIKH. I have 4+ year of Experience Automation Testing skills with Manual Testing, API, SQL, Java, Selenium, TestNG and other frameworks, Maven, Jenkins, BDD Cucumber, JIRA and Git/GitHub.
linkedin 
https://www.linkedin.com/in/heena-shaikh-software-engineer/ 

## Testing Coverage ##
1. Happy Flow Testing
2. Neagtive Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Node.js 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://github.com/HeenaSk18/Phoenix-Inwarranty-Flow/new/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/HeenaSk18/Phoenix-Inwarranty-Flow/blob/main/image.png)

## Project Structure ##
```
Phoenix-Inwarranty-Flow
├─ Inwarranty-flow Collection.postman_collection.json # Colletion File
├─ QA.postman_environment.json #Envirnment File
└─ testData.csv #TestData File

```

## How to run the Project? ##
You can run the project on your local system for that:
1. Clone the Project on Local System: https://github.com/HeenaSk18/Phoenix-Inwarranty-Flow/new.git
2. Install Node.js and NPM from https://nodejs.org/en
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra ``` npm install -g newman-reporter-htmlextra ```
5. Run the new Comman:
```
              newman run 'Inwarranty-flow Collection.postman_collection.json' \
             -e QA.postman_environmnent.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htlextra-export ./newman/index.html
```

