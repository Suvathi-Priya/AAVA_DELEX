# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 executed test log entries derived from the uploaded user story, test plan, and test log documents.

Document completeness is acceptable for the analyzed scope: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs mapped to acceptance criteria; each test log contains execution status per test case; no standalone defect log documents were provided, so defect details were derived from defect references embedded in the test log files. Overall coverage is Fully Covered for all 50 acceptance criteria at the mapping level, with execution evidence showing 18 failed test executions impacting requirement quality across 15 acceptance criteria.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC1 | NULL | Fully Covered |
| SCM-010 | AC2 | Defect observed in executed coverage: reminder notification omits current plan price for annual-billed subscriptions. | Fully Covered |
| SCM-010 | AC3 | NULL | Fully Covered |
| SCM-010 | AC4 | Coverage partial at field level: audit log verification present for subscription ID and renewal date, but payment method used, renewal amount, and timestamp are not explicitly validated by available test cases. | Fully Covered |
| SCM-010 | AC5 | Defect observed in executed coverage: subscription remains active after 3 failed payment retries instead of being suspended. | Fully Covered |
| SCM-011 | AC1 | Defect observed in executed coverage: duplicate cancellation request accepted when subscription already pending cancellation. | Fully Covered |
| SCM-011 | AC2 | NULL | Fully Covered |
| SCM-011 | AC3 | Coverage partial at field level: cancellation status is validated, but effective end date is not explicitly validated by available test cases. | Fully Covered |
| SCM-011 | AC4 | NULL | Fully Covered |
| SCM-011 | AC5 | Coverage partial at workflow level: prorated refund calculation is validated, but finance team review before refund issuance is not explicitly validated; defect observed in edge calculation with small negative refund value on last-day cancellation. | Fully Covered |
| SCM-012 | AC1 | NULL | Fully Covered |
| SCM-012 | AC2 | Defect observed in executed coverage: full price charged instead of minimal/zero proration on last-day upgrade. | Fully Covered |
| SCM-012 | AC3 | Defect observed in executed coverage: feature access delayed for midnight billing-boundary upgrades. | Fully Covered |
| SCM-012 | AC4 | Coverage partial at field level: previous plan, new plan, and timestamp are validated, but prorated amount and effective date are not explicitly validated by available test cases. | Fully Covered |
| SCM-012 | AC5 | NULL | Fully Covered |
| SCM-013 | AC1 | NULL | Fully Covered |
| SCM-013 | AC2 | Defect observed in executed coverage: revoke action for unassigned user returns generic server error instead of handled message. | Fully Covered |
| SCM-013 | AC3 | Coverage partial at field level: assignment status is validated, but expiration display is not explicitly validated by available test cases. | Fully Covered |
| SCM-013 | AC4 | NULL | Fully Covered |
| SCM-013 | AC5 | Defect observed in executed coverage: license pool count becomes inaccurate during rapid revoke/reassign sequence; administrator notification of limit is not explicitly validated by available test cases. | Fully Covered |
| SCM-014 | AC1 | NULL | Fully Covered |
| SCM-014 | AC2 | Defect observed in executed coverage: refund above threshold processed automatically before finance manager approval. | Fully Covered |
| SCM-014 | AC3 | NULL | Fully Covered |
| SCM-014 | AC4 | Defect observed in executed coverage: refund reason truncated in audit log; approver field is not explicitly validated by available test cases. | Fully Covered |
| SCM-014 | AC5 | NULL | Fully Covered |
| SCM-015 | AC1 | Defect observed in executed coverage: conversion attempted with expired payment method instead of downgrade path on exact trial end date. | Fully Covered |
| SCM-015 | AC2 | Coverage partial at requirement level: reminder timing is not explicitly validated because test cases do not specify or verify the configured lead time. | Fully Covered |
| SCM-015 | AC3 | Defect observed in executed coverage: downgrade notification not sent for invalid payment method scenario. | Fully Covered |
| SCM-015 | AC4 | NULL | Fully Covered |
| SCM-015 | AC5 | NULL | Fully Covered |
| SCM-016 | AC1 | NULL | Fully Covered |
| SCM-016 | AC2 | Defect observed in executed coverage: last-day add-on proration rounds to full month charge. | Fully Covered |
| SCM-016 | AC3 | Coverage partial at field level: active add-ons and individual charges are validated, but total subscription cost is not explicitly validated by available test cases. | Fully Covered |
| SCM-016 | AC4 | Defect observed in executed coverage: rapid add-on actions merged into single audit entry, losing one action. | Fully Covered |
| SCM-016 | AC5 | Coverage partial at requirement level: regional-regulation exception behavior for retroactive refund is not explicitly validated by available test cases. | Fully Covered |
| SCM-017 | AC1 | NULL | Fully Covered |
| SCM-017 | AC2 | Defect observed in executed coverage: international card format rejected as invalid. | Fully Covered |
| SCM-017 | AC3 | NULL | Fully Covered |
| SCM-017 | AC4 | Coverage partial at field level: subscription ID, new payment method reference, and timestamp are validated, but old payment method reference is not explicitly validated; defect observed where failed update attempt is not logged. | Fully Covered |
| SCM-017 | AC5 | Coverage gap: pending retry precondition is validated, but immediate retry using the new payment method is not explicitly validated by available test cases. | Fully Covered |
| SCM-018 | AC1 | Defect observed in executed coverage: consecutive failure counter does not reset after successful intervening payment. | Fully Covered |
| SCM-018 | AC2 | NULL | Fully Covered |
| SCM-018 | AC3 | Coverage partial at field level: suspension status is validated, but outstanding balance display is not explicitly validated by available test cases. | Fully Covered |
| SCM-018 | AC4 | Defect observed in executed coverage: audit log omits failed attempts from prior billing cycle. | Fully Covered |
| SCM-018 | AC5 | Coverage partial at requirement level: successful payment and block on unpaid balance are validated, but restoration of full access within a defined SLA is not explicitly validated by available test cases. | Fully Covered |
| SCM-019 | AC1 | Defect observed in executed coverage: only one of several simultaneous tier price changes detected. | Fully Covered |
| SCM-019 | AC2 | Coverage partial at requirement level: notification content is validated, but at least 30 days advance notice is not explicitly validated by available test cases. | Fully Covered |
| SCM-019 | AC3 | NULL | Fully Covered |
| SCM-019 | AC4 | Coverage partial at field level: subscription ID, notification sent date, and timestamp are validated, but old price and new price capture in audit log are not explicitly validated by available test cases. | Fully Covered |
| SCM-019 | AC5 | Defect observed in executed coverage: downgrade request at effective-date boundary incorrectly charged penalty fee. | Fully Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 planned test cases include explicit user story and acceptance criteria mappings; all 150 executed test log entries map back to planned test cases and user stories. | NULL | NULL | Low |
| TP_SCM10_009, TP_SCM10_010 | Partial | AC4 requires subscription ID, renewal date, payment method used, renewal amount, and timestamp, but available tests validate only subscription ID and renewal date. | SCM-010 | AC4 | Medium |
| TP_SCM11_007, TP_SCM11_008, TP_SCM11_015 | Partial | AC3 requires cancellation status and effective end date; tests validate status visibility but not effective end date. | SCM-011 | AC3 | Medium |
| TP_SCM11_012, TP_SCM11_013 | Partial | AC5 requires prorated refund calculation subject to finance team review before issuance; tests validate calculation only, not review gate. | SCM-011 | AC5 | High |
| TP_SCM12_008, TP_SCM12_009 | Partial | AC4 requires previous plan, new plan, prorated amount, effective date, and timestamp; tests omit explicit validation of prorated amount and effective date in audit log. | SCM-012 | AC4 | Medium |
| TP_SCM13_006, TP_SCM13_007, TP_SCM13_015 | Partial | AC3 requires assignment status and expiration; tests validate status but not expiration. | SCM-013 | AC3 | Medium |
| TP_SCM13_011, TP_SCM13_012 | Partial | AC5 requires blocking assignment at license limit and notifying administrator; tests validate block/count behavior but not notification content/dispatch. | SCM-013 | AC5 | Medium |
| TP_SCM14_008, TP_SCM14_009 | Partial | AC4 requires approver field when applicable; tests validate subscription ID, amount, reason, and timestamp, but not approver capture. | SCM-014 | AC4 | Medium |
| TP_SCM15_003, TP_SCM15_004, TP_SCM15_015 | Ambiguous | AC2 requires reminder notification a specified number of days before trial expiration, but test cases do not evidence validation of the configured timing rule. | SCM-015 | AC2 | Medium |
| TP_SCM16_005, TP_SCM16_006, TP_SCM16_014 | Partial | AC3 requires active add-ons, individual charges, and total subscription cost; tests omit explicit total subscription cost validation. | SCM-016 | AC3 | Medium |
| TP_SCM16_010, TP_SCM16_011 | Partial | AC5 includes regional-regulation refund exception, but tests validate only default no-refund behavior and next-cycle billing stop. | SCM-016 | AC5 | Medium |
| TP_SCM17_007, TP_SCM17_008, TP_SCM17_009, TP_SCM17_015 | Partial | AC4 requires old and new payment method references plus timestamp; old reference is not explicitly validated and failed-update audit behavior is defective. | SCM-017 | AC4 | Medium |
| TP_SCM17_010 | Ambiguous | AC5 requires immediate retry using the new payment method; available test validates pending retry precondition only, not retry execution outcome. | SCM-017 | AC5 | High |
| TP_SCM18_005, TP_SCM18_013 | Partial | AC3 requires suspension status and outstanding balance display; tests validate status but not outstanding balance. | SCM-018 | AC3 | Medium |
| TP_SCM18_009, TP_SCM18_010 | Partial | AC5 requires restoration of full access within defined SLA after payment; tests validate reinstatement gating but not SLA-based access restoration timing. | SCM-018 | AC5 | Medium |
| TP_SCM19_003, TP_SCM19_004, TP_SCM19_005, TP_SCM19_013 | Partial | AC2 requires notification at least 30 days in advance; tests validate content and duplication control but not advance notice timing rule. | SCM-019 | AC2 | High |
| TP_SCM19_008, TP_SCM19_009 | Partial | AC4 requires old price and new price in audit log; tests validate subscription ID, notification sent date, and timestamp only. | SCM-019 | AC4 | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 planned test cases include explicit user story and acceptance criteria mappings; all 150 executed test log entries map back to planned test cases and user stories. | NULL | NULL | Low |
| TP_SCM10_009, TP_SCM10_010 | Partial | AC4 requires subscription ID, renewal date, payment method used, renewal amount, and timestamp, but available tests validate only subscription ID and renewal date. | SCM-010 | AC4 | Medium |
| TP_SCM11_007, TP_SCM11_008, TP_SCM11_015 | Partial | AC3 requires cancellation status and effective end date; tests validate status visibility but not effective end date. | SCM-011 | AC3 | Medium |
| TP_SCM11_012, TP_SCM11_013 | Partial | AC5 requires prorated refund calculation subject to finance team review before issuance; tests validate calculation only, not review gate. | SCM-011 | AC5 | High |
| TP_SCM12_008, TP_SCM12_009 | Partial | AC4 requires previous plan, new plan, prorated amount, effective date, and timestamp; tests omit explicit validation of prorated amount and effective date in audit log. | SCM-012 | AC4 | Medium |
| TP_SCM13_006, TP_SCM13_007, TP_SCM13_015 | Partial | AC3 requires assignment status and expiration; tests validate status but not expiration. | SCM-013 | AC3 | Medium |
| TP_SCM13_011, TP_SCM13_012 | Partial | AC5 requires blocking assignment at license limit and notifying administrator; tests validate block/count behavior but not notification content/dispatch. | SCM-013 | AC5 | Medium |
| TP_SCM14_008, TP_SCM14_009 | Partial | AC4 requires approver field when applicable; tests validate subscription ID, amount, reason, and timestamp, but not approver capture. | SCM-014 | AC4 | Medium |
| TP_SCM15_003, TP_SCM15_004, TP_SCM15_015 | Ambiguous | AC2 requires reminder notification a specified number of days before trial expiration, but test cases do not evidence validation of the configured timing rule. | SCM-015 | AC2 | Medium |
| TP_SCM16_005, TP_SCM16_006, TP_SCM16_014 | Partial | AC3 requires active add-ons, individual charges, and total subscription cost; tests omit explicit total subscription cost validation. | SCM-016 | AC3 | Medium |
| TP_SCM16_010, TP_SCM16_011 | Partial | AC5 includes regional-regulation refund exception, but tests validate only default no-refund behavior and next-cycle billing stop. | SCM-016 | AC5 | Medium |
| TP_SCM17_007, TP_SCM17_008, TP_SCM17_009, TP_SCM17_015 | Partial | AC4 requires old and new payment method references plus timestamp; old reference is not explicitly validated and failed-update audit behavior is defective. | SCM-017 | AC4 | Medium |
| TP_SCM17_010 | Ambiguous | AC5 requires immediate retry using the new payment method; available test validates pending retry precondition only, not retry execution outcome. | SCM-017 | AC5 | High |
| TP_SCM18_005, TP_SCM18_013 | Partial | AC3 requires suspension status and outstanding balance display; tests validate status but not outstanding balance. | SCM-018 | AC3 | Medium |
| TP_SCM18_009, TP_SCM18_010 | Partial | AC5 requires restoration of full access within defined SLA after payment; tests validate reinstatement gating but not SLA-based access restoration timing. | SCM-018 | AC5 | Medium |
| TP_SCM19_003, TP_SCM19_004, TP_SCM19_005, TP_SCM19_013 | Partial | AC2 requires notification at least 30 days in advance; tests validate content and duplication control but not advance notice timing rule. | SCM-019 | AC2 | High |
| TP_SCM19_008, TP_SCM19_009 | Partial | AC4 requires old price and new price in audit log; tests validate subscription ID, notification sent date, and timestamp only. | SCM-019 | AC4 | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 150.00 |
| Total Test Logs | 150.00 |
| Missing Test Cases | 0.00 |
| Missing Test Logs | 0.00 |
| Consistency Status | Consistent with partial requirement-to-test validation gaps. Explicit testcase-to-AC mapping integrity is strong, but 16 acceptance-criteria-level mapping sufficiency issues were identified where testcase intent does not fully validate all requirement elements. |

## Defect Details

Defect Details:

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

Unit test mapping coverage is complete at the acceptance-criteria level, but execution quality is not release-ready due to 20.00 defects/failures and multiple partial validation gaps against required fields, timing rules, approval gates, and SLA conditions. Remediation should prioritize failed ACs and add missing test coverage for unvalidated requirement elements before sign-off.
