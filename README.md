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

# Assignment 5: Collaborative Project with Advanced Git Techniques 

# Objective
The objective of this assignment is to simulate a real-world development scenario using advanced Git techniques. The goal is to implement a collaborative Git workflow while using various advanced operations to manage development, including choosing a branching strategy, setting up Git hooks, conducting code reviews, and utilizing version control tools to maintain a clean codebase.

# Branching Strategy
The assignment requires me to choose and implement a branching strategy for the project. I decided to use GitHub Flow, which is suitable for continuous deployment models. In this workflow, I create feature branches from the main branch and merge them back into the main branch after code review and approval. To ensure the stability of the project, I protect the main branch and require pull requests for changes.

Protected Branches: I configure the main branch as a protected branch in GitHub, preventing direct commits and ensuring that all changes require a pull request for review and approval.

Code Owners: To maintain high code quality, I designate specific team members as code owners for different parts of the codebase, ensuring that changes to those parts are reviewed by the right person.


# Advanced Git Techniques

# Interactive Rebase
I use interactive rebase to clean up the commit history before merging a feature branch into the main branch. This operation allows me to rewrite commit history by squashing multiple commits into one or reordering them, ensuring a more readable and linear history.

# Cherry-pick
The cherry-pick command enables me to apply specific commits from one branch to another. For example, if a critical fix is made in a feature branch, I can cherry-pick that commit and apply it directly to the main branch, without needing to merge the entire feature branch.

# Git Bisect
To simulate the introduction of a bug, I use git bisect to identify the commit responsible for the issue. This command helps narrow down the commit range by performing a binary search, allowing me to quickly find the problematic commit.

# Reflog Recovery
If I make a mistake, such as deleting a branch or losing work, I use git reflog to recover lost commits. The reflog records all changes to the HEAD, even if the commits are no longer part of the current branch, allowing me to restore work and continue development without losing progress.

# Pull Request Templates and Code Reviews
To ensure consistency and clarity in code changes, I implement pull request templates. These templates guide me to include essential information in each pull request, such as a description of the changes and any testing performed. I also participate in code reviews to ensure that all changes are thoroughly checked for quality and correctness before being merged.

# Release and Versioning
Once all features are implemented, I create a release and apply versioning using Git tags. Versioning helps me track different stages of the project, and tagging specific commits allows me to mark important milestones or stable releases in the development cycle.

