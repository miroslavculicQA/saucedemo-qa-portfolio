# Test Design Techniques (CTFL Notes)

This document summarizes the main test design techniques used in the SauceDemo QA portfolio project and shows how they were applied in practice.

## Equivalence Partitioning (EP)
Equivalence Partitioning was used for input validation scenarios by dividing input conditions into meaningful groups such as:
- valid input
- missing required input
- invalid input

### Applied examples
- Login:
  - valid credentials
  - invalid credentials
  - missing username
  - missing password
- Checkout: Your Information
  - valid first name / last name / postal code
  - empty first name
  - empty last name
  - empty postal code

This helped create representative negative and positive scenarios without testing every possible text combination.

## Boundary Value Analysis (BVA)
Boundary Value Analysis is typically used where numeric or length constraints exist.

In this project, explicit field length constraints were not clearly defined in the application UI, so BVA was noted as a relevant technique but was not heavily applied in the current test set.

If additional validation rules are identified later, BVA-based test cases can be added.

## Decision Tables
Decision Tables were used to model system outcomes based on combinations of input conditions.

### Example: Login Decision Table (Swag Labs)

**Conditions**
- C1: Username provided?
- C2: Password provided?
- C3: Credentials valid? *(based on demo accounts shown on the login page)*

**Actions**
- A1: Login succeeds and the Inventory page is displayed
- A2: Login is blocked; an error message is displayed and the user remains on the Login page

| Rule | C1 Username | C2 Password | C3 Valid creds | Expected Result |
|------|-------------|-------------|----------------|-----------------|
| R1   | Yes         | Yes         | Yes            | A1              |
| R2   | No          | Yes         | N/A            | A2              |
| R3   | Yes         | No          | N/A            | A2              |
| R4   | No          | No          | N/A            | A2              |
| R5   | Yes         | Yes         | No             | A2              |

### Mapping to test cases
- R1 → TC-001
- R2 → TC-002
- R3 → TC-003
- R4 → TC-004
- R5 → TC-005

The login negative and positive scenarios were derived directly from this decision table.

## State Transition (Light)
State Transition thinking was used for cart and checkout flows.

### Cart flow
- empty cart → product added → cart contains item(s) → product removed → empty cart

### Checkout flow
- cart with item(s) → Checkout: Your Information → Checkout: Overview → Checkout: Complete!
- invalid required input → error message displayed on Checkout: Your Information

### Applied examples
- Add/remove product from cart
- Start checkout with product in cart
- Checkout with valid customer information
- Complete checkout successfully
- Checkout validation with missing required fields

## Functional Scenario Design
Some test cases were designed as functional workflow scenarios based on expected user behavior through the application.

### Applied examples
- Inventory page displays product list
- Added product is displayed on the Cart page
- Two added products are displayed on the Cart page
- Sort products by name from Z to A
- Sort products by price (low to high)
- Sort products by price (high to low)

## Notes
Test case IDs and detailed execution steps are maintained in `testcases/test-cases.csv`.
