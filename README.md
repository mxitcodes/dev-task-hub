# DevTask Hub

[![Pipeline Status](https://img.shields.io/badge/pipeline-passing-brightgreen.svg)](#)
[![Release](https://img.shields.io/badge/release-v1.0.0-blue.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#)

> **DevTask Hub** (main production) serves as the primary operational dashboard and CI/CD automation pipeline for agile software delivery.

---

## 👨‍💻 Student & Project Information

- **Student Name:** Man Patel
- **Enrollment Number:** `202403103510057`
- **Username / Handle:** `mxitcodes`
- **Project Name:** DevTask Hub
- **Release Version:** `v1.0.0`

---

## 🚀 Project Overview & Architecture

DevTask Hub provides development teams with a clean, responsive Kanban dashboard to track tasks across development milestones.

```
dev-task-hub/
├── .gitignore          # Excludes build artifacts and dependencies
├── .gitlab-ci.yml      # CI/CD multi-stage automation pipeline
├── README.md           # Project documentation and setup guide
├── index.html          # DevTask Hub interactive web application
└── test.js             # Unit test validation suite using Node.js assert
```

### Key Technical Highlights
- **Zero-Dependency Frontend:** Built entirely using modern HTML5, CSS3 Glassmorphism UI, and vanilla JavaScript.
- **Robust Input Validation:** Reusable validation logic ensures tasks meet strict data integrity requirements before addition.
- **Automated CI/CD Pipeline:** Multi-stage GitLab CI pipeline executing automated builds and unit test verification.
- **Full Git Lifecycle:** Strict feature branching, merge conflict simulation and resolution, issue tracking with closing keywords (`Closes #1`), and release tagging.

---

## 📋 Implementation Phases

### Phase 1: Setup & Local Git
1. Configure SSH key pair (`ed25519`) for secure GitLab repository communication.
2. Create remote project `dev-task-hub` on GitLab.
3. Initialize local repository on branch `main`, add `.gitignore` and `README.md`, commit and push to remote.

### Phase 2: Branching & Merge Conflicts
1. Create and switch to feature branch:
   ```bash
   git checkout -b feature/app-ui
   ```
2. Develop core code artifacts: `index.html` (interactive UI) and `test.js` (test suite).
3. Simulate concurrent development resulting in a merge conflict on `main`.
4. Resolve merge conflict manually, stage changes, and commit the resolved state.

### Phase 3: Issues, MRs & Tags
1. Create 3 GitLab Issues assigned to Milestone `v1.0.0` on the Project Board:
   - **Issue #1:** Setup DevTask Hub UI and Core Dashboard
   - **Issue #2:** Implement Task Validation and Unit Test Suite
   - **Issue #3:** Configure CI/CD Build and Automated Testing Pipeline
2. Open a Merge Request (MR) from `feature/app-ui` into `main` with resolution tag `Closes #1`.
3. Review and merge the MR into `main`.
4. Tag release:
   ```bash
   git tag -a v1.0.0 -m "Release v1.0.0"
   git push origin v1.0.0
   ```

### Phase 4: CI/CD Pipeline
1. Add `.gitlab-ci.yml` defining `build` and `test` stages.
2. Build Stage: Generates production distribution directory (`dist/`) with artifacts.
3. Test Stage: Runs `node test.js` inside `node:18-alpine` runner container.
4. Verify pipeline execution and green check status on GitLab Runner.

---

## 🧪 Local Testing & Verification

### Running the Test Suite
Ensure Node.js is installed, then run:
```bash
node test.js
```
Expected output:
```
Tests Passed!
```

### Running the DevTask Hub Web App
Open `index.html` in any modern web browser or serve locally:
```bash
npx serve .
```

---

## 📜 License
This project is open-source and available under the [MIT License](LICENSE).
