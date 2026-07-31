# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 10 user stories (SCM-010 to SCM-019), 150 planned unit test cases, and 150 executed test log entries derived directly from the uploaded user story, test plan, and test log documents. Document completeness and integrity validation is satisfactory for the provided scope: each user story contains an identifiable ID, title, and 5 acceptance criteria; each test plan contains test case IDs mapped to acceptance criteria and story IDs; each test log contains execution results per test case; no separate defect log documents were provided, so defect details were derived from defect references embedded in the test log documents. Overall, 50 acceptance criteria were assessed, all are covered by at least one mapped test case, 34.00 defects were identified from execution evidence, missing test cases = 0, missing test logs = 0, and no unreadable documents were detected.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC4 | No testcase mapped for payment method used.; No testcase mapped for renewal amount. | Partially Covered |
| SCM-011 | AC3 | No testcase mapped for effective end date. | Partially Covered |
| SCM-011 | AC5 | No testcase mapped for finance team review before refund issuance.; Defect observed in execution: refund calculation returns small negative value for last-day-of-cycle cancellations | Partially Covered |
| SCM-012 | AC4 | No testcase mapped for prorated amount.; No testcase mapped for effective date. | Partially Covered |
| SCM-013 | AC3 | No testcase mapped for expiration. | Partially Covered |
| SCM-013 | AC5 | No testcase mapped for administrator notification.; Defect observed in execution: inaccurate license count during rapid revoke/reassign | Partially Covered |
| SCM-014 | AC4 | No testcase mapped for approver (if applicable).; Defect observed in execution: refund reason truncated in audit log for long free-text values | Partially Covered |
| SCM-015 | AC2 | No testcase mapped for specified number of days before expiration. | Partially Covered |
| SCM-016 | AC3 | No testcase mapped for total subscription cost. | Partially Covered |
| SCM-016 | AC5 | No testcase mapped for regional regulation exception. | Partially Covered |
| SCM-017 | AC4 | No testcase mapped for old payment method reference.; Defect observed in execution: no audit log entry created on failed update attempt | Partially Covered |
| SCM-017 | AC5 | No testcase mapped for immediate retry using new payment method. | Partially Covered |
| SCM-018 | AC3 | No testcase mapped for outstanding balance. | Partially Covered |
| SCM-018 | AC5 | No testcase mapped for restore full access within defined SLA. | Partially Covered |
| SCM-019 | AC2 | No testcase mapped for 30 days in advance timing requirement. | Partially Covered |
| SCM-019 | AC4 | No testcase mapped for old price.; No testcase mapped for new price. | Partially Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped Acceptance Criteria ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 test cases in the uploaded test plans are explicitly mapped to a user story ID and acceptance criteria ID; corresponding 150 execution log entries were found for the same test case IDs. No ambiguous, duplicate, or missing mappings were identified from the provided documents. | NULL | NULL | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 test cases in the uploaded test plans are explicitly mapped to a user story ID and acceptance criteria ID; corresponding 150 execution log entries were found for the same test case IDs. No ambiguous, duplicate, or missing mappings were identified from the provided documents. | NULL | NULL | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total test cases | 150 |
| total test logs | 150 |
| missing test cases | 0 |
| missing test logs | 0 |
| consistency status | Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
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

Unit test traceability is structurally consistent and all acceptance criteria have some level of coverage, but multiple acceptance criteria are only partially covered and 20.00 execution defects were evidenced, so the overall unit test quality status is At Risk. Remediation should prioritize closing unmapped requirement elements in audit, timing, notification, SLA, and portal-detail coverage, and resolving all failed execution defects before sign-off.
