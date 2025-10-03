# Hello Java Maven - Jenkins Build Demo

This project demonstrates how to build a simple Java application using **Maven** in **Jenkins**.  
It is part of Task 8: *Run a Simple Java Maven Build Job in Jenkins*.

---

## 📂 Project Structure
hello-java-maven/
├── pom.xml
├── README.md
├── screenshots/
│ └── build-success-1.png
  └── build-success-2.png
└── src/main/java/
└── HelloWorld.java

yaml
Copy code

- **HelloWorld.java** → A simple Java program that prints `"Hello, Jenkins + Maven!"`.  
- **pom.xml** → Maven configuration file with compiler plugin setup.  
- **README.md** → Documentation file (this one).  
- **screenshots/** → Folder containing Jenkins build output screenshots.  

---

## 🛠 Prerequisites
- **Java JDK 8 or 11**  
- **Apache Maven** (configured in Jenkins)  
- **Jenkins** (installed locally or via Docker)  
- **Git** (optional)  

---

## 🚀 Steps to Run in Jenkins

1. **Start Jenkins**  
   
   docker run -d -p 8080:8080 --name jenkins jenkins/jenkins:lts
   
Configure Maven in Jenkins

Go to Manage Jenkins → Global Tool Configuration

Add Maven (e.g., Maven 3.8.6)

Create a Freestyle Job

Job type: Freestyle Project

Source: Point to this repo or upload files manually

Build → Invoke top-level Maven targets

Goals: clean package

Build the Job

Click Build Now

Check Console Output for:

[INFO] BUILD SUCCESS

Expected Output

When the build is successful, the console output should include

Hello, Jenkins + Maven!

[INFO] BUILD SUCCESS
