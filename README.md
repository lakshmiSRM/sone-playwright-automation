# sone-playwright-automation
Automated end-to-end test suite for the Sone web application using Microsoft Playwright. This repository contains modular, reusable test scripts built with TypeScript/JavaScript, following the Page Object Model (POM) design pattern to ensure scalability and maintainability.

# 🧪 Sone Playwright Automation

Automated **end-to-end testing framework** for the **Sone Web Application**, built using **Microsoft Playwright**.  
This project ensures faster regression cycles, improved test reliability, and seamless CI/CD integration.

---

## 🚀 Project Overview

The Sone Playwright automation suite validates key functional workflows of the web application.  
It supports **cross-browser**, **API**, and **UI automation** with environment-based configurations and detailed reporting.

---

## 🧰 Tech Stack

- **Automation Tool:** Playwright  
- **Language:** TypeScript (or JavaScript)  
- **Test Runner:** Playwright Test / Jest  
- **Reporting:** Allure / HTML Reporter  
- **CI/CD:** Jenkins / GitHub Actions  
- **Version Control:** Git  

---

## 🏗️ Project Structure
sone-playwright-automation/
│
├── tests/ # Test specs organized by feature/module
│ ├── login.spec.ts
│ ├── userManagement.spec.ts
│ └── auditFlow.spec.ts
│
├── pages/ # Page Object Model classes
│ ├── LoginPage.ts
│ ├── DashboardPage.ts
│ └── AuditPage.ts
│
├── utils/ # Utility functions and helpers
│ ├── testData.ts
│ └── environment.ts
│
├── config/ # Environment & Playwright config files
│ ├── playwright.config.ts
│ └── env.qa.json
│
├── reports/ # HTML / Allure test reports
├── package.json
├── README.md
└── tsconfig.json


---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/sone-playwright-automation.git
cd sone-playwright-automation
2️⃣ Install Dependencies
npm install

3️⃣ Run Tests
Run all tests in default browser (Chromium):
npx playwright test

Run in specific browser:
npx playwright test --project=firefox

Run headed (visible browser mode):
npx playwright test --headed

📊 Reports
Generate and View Allure Report
npx allure generate allure-results --clean -o allure-report
npx allure open allure-report


Or for HTML report:

npx playwright show-report

🔄 Continuous Integration (CI)

This repo supports GitHub Actions / Jenkins pipelines for continuous testing.
Sample workflow: .github/workflows/playwright.yml

name: Playwright Tests
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
      - run: npm ci
      - run: npx playwright install --with-deps
      - run: npx playwright test

✅ Key Highlights

🔹 Modular design with Page Object Model (POM)

🔹 Supports multi-environment testing

🔹 Video, trace, and screenshot capture on failures

🔹 Parallel execution and cross-browser support

🔹 Seamless CI/CD integration

👨‍💻 Contributors

Lakshmi Narayanan P
Automation Architech Engineer | Playwright | JavaScript | Node.js
