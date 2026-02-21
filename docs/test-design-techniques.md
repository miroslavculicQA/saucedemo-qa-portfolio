# Test Design Techniques (CTFL Notes)

## Equivalence Partitioning (EP)
Use EP for input fields (e.g., empty vs non-empty values; valid vs invalid formats).

## Boundary Value Analysis (BVA)
Apply BVA where numeric/length constraints exist. If constraints are unknown, document exploratory findings and adapt.

## Decision Tables
Use for login outcomes based on combinations of username/password validity (valid/invalid/empty).

## State Transition (Light)
Use for cart and checkout:
- Cart: empty → has items → empty
- Checkout: step 1 → step 2 → complete; also invalid input → error state
