# Lab #4 – GitHub Actions Workflows


## Overview
This lab demonstrates the use of GitHub Actions to automate different workflow scenarios such as dependent jobs, environment variables and secrets, and running jobs across multiple platforms.

Three separate workflow files were created inside the `.github/workflows/` folder:

1. dependent-jobs.yml – Demonstrates job dependency using "needs" between build, test, and deploy stages.  
2. env-and-secrets.yml – Demonstrates the use of environment variables and repository secrets inside GitHub Actions.  
3. multi-platform.yml – Demonstrates running jobs in parallel across Ubuntu, Windows, and macOS environments.

---

## Repository Structure
GitHubActionsLab--Gurvansh/
 ├── .github/
 │   └── workflows/
 │        ├── dependent-jobs.yml
 │        ├── env-and-secrets.yml
 │        └── multi-platform.yml
 ├── README.md

---

## Workflows Summary

### 1. Dependent Jobs Workflow
File: dependent-jobs.yml  
Trigger: On push to main branch  
Jobs: build → test → deploy  
Demonstrates sequential execution using the "needs" keyword.

Screenshots Required:
- Diagram showing 3 jobs in sequence
- Logs for build, test, and deploy showing success messages

---

### 2. Environment and Secrets Workflow
File: env-and-secrets.yml  
Trigger: On push to main branch  
Uses environment variables and repository-level secrets.  
Demonstrates how to securely use API keys or credentials in GitHub Actions.

Screenshots Required:
- Workflow diagram showing jobs success
- GitHub → Settings → Secrets and Variables → Actions → your secret name (proof of configuration)

---

### 3. Multi-Platform Workflow
File: multi-platform.yml  
Trigger: On pull request to main branch  
Runs jobs on three OS platforms in parallel:
- ubuntu-job
- windows-job
- macos-job

Each job displays OS information and creates a text file output.

Screenshots Required:
- Diagram showing 3 jobs running in parallel
- Logs for each job:
  - Ubuntu job (uname -a)
  - Windows job (systeminfo)
  - macOS job (uname -a)

---

## Results Summary
- All three workflows executed successfully.  
- Each job completed with a "Success" status in the Actions tab.  
- Environment variables and secrets were accessed securely.  
- Multi-OS jobs ran in parallel and displayed proper outputs.

---

## Repository Link
https://github.com/Gurvansh006/GitHubActionsLab--Gurvansh

---

## Tools Used
- GitHub  
- GitHub Actions  
- YAML Workflow Configuration  
- Ubuntu, Windows, macOS Virtual Runners  


---

Notes:
- Each workflow was committed, triggered, and verified using GitHub Actions.  
- Screenshots have been attached in the submission ZIP file for evidence.  
- All jobs show successful completion in the Actions tab.
