# Test Summary Report – Swag Labs (SauceDemo)

**Version:** 1.0  
**Date:** 29-03-2026  
**Test Cycle:** Defect-Focused Exploratory Testing (`problem_user`)

## 1. Summary
This test cycle focused on defect-oriented exploratory testing of the SauceDemo web application using the `problem_user` account.

The purpose of this cycle was not to repeat the full MVP execution already covered with `standard_user`, but to explore whether an alternative supported user context reveals inconsistent or broken behavior in core user flows.

The session primarily targeted inventory, cart, and checkout behavior after successful login. Multiple functional issues were identified and documented as GitHub Issues with supporting video evidence.

## 2. Scope of This Cycle
This exploratory cycle focused on:
- Login with `problem_user`
- Inventory behavior
- Cart behavior
- Checkout-related behavior affected after login and product interaction

This cycle was defect-focused and exploratory in nature. It was not intended to serve as a full regression pass of all previously executed MVP test cases.

## 3. Execution Overview
- Test approach: exploratory testing / defect-focused validation
- Test account: `problem_user`
- Environment: Chrome 145 / Windows 11 / 2560x1440
- Evidence type: video recordings stored under `evidence/bug-###/`

Login itself was successful with `problem_user`, but multiple downstream defects were observed in inventory, cart, and checkout-related flows.

## 4. Defects Overview
A total of **8 defects** were identified during this cycle and documented through GitHub Issues.

### Logged defects
- **bug-001** — Cart page becomes blank after adding affected product with `problem_user`
- **bug-002** — Cart badge count becomes inconsistent after adding affected product with `problem_user`
- **bug-003** — Inventory product thumbnails are incorrect with `problem_user`
- **bug-004** — Inventory item opens incorrect product detail page with `problem_user`
- **bug-005** — Last Name field does not accept input and typed text appears in First Name on Checkout: Your Information page with `problem_user`
- **bug-006** — Add to cart button is not clickable for multiple products on Inventory page with `problem_user`
- **bug-007** — Remove button is not functional for multiple products on Inventory page with `problem_user`
- **bug-008** — Product sorting is not applied when selecting any option on Inventory page with `problem_user`

### Defect severity overview
- Critical: 2
- High: 6
- Medium: 0
- Low: 0

## 5. Key Findings
- The `problem_user` account can log in successfully, but core post-login functionality is not reliable.
- Multiple defects were identified on the Inventory page, including incorrect thumbnails, incorrect product detail navigation, non-functional add/remove behavior for specific products, and non-functional sorting.
- Cart behavior is also affected, including inconsistent cart badge updates and a blank cart page under specific conditions.
- Checkout-related behavior is impacted by at least one confirmed input-related issue.
- The findings show that a successful login alone is not enough to confirm functional stability across supported user contexts.

## 6. Quality Assessment
Compared with the baseline MVP cycle executed with `standard_user`, the `problem_user` cycle exposed multiple severe defects in core e-commerce flows.

The most affected area in this cycle was **inventory**, followed by **cart**, with additional impact observed in **checkout**.

This confirms that the application behavior varies significantly depending on the user context used during testing, and it highlights the value of exploratory defect-focused coverage beyond the main happy path.

## 7. Go / No-Go Recommendation

**Recommendation:** No-Go for the `problem_user` user context

**Rationale:**  
Although login is successful, multiple confirmed high-severity defects affect core post-login functionality, especially inventory interaction, cart behavior, and sorting. Based on this cycle, the application cannot be considered functionally stable for the `problem_user` context.

## 8. Final Notes
This report is intentionally separated from the original MVP Manual Testing summary created for `standard_user`.

The original MVP cycle remains valid as a baseline execution report for the `standard_user` flow. This report documents a separate exploratory cycle focused specifically on defect discovery with `problem_user`.
