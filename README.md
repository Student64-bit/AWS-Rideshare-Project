# AWS Rideshare Project

## Overview

This project showcases the integration of various AWS components for hosting and managing an existing unicorn rideshare application. While the application itself was not created by me, I implemented the integration of AWS services to demonstrate scalability, security, and functionality enhancements.

## AWS Services Used

- **Amplify:** Utilized for hosting and continuous deployment of application changes.
- **Cognito:** Implemented for user login authentication.
- **Lambda:** Employed to handle user application data and interact with DynamoDB.
- **IAM:** Set up to ensure least privilege and adhere to good security practices.
- **CodeCommit:** Used for version control and storage of code.
- **DynamoDB:** Chosen as the database to store application data created by users.
- **API Gateway:** Implemented to build a RESTful API and invoke Lambda functions for application tasks and communication with Cognito.

## Setup and Functionality

### 1. Setting up Permissions for the Code

The initial step involved creating a new IAM user account with appropriate permissions. This practice mitigates security risks associated with using AWS root accounts and follows the principle of least privilege. Permissions granted include access to CodeCommit for file storage.
<img src="https://i.imgur.com/CZR8v71.png" height="80%" width="80%" alt="Code commit permissions"/>
<br />
<br />

### 2. Storing, Updating, and Pulling the Code

CodeCommit was utilized to fork the tutorial code into a personal repository and clone the contents. HTTPS Git commit permissions were granted to the IAM user to enable HTTPS connections to CodeCommit, facilitating the use of AWS CloudShell for forking/cloning files.
<img src="https://i.imgur.com/HCzCrc3.png" height="80%" width="80%" alt="Https git credentials"/>
<br />
<br />

### 3. Using Amplify to Host the Web Application Files from CodeCommit

Leveraging the serverless and fully managed Amplify service, the website files were hosted with continuous deployment capabilities. Any changes made to files in CodeCommit were automatically reflected on the website within minutes.
<img src="https://i.imgur.com/wDijTv2.png" height="80%" width="80%" alt="Https git credentials"/>
<br />
<br />

### 4. Implementing User Authentication with Cognito

Cognito user pools were utilized to implement user login and registration functionalities along with JWT-based authentication. Upon signing up, users were required to verify themselves with a code sent via email.
<img src="https://i.imgur.com/BOI6xdO.png" height="80%" width="80%" alt="Https git credentials"/>
<br />
<br />

### 5. Application Functionality using Lambda and DynamoDB

A Lambda function was created to select a unicorn for the rideshare fleet and store the relevant data in DynamoDB. The choice of a non-relational database like DynamoDB was suitable for this use case due to the simplicity of data requirements.

### 6. Utilizing API Gateway to Invoke Lambda Functions

Lastly, a RESTful API was created using API Gateway to invoke the Lambda function for storing user data in DynamoDB when users interacted with the application using HTTP POST methods.
<img src="https://i.imgur.com/8AAuQBN.png" height="80%" width="80%" alt="Https git credentials"/>
<br />
<br />
<img src="https://i.imgur.com/8wXScb9.png" height="80%" width="80%" alt="Https git credentials"/>
<br />
<br />
<img src="https://i.imgur.com/CTI3Oib.png" height="80%" width="80%" alt="Https git credentials"/>
<br />
<br />



## Video Demo

