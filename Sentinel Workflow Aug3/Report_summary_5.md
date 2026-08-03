# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 8 user stories: SCM-010 through SCM-017. All listed user story, test plan, and test log documents were present and readable; no defect log files were separately provided, so defect details were derived from the defect references embedded in the test log documents.

Across the analyzed scope, 40 acceptance criteria (5 per user story), 120 planned test cases, and 120 executed test log entries were identified. Document completeness was acceptable because each user story contained an identifiable ID, title, and acceptance criteria; each test plan contained test case IDs mapped to acceptance criteria and story IDs; and each test log contained execution status per test case. Overall unit test scope includes renewal, cancellation, upgrade, license allocation, refund, trial conversion, add-on bundling, and payment method update processing.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC4 | No testcase mapped for payment method used; renewal amount audit field not explicitly validated. | Partially Covered |
| SCM-011 | AC3 | No testcase mapped for effective end date display. | Partially Covered |
| SCM-011 | AC5 | No testcase mapped for finance team review before refund issuance. | Partially Covered |
| SCM-012 | AC4 | No testcase mapped for prorated amount in audit log; no testcase mapped for effective date in audit log. | Partially Covered |
| SCM-013 | AC3 | No testcase mapped for license expiration display. | Partially Covered |
| SCM-013 | AC5 | No testcase mapped for administrator notification of license limit. | Partially Covered |
| SCM-014 | AC4 | No testcase mapped for approver field in audit log. | Partially Covered |
| SCM-015 | AC2 | Reminder lead time is not explicitly validated; no testcase mapped to verify specified number of days. | Partially Covered |
| SCM-016 | AC3 | No testcase mapped for total subscription cost display. | Partially Covered |
| SCM-016 | AC5 | No testcase mapped for regional-regulation exception handling. | Partially Covered |
| SCM-017 | AC4 | No testcase mapped for old payment method reference in audit log. | Partially Covered |
| SCM-017 | AC5 | No testcase mapped for immediate retry execution using new payment method; only pending retry precondition is validated. | Partially Covered |

## Consistency Analysis
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 120 test cases contain explicit mapping to both user story ID and acceptance criteria ID in the test plan and corresponding test log. | NULL | NULL | Low |
| NULL | Missing | No standalone defect log documents were provided; defect linkage was inferred from defect references embedded in test logs. | NULL | NULL | Medium |
| TP_SCM17_010 | Ambiguous/Partial | Test case validates only existence of pending retry state and does not validate AC5 outcome of immediate retry using the new payment method. | SCM-017 | AC5 | Medium |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 120 test cases contain explicit mapping to both user story ID and acceptance criteria ID in the test plan and corresponding test log. | NULL | NULL | Low |
| NULL | Missing | No standalone defect log documents were provided; defect linkage was inferred from defect references embedded in test logs. | NULL | NULL | Medium |
| TP_SCM17_010 | Ambiguous/Partial | Test case validates only existence of pending retry state and does not validate AC5 outcome of immediate retry using the new payment method. | SCM-017 | AC5 | Medium |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total test cases | 120 |
| Total test logs | 120 |
| Missing test cases | 0 |
| Missing test logs | 0 |
| Test case to test log reconciliation | 100.00% |
| Mapping consistency status | Mostly Consistent |

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

## Conclusion
Unit test execution evidence is complete and traceable, but overall quality is not yet release-ready because 12 acceptance criteria are only partially covered and 16 defects remain evidenced in execution logs. Remediation should prioritize closing missing validation points in audit, notification timing, portal display, approval, and retry-path scenarios, then retesting all failed and impacted edge/negative cases.
