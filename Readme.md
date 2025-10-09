# 🚀 CI/CD Pipeline using GitHub Actions (Spring Boot Project)

This repository demonstrates how to set up a **Continuous Integration (CI)** and **Continuous Deployment (CD)** pipeline for a **Spring Boot** application using **GitHub Actions**.  
It automatically builds and tests your project whenever code is pushed to the `main` branch.

---

## 🧠 Overview

This project focuses on automating the build and test process of a Spring Boot application using GitHub Actions.  
It ensures that every new commit is verified through automated workflows — providing reliability and consistency in development.

---

## ⚙️ Workflow Details

### **Trigger**
The pipeline runs automatically on every push to the `main` branch:
```yaml
on:
  push:
    branches: [ main ]
```

### **Jobs**
The pipeline consists of two main jobs:

#### 🏗️ **1. Build Job**
- Runs on `ubuntu-latest`
- Checks out the repository
- Sets up **Java 17**
- Builds the project using Maven

```yaml
- name: Build with Maven
  run: mvn -B package --file pom.xml
```

#### 🧪 **2. Test Job**
- Depends on the **Build Job**
- Runs the Maven test suite to ensure everything works correctly

```yaml
- name: Run tests
  run: mvn test
```

---

## 📂 Folder Structure

```
.
├── .github/
│   └── workflows/
│       └── ci-cd.yml
├── src/
│   ├── main/
│   └── test/
├── pom.xml
└── README.md
```

---

## 🛠️ Technologies Used

- **Spring Boot** – Java-based web framework
- **Maven** – Build automation tool
- **GitHub Actions** – CI/CD automation platform
- **Java 17 (Temurin)** – Runtime environment

---

## 🚦 How It Works

1. Push code to the `main` branch.
2. GitHub Actions triggers the workflow.
3. The pipeline:
    - Builds the project (`mvn package`)
    - Runs the tests (`mvn test`)
4. Results are displayed directly in the **Actions** tab on GitHub.

---

## ✅ Benefits

- Automated builds and tests
- Detects issues early
- Saves developer time
- Improves code quality and reliability

---

## 📸 Example Workflow Output

You can view the build and test results in the **Actions** tab of your repository.  
Each job will show logs for easy debugging and monitoring.



---

## 🧑‍💻 Author

**Tornov Dutta**  
💼 *Aspiring Software Engineer | Java & Spring Boot Developer*  
📧 [torno@gmail.com](mailto:shariqsd2003@gmail.com)
