# Devops---2026

ViteJS "Hello World" application with CI/CD pipeline.

## Features

- ⚡️ ViteJS for fast development and builds
- 🔍 ESLint for code linting
- 💅 Prettier for code formatting
- 🔒 Snyk for security vulnerability scanning
- 🚀 GitHub Actions CI/CD pipeline

## Getting Started

### Prerequisites

- Node.js 20 or higher
- npm

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

### Build

```bash
npm run build
```

### Linting

```bash
npm run lint
```

### Formatting

```bash
# Check formatting
npm run format:check

# Fix formatting
npm run format
```

## CI/CD Pipeline

The project includes a GitHub Actions workflow that runs on every push and pull request to the main/master branch.

### Pipeline Steps (in order):

1. **Lint** - Checks code quality with ESLint
2. **Format** - Validates code formatting with Prettier
3. **Snyk** - Scans for security vulnerabilities
4. **Build** - Builds the application with Vite

### Setting up Snyk

To enable Snyk security scanning in GitHub Actions:

1. Sign up for a free account at [Snyk.io](https://snyk.io/)
2. Get your Snyk API token from your account settings
3. Add the token as a GitHub secret named `SNYK_TOKEN`:
   - Go to your repository Settings → Secrets and variables → Actions
   - Click "New repository secret"
   - Name: `SNYK_TOKEN`
   - Value: Your Snyk API token

## Project Structure

```
.
├── .github/
│   └── workflows/
│       └── ci.yml          # CI/CD pipeline configuration
├── public/                 # Static assets
├── src/                    # Source code
│   ├── main.js            # Application entry point
│   ├── counter.js         # Counter component
│   └── style.css          # Styles
├── index.html             # HTML template
├── eslint.config.js       # ESLint configuration
├── .prettierrc            # Prettier configuration
└── package.json           # Project dependencies and scripts
```

## License

This project is open source and available under the MIT License.
