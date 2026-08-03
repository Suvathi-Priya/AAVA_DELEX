# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 corresponding execution log entries derived directly from the uploaded user story, test plan, and test log documents.

Document completeness and integrity are acceptable for analysis: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs and explicit AC mappings; each test log contains execution results per test case; no separate defect log documents were uploaded, so defect details were derived from defect references embedded in the execution logs; missing standalone defect logs are noted as NULL and do not prevent reporting.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC3 | Acceptance criterion requires upcoming renewal date, renewal amount, and auto-renewal status in portal; no testcase explicitly validates all required fields in a single end-to-end view. | Partially Covered |
| SCM-010 | AC4 | Audit logging requirement includes subscription ID, renewal date, payment method used, renewal amount, and timestamp; testcases validate subscription ID and renewal date only. Payment method used, renewal amount, and timestamp are not covered. | Partially Covered |
| SCM-010 | AC5 | Requirement states retry up to 3 times before suspension and customer notification; testcases cover retry initiation, suspension after 3 failed retries, and notification, but do not explicitly validate all three retry attempts. | Partially Covered |
| SCM-011 | AC1 | Acceptance criterion requires administrators or customers to initiate cancellation; testcases cover administrator initiation only. Customer-initiated cancellation scenario missing. | Partially Covered |
| SCM-011 | AC3 | Acceptance criterion requires cancellation status and effective end date in portal; testcases validate status visibility and updates, but effective end date display is not explicitly covered. | Partially Covered |
| SCM-011 | AC5 | Requirement includes prorated refund calculation subject to finance team review before refund issuance; testcases cover calculation accuracy, but finance review workflow and pre-issuance control are not explicitly validated. | Partially Covered |
| SCM-012 | AC4 | Audit logging requirement includes previous plan, new plan, prorated amount, effective date, and timestamp; testcases validate previous/new plan and timestamp only. Prorated amount and effective date are not explicitly covered. | Partially Covered |
| SCM-013 | AC3 | Acceptance criterion requires team members to view assignment status and expiration in portal; testcases validate assignment status and real-time update behavior, but expiration display is not explicitly covered. | Partially Covered |
| SCM-013 | AC5 | Requirement includes prevention of assignment at license limit and administrator notification; testcases validate assignment blocking and count behavior, but administrator notification is not explicitly covered. | Partially Covered |
| SCM-014 | AC4 | Audit logging requirement includes subscription ID, refund amount, reason, approver if applicable, and timestamp; testcases validate subscription ID, refund amount, reason, and timestamp, but approver capture is not explicitly covered. | Partially Covered |
| SCM-015 | AC2 | Acceptance criterion requires reminder notification a specified number of days before expiration; testcases validate reminder presence and expiration date content, but the timing rule for the specified lead time is not explicitly validated. | Partially Covered |
| SCM-016 | AC3 | Acceptance criterion requires active add-ons, individual charges, and total subscription cost in portal; testcases validate active add-ons and individual charges, but total subscription cost is not explicitly covered. | Partially Covered |
| SCM-016 | AC5 | Requirement includes no retroactive refund unless required by regional regulation; regional regulation exception scenario is not covered. | Partially Covered |
| SCM-017 | AC4 | Audit logging requirement includes subscription ID, old payment method reference, new payment method reference, and timestamp; testcases validate subscription ID, new reference, and timestamp, but old payment method reference is not explicitly covered. | Partially Covered |
| SCM-017 | AC5 | Requirement states payment method update must trigger an immediate retry using the new method when retry is pending; testcase validates pending retry existence only. Immediate retry using new payment method is not explicitly covered. | Partially Covered |
| SCM-018 | AC3 | Acceptance criterion requires suspension status and outstanding balance in portal; testcases validate suspension status and post-reinstatement clearance, but outstanding balance display is not explicitly covered. | Partially Covered |
| SCM-018 | AC5 | Requirement includes restoration of full access within a defined SLA; testcases validate payment prerequisite and reinstatement blocking logic, but SLA restoration timing is not explicitly covered. | Partially Covered |
| SCM-019 | AC2 | Acceptance criterion requires notification at least 30 days in advance; testcases validate notification content and duplicate prevention, but the 30-day advance timing rule is not explicitly covered. | Partially Covered |
| SCM-019 | AC4 | Audit logging requirement includes subscription ID, old price, new price, notification sent date, and timestamp; testcases validate subscription ID, notification sent date, and timestamp only. Old price and new price audit fields are not explicitly covered. | Partially Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test cases in the uploaded test plans contain explicit mappings to a single user story ID and a single acceptance criteria ID; no ambiguous or duplicate AC mappings were identified from the source documents. | SCM-010 to SCM-019 | AC1 to AC5 | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test cases in the uploaded test plans contain explicit mappings to a single user story ID and a single acceptance criteria ID; no ambiguous or duplicate AC mappings were identified from the source documents. | SCM-010 to SCM-019 | AC1 to AC5 | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 150 |
| total_testlogs | 150 |
| missing_testcases | 0 |
| missing_testlogs | 0 |
| consistency_status | Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | Reminder notification omits current plan price for annual-billed subscriptions | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | Subscription remains active state after 3rd failed retry instead of moving to suspended | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | Duplicate cancellation request accepted when subscription already pending cancellation | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | Revoking license from team member with no assignment returns generic server error instead of handled message | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | License pool count briefly shows incorrect total when revoke and reassign occur within same second | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | Refund reason field truncated to 50 characters in audit log for long free-text reasons | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | Refund request above threshold processed automatically before finance manager approval recorded | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | Conversion attempted using expired payment method instead of failing over to downgrade path | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | Audit log merges two rapid add-on actions into a single entry, losing the first action | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | International card format with alphanumeric routing details rejected as invalid | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | No audit log entry created when payment method update fails midway through processing | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | Consecutive failure counter does not reset after an intervening successful payment | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | Suspension audit log omits failed attempts that occurred in a prior billing cycle | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | Only one of several simultaneous tier price changes is detected and flagged for notification | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | Downgrade request submitted on effective date boundary is charged a penalty fee in error | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

## Conclusion

Unit test traceability and execution completeness are consistent across the uploaded artifacts, but several acceptance criteria remain only partially covered due to missing validation of timing rules, complete audit fields, portal data elements, approval controls, and exception scenarios. Remediation is required to add the identified missing test coverage and resolve the 20 logged defects before this test scope can be considered fully compliant and coverage-complete.