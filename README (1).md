# Home Credit LAP AI Voice Agent

## Overview
A Retell AI voice-agent prototype for conducting a **preliminary eligibility assessment** for a potential Home Credit Loan Against Property (LAP) offer of up to ₹75 lakh.

The agent screens property type, ownership, original property documents, requested amount, occupation and income mode, estimated property market value, and repayment tenure. It also checks for existing property loans and loan-transfer/EMI-reduction needs.

> **Important:** This is a preliminary screening prototype. It does not approve loans, guarantee eligibility, promise disbursal, or provide unverified interest rates or fees.

## Objectives
- Conduct a natural, polite voice conversation.
- Capture all seven eligibility checkpoints.
- Route existing property loan / transfer / EMI-reduction cases to a specialist.
- Stop the fresh-loan flow when a disqualifying condition is identified.
- Handle interruptions, out-of-order answers, and unclear responses.
- Avoid inventing rates, fees, approval decisions, or callback bookings.

## Preliminary eligibility rules
1. **Property:** Residential, commercial, and industrial properties may proceed; agricultural property is ineligible.
2. **Ownership:** Sole and joint ownership are accepted at the preliminary stage.
3. **Documents:** Original property documents must be available for verification.
4. **Loan amount:** Maximum ₹75 lakh. For requests above the cap, ask whether the customer wants to proceed with ₹75 lakh.
5. **Occupation/income:** Salaried and self-employed are accepted, but income must be received through a bank. Cash income is ineligible.
6. **Market value:** Record the estimate. No minimum market-value threshold was provided in the assignment.
7. **Tenure:** 3–15 years, inclusive.
8. **Priority routing:** Existing property loans or a transfer/EMI-reduction need are referred to a loan-transfer specialist.

## Technology
- Retell AI
- Prompt engineering and conversational AI
- Voice-agent conversation design
- Rule-based preliminary eligibility screening

## Repository contents
- `system_prompt.txt` — system prompt for the voice agent.
- `test_cases.md` — test scenarios and expected behavior.
- `test_results.md` — observed outcomes from the nine test transcripts.
- `evidence/` — optional links to recordings/transcripts, if safe to share.

## Testing
Nine recorded test conversations were reviewed. See [`test_cases.md`](test_cases.md) and [`test_results.md`](test_results.md).

## Evidence
- Retell agent/demo: [Add link if shareable]
- Recordings and transcripts: [Add a shareable folder link if appropriate]

Do not commit API keys, access tokens, private customer data, or sensitive recordings. Use synthetic test data and verify sharing permissions before publishing evidence.
