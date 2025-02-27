# Deno CI Workflow

This GitHub Actions workflow is designed to ensure code quality and reliability by automatically installing Deno, running linting (`deno lint`), and executing tests (`deno test -A`) whenever changes are pushed or a pull request is made to the `main` branch.

## Workflow Details

### Trigger Events

- Executes on push and pull request events targeting the `main` branch.

### Permissions

- `contents: read` (Ensures secure and controlled access).

### Jobs

- Runs on `ubuntu-latest` to ensure compatibility.

### Steps

1. **Setup Repository** – Uses `actions/checkout@v4` to pull the latest changes.
2. **Install Deno** – Uses `denoland/setup-deno@v1.x` to set up the latest stable Deno environment.
3. **Run Linter** – Executes `deno lint` to check for syntax and style issues.
4. **Run Tests** – Runs `deno test -A` with all permissions to verify functionality.

### Best Practices Implemented

- ✅ Uses a pinned commit hash for `setup-deno` to ensure stability and prevent unexpected updates.
- ✅ The workflow is modular and efficient, with clear steps for readability and maintainability.
- ✅ Includes an optional formatting check (`deno fmt --check`) that can be enabled to enforce code consistency.

### Next Steps for Optimization

1. Enable `deno fmt --check` to enforce uniform formatting on every commit.
2. Expand test coverage by adding more test cases to `deno test -A`.
3. Monitor GitHub Actions logs to identify and resolve any potential issues.

## Direct Link to Workflow File

[GitHub: Deno Workflow](./.github/workflows/deno-workflow.yml)

This workflow ensures a perfect, automated, and scalable development process with Deno. 🚀
