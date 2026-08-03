# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 10 user stories: SCM-010 through SCM-019. A total of 150 unit test cases were identified from the uploaded unit test plan documents, and 150 corresponding test log entries were identified from the uploaded execution logs, resulting in 100.00% test log availability with 0 missing test cases and 0 missing test logs.

All reviewed user story documents contained an identifiable user story ID, title, and acceptance criteria. All reviewed test plan documents contained explicit mappings between test cases and acceptance criteria, and all reviewed test log documents contained execution results per test case. No separate defect log documents were provided; defect details were derived from the defect references embedded in the execution log documents. Overall unit test scope includes functional, negative, and edge coverage across 50 acceptance criteria.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC1 | NULL | Fully Covered |
| SCM-010 | AC2 | Defect observed in reminder content validation for annual-billed subscriptions. | Fully Covered |
| SCM-010 | AC3 | NULL | Fully Covered |
| SCM-010 | AC4 | Audit log coverage is partial: payment method used, renewal amount, and timestamp were not explicitly validated by available test cases. | Partially Covered |
| SCM-010 | AC5 | Defect observed in suspension after 3 failed payment retries. | Fully Covered |
| SCM-011 | AC1 | Defect observed for duplicate cancellation handling when already pending cancellation. | Fully Covered |
| SCM-011 | AC2 | NULL | Fully Covered |
| SCM-011 | AC3 | Effective end date was not explicitly validated by available test cases. | Partially Covered |
| SCM-011 | AC4 | NULL | Fully Covered |
| SCM-011 | AC5 | Finance team review before refund issuance was not explicitly validated by available test cases; defect observed in last-day prorated refund calculation. | Partially Covered |
| SCM-012 | AC1 | NULL | Fully Covered |
| SCM-012 | AC2 | Defect observed for last-day billing-cycle proration. | Fully Covered |
| SCM-012 | AC3 | Defect observed for delayed feature access at midnight billing boundary. | Fully Covered |
| SCM-012 | AC4 | Audit log coverage is partial: prorated amount and effective date were not explicitly validated by available test cases. | Partially Covered |
| SCM-012 | AC5 | NULL | Fully Covered |
| SCM-013 | AC1 | NULL | Fully Covered |
| SCM-013 | AC2 | Defect observed for revoke action error handling when no license is assigned. | Fully Covered |
| SCM-013 | AC3 | License expiration was not explicitly validated by available test cases. | Partially Covered |
| SCM-013 | AC4 | NULL | Fully Covered |
| SCM-013 | AC5 | Defect observed for transient license count inconsistency during rapid revoke/reassign operations. | Fully Covered |
| SCM-014 | AC1 | NULL | Fully Covered |
| SCM-014 | AC2 | Defect observed where above-threshold refund was processed before finance manager approval. | Fully Covered |
| SCM-014 | AC3 | NULL | Fully Covered |
| SCM-014 | AC4 | Audit log coverage is partial: approver field was not explicitly validated by available test cases; defect observed for refund reason truncation. | Partially Covered |
| SCM-014 | AC5 | NULL | Fully Covered |
| SCM-015 | AC1 | Defect observed for expired payment method handling on exact trial end date. | Fully Covered |
| SCM-015 | AC2 | Reminder timing in days before trial expiration was not explicitly validated by available test cases. | Partially Covered |
| SCM-015 | AC3 | Defect observed where downgrade notification was not sent for invalid payment method. | Fully Covered |
| SCM-015 | AC4 | NULL | Fully Covered |
| SCM-015 | AC5 | NULL | Fully Covered |
| SCM-016 | AC1 | NULL | Fully Covered |
| SCM-016 | AC2 | Defect observed for incorrect last-day prorated charge rounding. | Fully Covered |
| SCM-016 | AC3 | Total subscription cost was not explicitly validated by available test cases. | Partially Covered |
| SCM-016 | AC4 | Defect observed where rapid add-on actions were merged into one audit entry. | Fully Covered |
| SCM-016 | AC5 | Regional regulation exception for retroactive refund was not explicitly validated by available test cases. | Fully Covered |
| SCM-017 | AC1 | NULL | Fully Covered |
| SCM-017 | AC2 | Defect observed for international card format validation. | Fully Covered |
| SCM-017 | AC3 | NULL | Fully Covered |
| SCM-017 | AC4 | Audit log coverage is partial: old payment method reference was not explicitly validated by available test cases; defect observed for failed-update logging. | Partially Covered |
| SCM-017 | AC5 | Immediate retry using the new payment method was not explicitly validated by available test cases; only pending retry precondition was tested. | Partially Covered |
| SCM-018 | AC1 | Defect observed where consecutive failure counter does not reset after successful payment. | Fully Covered |
| SCM-018 | AC2 | NULL | Fully Covered |
| SCM-018 | AC3 | Outstanding balance was not explicitly validated by available test cases. | Partially Covered |
| SCM-018 | AC4 | Defect observed where prior-cycle failed attempts were omitted from suspension audit log. | Fully Covered |
| SCM-018 | AC5 | Restoration within defined SLA was not explicitly validated by available test cases. | Partially Covered |
| SCM-019 | AC1 | Defect observed for incomplete detection of simultaneous tier price changes. | Fully Covered |
| SCM-019 | AC2 | Advance notice timing of at least 30 days was not explicitly validated by available test cases. | Partially Covered |
| SCM-019 | AC3 | NULL | Fully Covered |
| SCM-019 | AC4 | Audit log coverage is partial: old price and new price were not explicitly validated by available test cases. | Partially Covered |
| SCM-019 | AC5 | Defect observed for penalty charged at effective-date downgrade boundary. | Fully Covered |

## Consistency Analysis
| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 reviewed test cases contained explicit acceptance-criteria mappings in the test plan and matching acceptance-criteria references in the execution logs. No ambiguous, missing, or duplicate testcase-to-AC mappings were identified from the uploaded documents. | NULL | NULL | Low |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All 150 reviewed test cases contained explicit acceptance-criteria mappings in the test plan and matching acceptance-criteria references in the execution logs. No ambiguous, missing, or duplicate testcase-to-AC mappings were identified from the uploaded documents. | NULL | NULL | Low |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 150 |
| Total Test Logs | 150 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

Document-to-test mapping integrity is consistent across all reviewed user stories. While mapping completeness is strong, several acceptance criteria remain only partially covered where some obligation elements were not explicitly validated despite the presence of mapped test cases.

## Defect Details
| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-010 | AC2 | DEF-SCM10-101 | TP_SCM10_005 | Reminder notification omits current plan price for annual-billed subscriptions |
| SCM-010 | AC5 | DEF-SCM10-102 | TP_SCM10_012 | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| SCM-011 | AC5 | DEF-SCM11-101 | TP_SCM11_013 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| SCM-011 | AC1 | DEF-SCM11-102 | TP_SCM11_014 | Duplicate cancellation request accepted when subscription already pending cancellation |
| SCM-012 | AC3 | DEF-SCM12-101 | TP_SCM12_014 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| SCM-012 | AC2 | DEF-SCM12-102 | TP_SCM12_015 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| SCM-013 | AC2 | DEF-SCM13-101 | TP_SCM13_005 | Revoking license from team member with no assignment returns generic server error instead of handled message |
| SCM-013 | AC5 | DEF-SCM13-102 | TP_SCM13_012 | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| SCM-014 | AC4 | DEF-SCM14-101 | TP_SCM14_009 | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| SCM-014 | AC2 | DEF-SCM14-102 | TP_SCM14_013 | Refund request above threshold processed automatically before finance manager approval recorded |
| SCM-015 | AC1 | DEF-SCM15-101 | TP_SCM15_013 | Conversion attempted using expired payment method instead of failing over to downgrade path |
| SCM-015 | AC3 | DEF-SCM15-102 | TP_SCM15_014 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| SCM-016 | AC2 | DEF-SCM16-101 | TP_SCM16_013 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| SCM-016 | AC4 | DEF-SCM16-102 | TP_SCM16_015 | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| SCM-017 | AC2 | DEF-SCM17-101 | TP_SCM17_012 | International card format with alphanumeric routing details rejected as invalid |
| SCM-017 | AC4 | DEF-SCM17-102 | TP_SCM17_015 | No audit log entry created when payment method update fails midway through processing |
| SCM-018 | AC1 | DEF-SCM18-101 | TP_SCM18_011 | Consecutive failure counter does not reset after an intervening successful payment |
| SCM-018 | AC4 | DEF-SCM18-102 | TP_SCM18_014 | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| SCM-019 | AC1 | DEF-SCM19-101 | TP_SCM19_012 | Only one of several simultaneous tier price changes is detected and flagged for notification |
| SCM-019 | AC5 | DEF-SCM19-102 | TP_SCM19_015 | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

## Conclusion
Unit test artifacts are structurally complete and mapping consistency is strong, but quality risk remains due to 20 logged defects and multiple partially covered acceptance criteria where key business obligations were not explicitly validated. Remediation should prioritize defect closure and add targeted test cases for missing obligation elements, especially audit fields, timing/SLA validations, portal data completeness, approval controls, and regulatory or boundary-condition behaviors.
