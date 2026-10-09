# Test Results — Home Credit LAP AI Voice Agent

## Summary
Nine uploaded test-call transcripts were reviewed. These statuses describe observed behavior in the transcripts, not a claim that every call was flawless.

| ID | Scenario observed | Observed result | Status | Notes |
|---|---|---|---|---|
| TC01 | Residential property; sole ownership; original documents; ₹50 lakh; salaried with bank income; value ₹1 crore; 4-year tenure | Agent gave preliminary-qualification handoff | Pass with observation | The transcript did not include the required existing-property-loan/EMI screening question. Verify this screening is present in the deployed flow. |
| TC02 | Residential flat; sole ownership; original documents; ₹40 lakh; salaried with bank income; value ₹80 lakh; 10-year tenure | Agent gave preliminary-qualification handoff | Pass with observation | The transcript did not include the existing-loan screening question. Verify deployed prompt/version. |
| TC03 | Existing-loan question answered negatively; residential flat; market value supplied early; other answers out of order | Agent clarified value after initially failing to recognize it, then completed the handoff | Partial pass | Improve extraction/memory for answers provided out of order to avoid asking customers to repeat themselves. |
| TC04 | Customer mentioned agricultural and residential property; chose residential; joint ownership; requested ₹80 lakh and accepted ₹75 lakh; bank income; 10-year tenure | Agent clarified property choice, explained agricultural exclusion and the cap, then handed off | Pass with observation | Market value was transcribed unclearly (“one curve”); the agent should confirm unclear numeric values before completing. |
| TC05 | Customer had residential and commercial property, was self-employed, and confirmed cash income; tenure was initially conflicting | Agent disqualified based on cash income and ended the assessment | Pass | Correctly applied the cash-income rule. |
| TC06 | Customer was busy and preferred a callback around 6–7 PM | Agent asked for and noted the preferred time | Pass | It did not claim a callback had been technically scheduled. |
| TC07 | Customer confirmed an existing loan against a commercial property | Agent referred the customer to a loan-transfer specialist and ended politely | Pass | Correctly stopped the fresh-loan checklist. |
| TC08 | Customer said there was no loan but an EMI was running on a residential property, then asked about a commercial property | Agent referred to a loan-transfer specialist and maintained the referral | Pass with observation | The referral followed the configured priority rule. Clarify when an EMI is mentioned if it is not clear whether it represents an existing property loan or transfer/EMI-reduction need. |
| TC09 | Customer gave answers out of order and said “eighty years” for tenure, then clarified eight years | Agent explained the 3–15-year range, clarified tenure, and gave preliminary handoff | Partial pass | The requested loan amount was transcribed ambiguously (“six five lakhs”) and was not clearly confirmed before handoff. |

## Improvements identified
1. Ensure every fresh-loan flow asks the existing-property-loan / transfer / EMI-reduction question unless already answered.
2. Improve retention of out-of-order answers, especially property market value.
3. Confirm unclear loan amounts, market values, and conflicting numeric answers before completing the assessment.
4. Clarify whether a stated EMI indicates an existing property loan or a transfer/EMI-reduction need before routing.
5. Keep the final outcome explicitly preliminary; never imply final approval.

## Status legend
- **Pass:** The main expected rule was followed.
- **Pass with observation:** The main outcome was correct, but an improvement was identified.
- **Partial pass:** The flow completed, but a material conversation-handling issue occurred.

Results are based on the uploaded text transcripts. Audio quality, latency, and speech-recognition accuracy were not independently measured.
