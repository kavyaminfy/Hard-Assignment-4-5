# Assignment 4: Git Hooks & Automation 
Objective
The objective of this assignment was to implement quality controls and automation within the Git workflow. I explored Git hooks using Husky, automated code checks with lint-staged, validated commit messages with commitlint, and set up a CI pipeline using GitHub Actions.
Tasks and My Implementation
1. Repository Setup
git init
npm init -y
2. I began by creating a new Git repository and initializing a Node.js project:
npm install husky lint-staged prettier eslint commitlint @commitlint/config-conventional --save-dev
3. Configuring Husky
I enabled Husky to manage Git hooks:
npx husky install
npm set-script prepare "husky install"
npm run prepare

Pre-commit hook to run lint-staged:
npx husky add .husky/pre-commit "npx lint-staged"

4. Setting Up lint-staged and Prettier
In my package.json, I added:

"lint-staged": {
  "*.js": ["eslint --fix", "prettier --write"]
}

For Prettier configuration, I created a .prettierrc file:
{
  "semi": true,
  "singleQuote": true
}

5. Setting Up ESLint and Commitlint
I initialized ESLint using:

npx eslint --init

Then I created a commitlint.config.js file:
module.exports = {
  extends: ['@commitlint/config-conventional']
};

6. Testing the Hooks
I attempted several types of commits:

With code that failed ESLint rules

With code that was improperly formatted

With invalid commit messages

All were rejected as expected. I then fixed the issues and successfully committed, which confirmed the hooks were working correctly.

7. GitHub Actions CI Setup
I created a simple CI workflow using GitHub Actions at .github/workflows/ci.yml:
name: CI - Lint Check

on: [push, pull_request]

jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '18'
      - run: npm ci
      - run: npm run lint





