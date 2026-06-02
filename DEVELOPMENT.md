# Development Guide

This document contains contributor and release workflow docs for mindcode-tools.

## Local Development

### Prerequisites

* Node.js 20+
* npm
* VS Code

### Install

```bash
npm ci
```

### Build and checks

```bash
npm run package
```

This runs type-checking, linting, and production bundling.

### Run tests

```bash
npm test
```

### Watch mode

```bash
npm run watch
```

## Publish To Marketplace

This repository includes a GitHub Actions workflow at [.github/workflows/publish.yml](.github/workflows/publish.yml) so publishing does not require running `vsce` locally.

### 1. Create a Marketplace personal access token

Create the token in Azure DevOps:

* Go to [https://dev.azure.com](https://dev.azure.com)
* Open User settings -> Personal access tokens
* Create a new token with Marketplace publish/manage permissions
* Copy the token value once when it is shown

### 2. Add the token to GitHub

In your GitHub repository:

* Settings -> Secrets and variables -> Actions
* Create a new repository secret named `VSCE_PAT`
* Paste the Azure DevOps token value

### 3. Publish from GitHub

Option A: Manual publish

* Open Actions -> Publish VS Code Extension
* Click Run workflow
* Choose `version_bump`: `none`, `patch`, `minor`, or `major`

Option B: Tag publish

* Push a tag like `v0.1.1`
* The workflow publishes the version already present in [package.json](package.json)

### Notes

* The `publisher` in [package.json](package.json) must match your Marketplace publisher ID.
* If you use tag publishing, bump [package.json](package.json) first, then tag that commit.
* For tag publishing, ensure the tag points at the commit containing the intended version.
