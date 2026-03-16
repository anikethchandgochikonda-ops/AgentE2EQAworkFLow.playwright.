# End-to-End QA Workflow with Natural Language

## Workflow Overview
This prompt guides you through a complete 7-step QA workflow using MCP servers and AI agents to go from user story to committed automated test scripts.

---

## 🧾 STEP 1: Read User Story

**Prompt:**
I need to start a new testing workflow. Please read the user story from the file: user-stories/SCRUM-101-ecommerce-checkout.md

Summarize the key requirements, acceptance criteria, and testing scope.

**Expected Output:**
- Summary of the user story
- List of acceptance criteria
- Application URL and test credentials
- Key features to test

---

## 🧾 STEP 2: Create Test Plan

**Prompt:**
Based on the user story SCRUM-101 that we just reviewed, use the playwright-test-planner agent to:

1. Read the application URL and test credentials from the user story  
2. Explore the application and understand all workflows mentioned in the acceptance criteria  
3. Create a comprehensive test plan that covers all acceptance criteria including:  
   - Happy path scenarios  
   - Negative path scenarios  
   - Edge cases  
   - Data validation checks  

**Expected Output:**
- Detailed test plan document
- Mapping of acceptance criteria to test cases
- Coverage matrix

---

## 🧾 STEP 3: Manual Testing

**Prompt:**
Run exploratory and manual tests against the application using the acceptance criteria from STEP 1.

**Expected Output:**
- List of manual test cases executed  
- Defect log with reproduction steps  
- Confirmation of coverage against acceptance criteria  
- Screenshots/logs for defects  

---

## 🧾 STEP 4: Generate Automation Scripts

**Prompt:**
Using the manual test cases and acceptance criteria, generate Playwright automation scripts.

**Expected Output:**
- Playwright test scripts for checkout workflow  
- Organized folder structure under `tests/saucedemo-checkout/`  
- Notes on assumptions or skipped scenarios  

---

## 🧾 STEP 5: Execute and Heal Tests

**Prompt:**
Run all automation scripts from `tests/saucedemo-checkout/`. Use the playwright-test-healer agent to identify and auto-heal any failing tests. Re-run tests until all are stable and passing. Document healing activities.

**Expected Output:**
- Stable, passing test suite  
- Healing activity log  
- Updated scripts with fixes  

---

## 🧾 STEP 6: Create Test Report

**Prompt:**
Create a comprehensive test execution report at: `test-results/SCRUM-101-checkout-test-report.md`

Compile results from Step 3 (manual testing), Step 4 (script generation), and Step 5 (execution and healing). Include PASS/FAIL status, healing summary, defects log, and test coverage analysis.

**Expected Output:**
- Consolidated test report  
- PASS/FAIL summary  
- Defects log  
- Coverage analysis  

---

## 🧾 STEP 7: Commit to Git

**Git Repoistory UrL:**https://github.com/anikethchandgochikonda-ops/AgentE2EQAworkFLow.playwright.

**Prompt:**
Use the GitHub MCP agent to commit all new files with a descriptive message and push to the repository.

Git Repoistory UrL:https://github.com/anikethchandgochikonda-ops/AgentE2EQAworkFLow.playwright.

**Expected Output:**
- Git commit with descriptive message  
- Updated repository with test plan, scripts, and reports  

---

## ✅ Workflow Execution
Execute this complete workflow and provide status updates after each step.
