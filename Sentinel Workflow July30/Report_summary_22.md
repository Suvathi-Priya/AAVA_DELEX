# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 corresponding execution log entries reviewed directly from the uploaded source documents. Document completeness and integrity are acceptable for all reviewed items: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs with explicit AC mapping; each test log contains execution status per test case; no separate defect log documents were provided, so defect details were derived from the defect references embedded in the execution logs. Overall consistency summary: total test cases = 150, total test logs = 150, missing test cases = 0, missing test logs = 0, consistency status = Consistent.

Coverage assessment by derived AC mapping indicates 45 acceptance criteria are Fully Covered and 5 acceptance criteria are Partially Covered; 0 acceptance criteria are Not Covered.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC2 | Defect observed in plan detail/price inclusion scenario for annual-billed subscriptions. | Partially Covered |
| SCM-010 | AC4 | No testcase mapped for payment method used. No testcase mapped for renewal amount. | Partially Covered |
| SCM-010 | AC5 | Defect observed in suspension after 3 failed retries scenario. Missing explicit testcase for full retry sequence up to 3 attempts. | Partially Covered |
| SCM-011 | AC3 | No testcase mapped for effective end date display. | Partially Covered |
| SCM-011 | AC5 | No testcase mapped for finance team review before refund issuance. Defect observed in last-day prorated refund calculation edge scenario. | Partially Covered |
| SCM-012 | AC4 | No testcase mapped for prorated amount in audit log. No testcase mapped for effective date in audit log. | Partially Covered |
| SCM-013 | AC3 | No testcase mapped for license expiration display. | Partially Covered |
| SCM-013 | AC5 | No testcase mapped for administrator notification of license limit. Defect observed in quick revoke/reassign count accuracy scenario. | Partially Covered |
| SCM-015 | AC2 | No testcase mapped for validation of specified reminder lead time. | Partially Covered |
| SCM-016 | AC3 | No testcase mapped for total subscription cost display. | Partially Covered |
| SCM-016 | AC5 | No testcase mapped for regional regulation exception. | Partially Covered |
| SCM-017 | AC4 | No testcase mapped for old payment method reference capture. Defect observed for failed update audit logging. | Partially Covered |
| SCM-017 | AC5 | No testcase mapped for immediate retry execution using new payment method. Existing testcase validates pending retry precondition only. | Partially Covered |
| SCM-018 | AC3 | No testcase mapped for outstanding balance display. | Partially Covered |
| SCM-018 | AC5 | No testcase mapped for restoration within defined SLA. | Partially Covered |
| SCM-019 | AC2 | No testcase mapped for validation of 30 days advance notice. | Partially Covered |
| SCM-019 | AC4 | No testcase mapped for old price capture in audit log. No testcase mapped for new price capture in audit log. | Partially Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 test cases in the reviewed test plans include explicit mapping to user story ID and acceptance criteria ID; no ambiguous, duplicate, or missing mappings identified. | NULL | NULL | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 test cases in the reviewed test plans include explicit mapping to user story ID and acceptance criteria ID; no ambiguous, duplicate, or missing mappings identified. | NULL | NULL | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 150 |
| total_testlogs | 150 |
| missing_testcases | 0 |
| missing_testlogs | 0 |
| consistency_status | Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title / Description |
|---|---|---|---|
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

## Conclusion

The unit test set is structurally consistent and substantially complete, but quality risk remains because multiple acceptance criteria are only partially covered and 20 executed test cases failed with linked defects. Remediation should prioritize closing uncovered requirement elements in audit, timing, notification, SLA, and portal-display scenarios and retesting all defect-affected acceptance criteria before sign-off.
