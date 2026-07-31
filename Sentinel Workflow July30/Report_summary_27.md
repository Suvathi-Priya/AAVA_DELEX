# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 10 user stories (SCM-010 through SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 corresponding execution log entries derived directly from the uploaded user story, test plan, and test log documents. Document completeness and integrity validation is satisfactory for all uploaded artifacts: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs with explicit AC mapping; each test log contains execution results per test case; and no standalone defect log document was provided, so defect details were derived from defect references embedded in the execution logs.

Total derived metrics: 150 test cases, 150 test logs, 0 missing test cases, 0 missing test logs, 10 user stories in scope, and 50 acceptance criteria assessed for coverage.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC3 | Auditably covered by test plan, but execution evidence does not validate plan details, price, and at least 7 days prior timing as separate conditions. | Partially Covered |
| SCM-010 | AC4 | Payment method used, renewal amount, and timestamp are not explicitly validated by mapped test cases. | Partially Covered |
| SCM-011 | AC3 | Effective end date is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-011 | AC5 | Finance team review before refund issuance is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-012 | AC4 | Prorated amount and effective date are not explicitly validated by mapped test cases. | Partially Covered |
| SCM-013 | AC3 | License expiration visibility in portal is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-014 | AC4 | Approver (if applicable) is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-015 | AC2 | Reminder lead time is not explicitly validated because the user story states a specified number of days, but the exact timing rule is not tested as a distinct condition. | Partially Covered |
| SCM-016 | AC3 | Total subscription cost in portal is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-016 | AC5 | Regional regulation exception handling is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-017 | AC4 | Old payment method reference is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-017 | AC5 | Immediate retry using the new payment method is not explicitly validated; only pending retry existence is tested. | Partially Covered |
| SCM-018 | AC3 | Outstanding balance visibility in portal is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-018 | AC5 | Defined SLA for restoration of full access is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-019 | AC2 | At least 30 days advance timing is not explicitly validated by mapped test cases. | Partially Covered |
| SCM-019 | AC4 | Old price and new price are not explicitly validated by mapped audit log test cases. | Partially Covered |

## Consistency Analysis
| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test cases in the uploaded plans contain explicit mapping to a single user story ID and acceptance criteria ID, and all execution log entries align to the same mapped IDs. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| TP_SCM17_010 | Partial | Test case validates prerequisite pending retry state only and does not fully validate the AC5 obligation requiring immediate retry using the new payment method. | SCM-017 | AC5 | Medium |
| TP_SCM10_004 to TP_SCM10_005 | Partial | AC2 mapping is explicit, but planned tests do not fully decompose the timing obligation of at least 7 days prior as a separate validation point. | SCM-010 | AC2 | Medium |
| TP_SCM11_012 to TP_SCM11_013 | Partial | AC5 mapping is explicit, but finance team review before refund issuance is not directly evidenced in mapped tests. | SCM-011 | AC5 | Medium |
| TP_SCM18_009 to TP_SCM18_010 | Partial | AC5 mapping is explicit, but SLA-based restoration timing is not directly validated. | SCM-018 | AC5 | Medium |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All test cases in the uploaded plans contain explicit mapping to a single user story ID and acceptance criteria ID, and all execution log entries align to the same mapped IDs. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| TP_SCM17_010 | Partial | Test case validates prerequisite pending retry state only and does not fully validate the AC5 obligation requiring immediate retry using the new payment method. | SCM-017 | AC5 | Medium |
| TP_SCM10_004 to TP_SCM10_005 | Partial | AC2 mapping is explicit, but planned tests do not fully decompose the timing obligation of at least 7 days prior as a separate validation point. | SCM-010 | AC2 | Medium |
| TP_SCM11_012 to TP_SCM11_013 | Partial | AC5 mapping is explicit, but finance team review before refund issuance is not directly evidenced in mapped tests. | SCM-011 | AC5 | Medium |
| TP_SCM18_009 to TP_SCM18_010 | Partial | AC5 mapping is explicit, but SLA-based restoration timing is not directly validated. | SCM-018 | AC5 | Medium |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 150 |
| Total Test Logs | 150 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent with partial requirement-level validation gaps. No ambiguous mappings, duplicate testcase IDs, or unmapped execution log entries were identified from the uploaded documents. |

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
Unit test documentation is structurally complete and mapping consistency is generally sound, but quality is constrained by 20.00 logged defects and 15.00 partially covered acceptance criteria where key business obligations are not explicitly validated. Remediation is required to close requirement-level coverage gaps and resolve failed edge/negative scenarios before the test baseline can be considered fully compliant and coverage-complete.
