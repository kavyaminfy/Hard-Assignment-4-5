# Assignment 4: Git Hooks & Automation 

# Objective
The objective of this assignment was to understand and implement automation and quality control within a Git-based development workflow. I aimed to integrate tools like Husky, lint-staged, Prettier, ESLint, commitlint, and GitHub Actions in order to enforce code standards, validate commit messages, and introduce continuous integration into the version control process.

# Tools and Technologies I Used
Husky: I used Husky to manage Git hooks, allowing me to automate checks such as linting and commit message validation before a commit is finalized.

lint-staged: This tool helped me run linters only on staged files, ensuring that only relevant files were checked and formatted before committing.

ESLint: I used ESLint as a static code analysis tool to identify and fix issues in my JavaScript code.

Prettier: I configured Prettier to format my code consistently across the project, reducing formatting-related issues.

commitlint: To ensure meaningful and properly structured commit messages, I used commitlint based on conventional commit rules.

# GitHub Actions

I set up a simple GitHub Actions workflow to run automated checks (such as linting) whenever code was pushed or a pull request was made.

My Thoughts on Git Workflow Automation
Implementing automation in my Git workflow significantly improved my development process. With pre-commit hooks and commit message validation in place, I was able to catch issues early and maintain a clean and readable commit history. Automation ensured that my code met defined quality standards before it was even pushed to the repository.

Using GitHub Actions for continuous integration added another layer of reliability. It allowed me to automatically run checks on every push and pull request, reducing the risk of introducing errors into the main branch.

Overall, I found that integrating these tools not only improved the quality and consistency of my code but also encouraged a more disciplined and professional workflow. It made collaboration smoother and debugging easier, and it gave me a clearer understanding of how modern software teams maintain code quality at scale.




