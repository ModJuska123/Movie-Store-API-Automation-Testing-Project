## 🎬Movie-Store-API-Automation-Testing-Project🎥

Welcome to the My Node.js Application! This project is designed as a simple Node.js application with implemented GitHub workflow, tests developed in Postman, Newman running a collection. Below you'll find instructions for setting up and running the project, using Postman for API testing, Newman for automated tests, and details on the GitHub workflow for CI/CD.

📑### Table of Contents
1. Installation
2. Running the Application
2. GitHub Workflow

🛠### 1. Installation

1.1. Clone the repository:
```
git clone https://github.com/ModJuska123/Movie-Store-API-Automation-Testing-Project
```

1.2. Navigate to the project directory:
```
cd your-repo-name
```

1.3. Install the dependencies:
```
npm install -y
```

🚀### 2. Running the Application

2.1. To start application:
```
npm run dev
```

2.2. Testing the application:
```
npm run test
```
🧪 ### 3. Using Postman

Postman is used for API testing in this project. Make sure to have Postman installed on your system to run and manage your API tests effectively.

🔄### 3. GitHub Workflow
This project uses GitHub Actions for CI/CD. The workflow is defined in .github/workflows/node.js.yml. Here’s a brief overview:

Node.js CI: This workflow runs on push and pull request events to the main branch.
It installs dependencies, runs tests, and lints the code.
