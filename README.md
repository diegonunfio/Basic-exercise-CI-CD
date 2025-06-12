# GitHub Actions CI/CD Practice ⚙️

This project demonstrates how to implement **Continuous Integration (CI)** and **Continuous Deployment (CD)** workflows using **GitHub Actions**. It automates linting, testing, building, and deploying a Node.js-based application, providing a solid foundation for real-world DevOps practices.

## Workflows Overview 🚀

The following GitHub Actions workflows are defined to ensure code quality and simulate deployment steps:

### `Handle Issues`
Triggered on GitHub issue activity. Outputs the full event payload to help with automation or debugging.

```yaml
on: issues
```

### `Deployment 2` `(On Any Push)`
Triggered on every push to any branch. Executes a three-phase job flow:

### 1. Lint

- Installs dependencies

- Runs npm run lint

### 2. Test

- Runs after lint passes

- Executes npm run test

### 3. Deploy

- Depends on successful testing

- Installs dependencies, lints, tests, builds the project with npm run build, <br> and simulates deployment using echo

### `Deployment` 
Triggered only on push to the main branch. Runs lint, test, build, and deploy in a single job <br> intended to simulate a production-like deployment pipeline.

### `Technologies Used` 
- GitHub Actions (for CI/CD automation)

- Node.js & npm

- ESLint (npm run lint)

- Jest or similar (npm run test)

- TypeScript compiler or bundler (npm run build)
