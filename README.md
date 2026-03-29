# SauceDemo QA Portfolio (Manual → Automation Ready)

This repository documents a QA portfolio project based on the **Swag Labs (SauceDemo)** demo web application.

App under test:
https://www.saucedemo.com

## Goals
- Demonstrate ISTQB CTFL-aligned manual testing approach (test planning, test design, execution, defect reporting).
- Keep artifacts structured and automation-friendly for a later Java + Selenium implementation.

## Scope (MVP)
- Login / Logout
- Inventory (product list, product details, sorting)
- Cart (add/remove, cart contents)
- Checkout (form validation, checkout steps, order completion)

## Deliverables
- Test Plan: `docs/test-plan.md`
- Risk Assessment: `docs/risk-assessment.md`
- Test Design Notes (EP/BVA/Decision Tables, etc.): `docs/test-design-techniques.md`
- Test Cases: `testcases/test-cases.csv` (+ optional `testcases/test-cases.md`)
- Bug Reports: GitHub Issues (with evidence under `evidence/`)
- Test Summary Reports:
  - `docs/test-summary-report.md` – MVP Manual Testing (`standard_user`)
  - `docs/test-summary-report-problem-user.md` – Defect-Focused Exploratory Testing (`problem_user`)

## Current Status
- MVP manual test documentation and baseline execution were completed using `standard_user`.
- A separate defect-focused exploratory cycle was later executed using `problem_user`.
- Confirmed defects were documented as GitHub Issues with supporting evidence stored under `evidence/`.
- The next planned phase is UI test automation using Java and Selenium based on the current manual baseline.

## Planned Automation Stack
- Language: Java
- UI Automation: Selenium WebDriver
- IDE: IntelliJ IDEA

## Repository Structure
- `docs/` – testing documentation
- `testcases/` – test cases (CSV for filtering + MD for readability)
- `evidence/` – screenshots/videos per bug
- `.github/ISSUE_TEMPLATE/` – GitHub Issue forms/templates

## Notes
This is a demo system; defects may be intentional and not fixed. The purpose is to demonstrate a professional QA workflow and documentation quality.
