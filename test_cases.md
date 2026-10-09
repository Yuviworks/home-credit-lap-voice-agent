# Test Cases — Home Credit LAP AI Voice Agent

These scenarios reflect the assignment's preliminary eligibility rules.

| ID | Scenario | Test input / conditions | Expected behavior |
|---|---|---|---|
| TC01 | Fully eligible customer | No existing property loan or transfer need; residential property; sole ownership; original documents available; ₹50 lakh requested; salaried; bank income; market value ₹1 crore; 4-year tenure | Complete all seven checkpoints and provide a preliminary-qualification handoff without promising approval or a rate. |
| TC02 | Eligible residential profile | No existing loan/transfer need; residential flat; sole ownership; original documents available; ₹40 lakh; salaried with bank income; value ₹80 lakh; 10-year tenure | Complete screening and provide the preliminary handoff. |
| TC03 | Answers out of order | Customer provides market value and other later answers before all questions are asked | Retain known answers, ask only unanswered questions, and clarify ambiguous details. |
| TC04 | Agricultural property mentioned | Customer mentions agricultural and residential properties | Clarify which property will be used. If agricultural is selected, disqualify; if residential is selected, continue screening. |
| TC05 | Requested amount above cap | Customer requests ₹80 lakh and agrees to continue with ₹75 lakh | Explain the ₹75 lakh maximum, get agreement, and continue the remaining checkpoints. |
| TC06 | Cash income | Customer is salaried or self-employed but confirms income is received in cash | Explain that income must be received through a bank and end the assessment. |
| TC07 | Customer busy | Customer asks for a callback and prefers around 6–7 PM | Ask and note preferred time if supported; do not claim a callback is booked unless the system confirms it. |
| TC08 | Existing property loan | Customer confirms an existing loan against a property | Stop the fresh-loan checklist, refer to a loan-transfer specialist, and end politely. |
| TC09 | Existing EMI / unclear tenure | Customer mentions a current property EMI, or gives an unclear tenure such as “eighty years” | Clarify whether an existing loan/transfer need applies; route if appropriate. Clarify tenure and accept only 3–15 years. |

## General pass criteria
- The agent follows the stated eligibility rules.
- Disqualifying conditions stop the fresh-loan flow promptly.
- Existing property loan / transfer / EMI-reduction cases are routed appropriately.
- The agent does not invent rates, fees, minimum property value, approval, or disbursal.
- Previously supplied answers are retained and ambiguous numeric answers are clarified.
