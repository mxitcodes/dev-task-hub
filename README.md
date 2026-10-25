# DevTask Hub

A responsive, vanilla HTML/CSS/JavaScript task dashboard created for a Git and GitLab CI/CD practical.

## Student details
- **Name:** Man Patel
- **Enrollment number:** 202403103510057
- **GitLab project:** `dev-task-hub`
- **Release tag:** `v1.0.0`

## Features
- Responsive task dashboard UI in `index.html`
- Task validation tests in `test.js`
- GitLab CI pipeline with separate `build` and `test` stages in `.gitlab-ci.yml`
- Git history includes initial setup, feature branch work, a simulated conflict-resolution merge, CI configuration, and the `v1.0.0` tag

## Run locally
Open `index.html` in a browser.

To run the tests, install Node.js and execute:
```bash
node test.js
```
Expected output: `Tests Passed!`

## GitLab CI/CD
The pipeline:
1. Copies `index.html` into `dist/` during the `build` stage and saves it as an artifact.
2. Runs `node test.js` using the `node:18-alpine` image during the `test` stage.

A GitLab Runner must be available for jobs to execute. After pushing, open **Build > Pipelines** in GitLab and confirm both jobs pass.

## GitLab project checklist (complete these on GitLab)
- Create a public project named `dev-task-hub`.
- Add your SSH public key to GitLab, then add the remote URL to this local repository.
- Push `main`, `feature/app-ui`, and the `v1.0.0` tag.
- Create a milestone and three issues; add the issues to the project board.
- Open and merge a merge request from `feature/app-ui` to `main`. Its description should include `Closes #1`.
- Capture real screenshots of the issue board, merged merge request, and successful pipeline.

> Local files and Git history do not create GitLab Issues, milestones, merge requests, or pipeline screenshots automatically. Those items must be completed and verified in your GitLab account.

## Suggested issues
1. **Build the DevTask Hub dashboard** — UI and core task workflow.
2. **Validate task input** — ensure blank task names are rejected and add automated tests.
3. **Automate build and tests** — configure and verify the GitLab CI pipeline.
