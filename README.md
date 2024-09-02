# React-application-with-CI-CD-using-AWS-amplify
## **AWS Project Name: React application with CI/CD with GitHub**

**Project description:**
This project involves building a simple React application that allows users to answer quiz questions. The tools I will be using to help me build this project are AWS Amplify, AWS Cognito, GitHub, and VS code. I followed a Tiny Technical Tutorials video on how this application was built.

**Project Architecture:** 

<ins>refer to --> architecture.png</ins>

## **Steps in the Project:**

### **Step 1:** Setting up the environment and installing amplify CLI
-	During this step, I used the command “npm install -g @aws-amplify/cli” on the terminal in VScode to install the Amplify CLI 
-	Next, I used the command “amplify configure” where I created a new user under the name “Amplify-dev” enabling administrator control on Amplify

### **Step 2:** Creating React application
-	Executed command “npx create-react-app my-quiz-app” to create the application with the name “my-quiz-app”, 
-	Execute command “amplify init” to initialize app on AWS cloud under name “myquizapp”
 
<ins>refer to --> image 1.png</ins> 

### **Step 3:** Adding Authentication using AWS Cognito
-	Execute “amplify add auth” to add authentication using AWS cognito
-	Select “Default configuration” and allow users to sign-in using Email
-	Execute “amplify push” to build local backend I just created in the cloud
  
<ins>refer to --> image 2.png</ins>
  
### **Step 4:** Creating UI log in 
-	On VScode I accessed “App.js” and replaced following code with code provided by “Tiny technical tutorials”
-	Downloaded Amplify libraries by executing “npm install aws-amplify @aws-amplify/ui-react” to allow me to run the code
-	Executed “npm start” to launch the website allowing me to create an account
  
<ins>refer to --> image 3.png</ins>

### **Step 5:** Adding code for quiz application, adding functionality
-	Code for Quiz UI from “Tiny technical tutorials” added to new js file under “Quiz.js”
-	Created customized quiz questions under “quizData.js” 

<ins>refer to --> image 4.png</ins>

### **Step 6:** Pushing code into the GitHub Repository
-	Create a new GitHub repository under name “amplify-cognito-quiz”
-	Used Git commands following GitHub instructions git init , git commit “First Commit”, git branch -M main, git remote add origin https://githubrepository , git push origin main
-	Using commands allowed me to push code from VScode into my GitHub Repository


### **Step 7:** Linking AWS Amplify and GitHub Repository allowing CI/CD
-	Went into Amplify and going into “Branches” and clicked th GitHub option; after linking account I selected my repository “amplify-cognito-quiz”
-	Enabled full-stack CI/CD 
-	Launched and deployed application on the cloud

<ins>refer to --> image 5.png + image 6.png</ins>

## Problems faced during the project

### Problem in Step 1
-	One of the problems I faced during this process was setting up NodeJs properly on VS code as it was a new process to me. I learned I needed to set the right PATH for VScode to use NodeJs properly
-	The second problem I ran into was when I used “amplify configure,” I had an error message letting me know my computer restricted running commands. I found out that I needed to enable access to run this command and to do this, I ran Powershell as an administrator and used the command “Set-ExecutionPolicy Unrestricted”

### Problem in Step 6
-	The problem I ran into was installing Git and understanding that I needed to configure Git before I could properly use it. I found out as I used “git commit” the error “Please tell me who you are” came up. After going into the terminal and performing git configure –global user.email “name@gmail” and  “git configure –global user.name “full name” I was able solve my problem


## Summary
This project taught me the basics of AWS's two AWS services, AWS Amplify and AWS Cognito, and showed how the two services can be used in unison to create a web application. This project also taught me the basics of CI/CD and how to link GitHub to my Amplify application to allow for changes on GitHub to be applied immediately to my application on the web. This project even with the help of ‘Tiny Tech Tutorials” was quite tricky as I still ran into some problems that were not covered and I had to do external research and reading to solve them. Overall, this was a very fun project that gave me some essential skills in not only AWS architecture but also problem solving


Credit: https://www.youtube.com/@TinyTechnicalTutorials
