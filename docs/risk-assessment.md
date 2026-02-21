# Risk Assessment – Swag Labs (SauceDemo)

| Risk ID | Area     | Risk Description                                  | Impact | Likelihood | Priority | Notes |
|--------:|----------|---------------------------------------------------|:------:|:----------:|:--------:|------|
| R1      | Login    | Users cannot log in / log out                     | High   | Medium     | P0       | Blocks all testing beyond login |
| R2      | Cart     | Add/remove items fails or cart count is wrong     | High   | Medium     | P0       | Breaks purchase flow |
| R3      | Checkout | Required-field validation missing/incorrect       | High   | Medium     | P0       | Leads to invalid orders/UX issues |
| R4      | Inventory| Sorting or product details inconsistent           | Medium | Medium     | P1       | Affects browsing experience |
| R5      | UX/Errors| Error messages unclear or not actionable          | Medium | Medium     | P2       | Affects usability and support load |
