# Test Cases (Readable View)

**Source of truth:** `test-cases.csv`

This document provides a human-readable overview of manual test cases for the SauceDemo QA portfolio project. Detailed test steps, preconditions, and expected results are maintained in `test-cases.csv`.

## Legend
- **Priority:** P0 (highest) to P3 (lowest)
- **Test Type:** functional / negative / exploratory
- **Module:** login / inventory / cart / checkout

## Current Test Coverage

### Login / Logout / Access Control
- **TC-001** — Login with valid credentials
- **TC-002** — Login with empty username
- **TC-003** — Login with empty password
- **TC-004** — Login with empty username and password
- **TC-005** — Login with invalid credentials
- **TC-006** — Logout from the application
- **TC-007** — Access Inventory URL while logged out

### Inventory
- To be added

### Cart
- To be added

### Checkout
- To be added

## Notes
This file is a human-readable overview. Detailed steps and expected results are maintained in `test-cases.csv`.

Login negative scenarios were derived using the Decision Table technique documented in `docs/test-design-techniques.md`.
