# Test Plan – Swag Labs (SauceDemo)

**Project:** SauceDemo QA Portfolio  
**Version:** 1.0  
**Author:** Miroslav Ćulić  
**Date:** 21.02.2026.

## 1. Objective
Verify the core user flows of the Swag Labs (SauceDemo) web application and document findings using CTFL-aligned testing practices (planning, test design, execution, defect reporting, summary).

## 2. Test Basis
- Application behavior observed through the UI (screens, navigation, messages).
- Common expectations for an e-commerce flow (login → browse products → cart → checkout → confirmation).

## 3. Test Item
Swag Labs (SauceDemo) web application:
- Login / Logout
- Inventory (product list, product details, sorting)
- Cart
- Checkout

## 4. In Scope
- Functional UI testing for MVP flows
- Negative testing for form validation and authentication
- Exploratory testing sessions (time-boxed)
- Basic compatibility checks (Chrome + one additional browser)

## 5. Out of Scope
- API testing
- Performance/load testing (beyond basic observations)
- Security testing (beyond normal user behavior checks)
- Deep accessibility audit (optional lightweight checklist only)

## 6. Risks and Priorities (Risk-Based Testing)
See: `docs/risk-assessment.md`

## 7. Test Approach
### 7.1 Test Types
- Functional testing
- Negative testing
- Exploratory testing (time-boxed)
- Basic cross-browser checks

### 7.2 Test Design Techniques (CTFL)
- Equivalence Partitioning (EP)
- Boundary Value Analysis (BVA)
- Decision Tables (e.g., login combinations)
- State Transition (lightweight) for cart/checkout states

See: `docs/test-design-techniques.md`

## 8. Test Environment
- OS: Windows
- Browsers: Chrome (primary), Firefox or Edge (secondary)
- Resolution: Desktop + one mobile viewport (DevTools sanity)

## 9. Test Data
- Use credentials provided on the login page (demo test accounts).
- Checkout data: valid and invalid inputs for required fields (First Name, Last Name, Postal Code).

## 10. Entry Criteria
- Application is accessible
- Test data available (login credentials visible in app)
- MVP test cases drafted

## 11. Exit Criteria
- 100% of planned MVP test cases executed
- All Critical/High issues documented with clear reproduction steps and evidence
- Test Summary Report completed with execution metrics and conclusions

## 12. Deliverables
- Test Plan
- Test Cases (CSV/MD)
- Defect Reports (GitHub Issues + evidence)
- Test Summary Report

## 13. Defect Management & Reporting
- Defects will be tracked as GitHub Issues using the bug report template.
- Evidence (screenshots/videos) stored under `evidence/bug-###/`.

## 14. Roles and Responsibilities
- QA Engineer (planning/execution/reporting): Miroslav Ćulić

## 15. Schedule (High-Level)
- Day 1: Test Plan + test design + initial test cases
- Day 2: Execution + defect reporting
- Day 3: Retest (if applicable) + summary report

## 16. Assumptions and Constraints
- No formal requirements document is provided; test basis is derived from UI behavior and common e-commerce expectations.
- Demo environment: issues may be intentional and not fixed.
