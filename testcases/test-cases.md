# Test Cases (Readable View)

**Source of truth:** `test-cases.csv`

This document provides a human-readable overview of manual test cases for the SauceDemo QA portfolio project. Detailed test steps, preconditions, expected results, and priorities are maintained in `test-cases.csv`.

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
- **TC-008** — Inventory page displays product list for a logged-in user
- **TC-009** — Add product to cart from the Inventory page
- **TC-010** — Remove product from cart from the Inventory page
- **TC-020** — Add two products to cart from the Inventory page
- **TC-022** — Sort products by name from Z to A
- **TC-023** — Sort products by price (low to high)
- **TC-024** — Sort products by price (high to low)

### Cart
- **TC-011** — Open cart page from the cart icon
- **TC-012** — Added product is displayed on the Cart page
- **TC-021** — Two added products are displayed on the Cart page

### Checkout
- **TC-013** — Start checkout with product in cart
- **TC-014** — Checkout with valid customer information
- **TC-015** — Checkout with empty first name
- **TC-016** — Checkout overview page displays order summary
- **TC-017** — Complete checkout successfully
- **TC-018** — Checkout with empty last name
- **TC-019** — Checkout with empty postal code

## Notes
This file is a human-readable overview. Detailed steps and expected results are maintained in `test-cases.csv`.

Login negative scenarios were derived using the Decision Table technique documented in `docs/test-design-techniques.md`.
