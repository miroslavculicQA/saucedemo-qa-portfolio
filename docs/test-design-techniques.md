# Test Design Techniques (CTFL Notes)

## Equivalence Partitioning (EP)
Use EP for input fields (e.g., empty vs. non-empty values; valid vs. invalid formats).

## Boundary Value Analysis (BVA)
Apply BVA where numeric/length constraints exist. If constraints are unknown, document exploratory findings and adapt.

## Decision Tables
Use decision tables to model outcomes based on combinations of conditions (e.g., login scenarios).

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

**Mapping to test cases**
- R1 → TC-001
- R2 → TC-002
- R3 → TC-003
- R4 → TC-004
- R5 → TC-005

## State Transition (Light)
Use for cart and checkout flows:
- Cart: empty → has items → empty
- Checkout: step 1 → step 2 → complete; invalid input → error state

Test case IDs are maintained in `testcases/test-cases.csv`.
