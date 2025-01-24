PR Rules and Practices
1. Branch Naming Rules
Use a consistent branch naming convention. Examples:
feature/branch-name for new features.
bugfix/branch-name for bug fixes.
hotfix/branch-name for urgent fixes.
docs/branch-name for documentation changes.
Benefits:
Makes it easier to understand the purpose of a branch.
Keeps the repository organized.
2. Pull Request Description
Every PR should have a clear and concise description, including:
What the PR does (summary).
Why the change is necessary.
Steps to test the changes.
Screenshots, if applicable.
Template Example:
You can create a pull request template by adding a .github/PULL_REQUEST_TEMPLATE.md file:

markdown
Copy
Edit
### Description
<!-- Briefly describe what this PR does -->

### Related Issue(s)
<!-- Link to the related issue(s) (e.g., Fixes #123) -->

### Testing Instructions
<!-- Describe the steps to test this PR -->

### Screenshots
<!-- Add screenshots, if applicable -->

### Checklist
- [ ] Code follows the style guidelines.
- [ ] Relevant documentation is updated.
- [ ] Tests are added/updated, if applicable.
3. Code Review Rules
All PRs must be reviewed and approved by at least one or more collaborators before merging.
Use GitHub's Required Approvals in branch protection rules to enforce this.
4. CI/CD and Status Checks
Ensure all Continuous Integration/Continuous Deployment (CI/CD) checks pass before merging.
Examples of checks:
Build must succeed.
Tests must pass.
Linting (e.g., ESLint or Prettier) must be successful.
How to Enable:
Go to Settings > Branches > Branch protection rules.
Check Require status checks to pass before merging and select the checks to enforce.
5. Small and Focused PRs
PRs should focus on a single feature, bug fix, or change.
Avoid combining unrelated changes in one PR.
Benefits:
Easier to review.
Reduces risk of introducing bugs.
6. Use Draft PRs for Work-in-Progress
Use GitHub’s Draft Pull Requests to indicate that a PR is not ready for review yet.
Convert it to a regular PR once it's complete.
7. No Direct Merges to Protected Branches
All changes to key branches (e.g., main, master, develop) must go through a PR and not be pushed directly.
8. Conflict Resolution
The author of the PR is responsible for resolving merge conflicts before the PR is reviewed or merged.
9. Testing
Include unit tests, integration tests, or other necessary tests for new features or changes.
Ensure existing tests pass.
10. Documentation
Update relevant documentation (e.g., README, API docs) if changes affect the public interface or functionality.
How to Enforce These Rules
Use Branch Protection Rules:

Navigate to Settings > Branches > Add rule.
Configure rules such as:
Require pull requests before merging.
Require approvals.
Require status checks to pass.
PR Templates:

Add .github/PULL_REQUEST_TEMPLATE.md to standardize PR descriptions.
Automated Checks:

Integrate CI/CD tools (e.g., GitHub Actions, CircleCI, Travis CI) to automate checks like testing and linting.
Code Ownership:

Use a CODEOWNERS file to specify who must review PRs for certain parts of the codebase.
