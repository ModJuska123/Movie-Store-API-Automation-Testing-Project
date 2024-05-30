# Movie-Store-API-Automation-Testing-Project

Welcome to the My Node.js Application! This project is designed as a simple Node.js application with implemented GitHub workflow, tests developed in Postman, Newman running a collection. Below you'll find instructions for setting up and running the project, using Postman for API testing, Newman for automated tests, and details on the GitHub workflow for CI/CD.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Using Postman](#using-postman)

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (version 18.x or later)
- [npm](https://www.npmjs.com/get-npm) (Node Package Manager)
- [Postman](https://www.postman.com/) (for API testing)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/your-username/your-repo-name.git
    ```

2. Navigate to the project directory:

    ```sh
    cd your-repo-name
    ```

3. Install the dependencies:

    ```sh
    npm install
    ```

## Running the Application

To start the application, run:

```sh
npm start

```markdown
## Automated Testing with Newman

Newman allows you to run Postman collections from the command line. Follow these steps to run automated tests:

1. Install Newman globally:

    ```sh
    npm install -g newman
    ```

2. Run the Postman collection with Newman:

    ```sh
    newman run postman/collection.json -e postman/environment.json
    ```

## GitHub Workflow

This project uses GitHub Actions for CI/CD. The workflow is defined in `.github/workflows/node.js.yml`. Here’s a brief overview:

- **Node.js CI**: This workflow runs on push and pull request events to the `main` branch.
- It installs dependencies, runs tests, and lints the code.

Example of the GitHub Actions workflow file:

```yaml
name: Node.js CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [18.x]

    steps:
    - uses: actions/checkout@v3
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}
    - run: npm install
    - run: npm test
    - run: npm run lint

