# Movie-Store-API-Automation-Testing-Project

Welcome to the My Node.js Application! This project is designed as a simple Node.js application with implemented GitHub workflow, tests developed in Postman, Newman running a collection. Below you'll find instructions for setting up and running the project, using Postman for API testing, Newman for automated tests, and details on the GitHub workflow for CI/CD.

Table of Contents
Installation
Running the Application
Using Postman
Installation
Clone the repository:

git clone https://github.com/ModJuska123/Movie-Store-API-Automation-Testing-Project

Navigate to the project directory:

cd your-repo-name

Install the dependencies:

npm install -y

Running the Application
To start application:

npm run dev

Testing the application:

npm run test

GitHub Workflow
This project uses GitHub Actions for CI/CD. The workflow is defined in .github/workflows/node.js.yml. Here’s a brief overview:

Node.js CI: This workflow runs on push and pull request events to the main branch.
It installs dependencies, runs tests, and lints the code.
