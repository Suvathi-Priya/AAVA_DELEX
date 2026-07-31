# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 19 user stories (SCM-001 to SCM-019) derived from the uploaded user story, unit test plan, and unit test execution log documents. A total of 285 test cases and 283 test log entries were identified from the source files; 2 planned test cases do not have corresponding executable results because SCM-003 execution log contains 13 results for 15 planned test cases. Document completeness exceptions were noted for SCM-008, where the test plan and test log file naming differs from the standard hyphenated convention but remains readable; no standalone defect log documents were provided, so defect details were derived from execution logs only. Overall unit test scope includes requirement-to-acceptance-criteria validation, positive/negative/edge scenarios, execution outcome review, mapping consistency review, and defect extraction across all available stories.

This report evaluates unit test coverage and quality across 19 user stories (SCM-001 to SCM-019). These user stories, together with their mapped acceptance criteria, form the baseline reference for all coverage, execution, and defect assessments presented in this report.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date explicitly required in audit log AC but not validated by any testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Missing test log entries for TP_SCM3_014 and TP_SCM3_015. | Fully Covered |
| SCM-005 | AC4 | Channel used explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount explicitly required by AC but not directly validated by testcase design. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, credit issued, and timestamp are only partially validated; existing tests cover IDs and zero-credit edge only. | Partially Covered |
| SCM-006 | AC5 | Customer retention review explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-007 | AC3 | Billing change summary explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID explicitly required by AC but not directly validated by testcase design. | Partially Covered |
| SCM-008 | AC1 | Test case IDs in plan (TP_SCM8_xxx) and log (UT_SCM8_xxx) use inconsistent prefixes, causing ambiguous direct testcase-to-log matching. | Fully Covered |
| SCM-008 | AC2 | Test case IDs in plan (TP_SCM8_xxx) and log (UT_SCM8_xxx) use inconsistent prefixes, causing ambiguous direct testcase-to-log matching. | Fully Covered |
| SCM-008 | AC3 | Test case IDs in plan (TP_SCM8_xxx) and log (UT_SCM8_xxx) use inconsistent prefixes, causing ambiguous direct testcase-to-log matching. | Fully Covered |
| SCM-008 | AC4 | Test case IDs in plan (TP_SCM8_xxx) and log (UT_SCM8_xxx) use inconsistent prefixes, causing ambiguous direct testcase-to-log matching. | Fully Covered |
| SCM-008 | AC5 | Test case IDs in plan (TP_SCM8_xxx) and log (UT_SCM8_xxx) use inconsistent prefixes, causing ambiguous direct testcase-to-log matching. | Fully Covered |
| SCM-009 | AC2 | Edge testcase UT_SCM9_014 is pending/not executed. | Fully Covered |
| SCM-009 | AC5 | Edge testcase UT_SCM9_015 is pending/not executed. | Fully Covered |
| SCM-010 | AC2 | AC requires reminder at least 7 days prior; exact timing rule not directly validated beyond notification presence. | Partially Covered |
| SCM-010 | AC4 | Payment method used, renewal amount, and timestamp explicitly required by AC but not directly validated by testcase design. | Partially Covered |
| SCM-011 | AC5 | Finance team review explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-012 | AC4 | Prorated amount and effective date explicitly required by AC but not directly validated by testcase design. | Partially Covered |
| SCM-013 | AC3 | License expiration explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-013 | AC5 | Administrator notification of license limit explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-014 | AC4 | Approver field explicitly required by AC but not directly validated by testcase design. | Partially Covered |
| SCM-015 | AC2 | AC states reminder must be sent a specified number of days before expiry; exact day-rule not directly validated by testcase design. | Partially Covered |
| SCM-016 | AC3 | Total subscription cost explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-016 | AC5 | Regional regulation exception explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-017 | AC4 | Old payment method reference explicitly required by AC but not directly validated by testcase design. | Partially Covered |
| SCM-017 | AC5 | Immediate retry using the new payment method explicitly required by AC but not validated by any testcase; current test only confirms pending retry state exists. | Partially Covered |
| SCM-018 | AC3 | Outstanding balance explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-018 | AC5 | Defined SLA restoration timing explicitly required by AC but not validated by any testcase. | Partially Covered |
| SCM-019 | AC2 | AC requires notification at least 30 days in advance; timing rule not directly validated by testcase design. | Partially Covered |
| SCM-019 | AC4 | Old price and new price explicitly required by AC but not directly validated in audit log testcase design. | Partially Covered |

## Consistency Analysis

| Testcase ID / Scope | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| SCM-001 to SCM-002, SCM-004 to SCM-019 | Direct | Test plans explicitly map testcase IDs to AC IDs and story IDs; execution logs generally preserve the same mapping structure. | As listed | As listed | Low |
| SCM-003 | Missing Test Logs | Test plan contains 15 test cases but execution log contains only 13 results; TP_SCM3_014 and TP_SCM3_015 are missing from log. | SCM-003 | AC1, AC5 | High |
| SCM-008 | Ambiguous | Test plan uses TP_SCM8_xxx identifiers while execution log uses UT_SCM8_xxx identifiers, preventing strict one-to-one ID consistency despite apparent AC/story alignment. | SCM-008 | AC1-AC5 | Medium |
| SCM-001 | Execution Status Inconsistency | Execution log marks UT_SCM1_014 and UT_SCM1_015 as Passed while actual result text states not yet executed. | SCM-001 | AC2, AC5 | High |
| SCM-002 | Execution Status Inconsistency | Execution log marks TP_SCM2_014 and TP_SCM2_015 as Passed while actual result text states not yet executed. | SCM-002 | AC1, AC5 | High |
| SCM-009 | Execution Status Inconsistency | UT_SCM9_014 and UT_SCM9_015 are marked Pending, which is consistent for not executed edge tests; no issue. | SCM-009 | AC2, AC5 | Low |
| SCM-008 | Duplicate Mapping Field | Test plan includes duplicate mapped story columns (“Mapped Story ID” and “Mapped Story ID.1”), creating redundant mapping metadata. | SCM-008 | AC1-AC5 | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| SCM-001 to SCM-002, SCM-004 to SCM-019 | Direct | Test plans explicitly map testcase IDs to AC IDs and story IDs; execution logs generally preserve the same mapping structure. | As listed | As listed | Low |
| SCM-003 | Missing Test Logs | Test plan contains 15 test cases but execution log contains only 13 results; TP_SCM3_014 and TP_SCM3_015 are missing from log. | SCM-003 | AC1, AC5 | High |
| SCM-008 | Ambiguous | Test plan uses TP_SCM8_xxx identifiers while execution log uses UT_SCM8_xxx identifiers, preventing strict one-to-one ID consistency despite apparent AC/story alignment. | SCM-008 | AC1-AC5 | Medium |
| SCM-001 | Execution Status Inconsistency | Execution log marks UT_SCM1_014 and UT_SCM1_015 as Passed while actual result text states not yet executed. | SCM-001 | AC2, AC5 | High |
| SCM-002 | Execution Status Inconsistency | Execution log marks TP_SCM2_014 and TP_SCM2_015 as Passed while actual result text states not yet executed. | SCM-002 | AC1, AC5 | High |
| SCM-009 | Execution Status Inconsistency | UT_SCM9_014 and UT_SCM9_015 are marked Pending, which is consistent for not executed edge tests; no issue. | SCM-009 | AC2, AC5 | Low |
| SCM-008 | Duplicate Mapping Field | Test plan includes duplicate mapped story columns (“Mapped Story ID” and “Mapped Story ID.1”), creating redundant mapping metadata. | SCM-008 | AC1-AC5 | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total test cases | 285 |
| total test logs | 283 |
| missing test cases | 0.00 |
| missing test logs | 2.00 |
| consistency status | Partially Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | Notification template rendering issue | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | Refund workflow synchronization error | Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | Pause reason not captured consistently | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | Activation allowed without completed approval | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | Revised billing amount not included in upgrade confirmation notification | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | Applicable refund details not included in cancellation confirmation notification | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | Finance team approval workflow fails for mixed currency outstanding balances | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | System sends reminder even when subscription expiry date is null | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | Reminder log delivery status remains blank when notification channel fails | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | Audit log not created when downgrade results in zero credit amount | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 / TP_SCM7_015 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | Audit log authorization reference field empty when transfer initiated via bulk admin API | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | Points posting service delay | Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | Balance refresh cache issue | Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | Redemption workflow synchronization issue | Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | SMS gateway timeout prevents delivery | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | Push notification service ignores user preference flag | Push notification service ignores user preference flag |
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

Unit test coverage is broadly established across all 19 user stories, but overall quality status is Partially Compliant due to multiple partially covered acceptance criteria, 2.00 missing execution records, mapping inconsistencies, and numerous functional defects including approval, notification, audit-log, boundary, and retry-flow failures. Remediation should prioritize closure of missing/contradictory execution evidence, addition of test cases for explicitly unvalidated AC elements, and retest of all failed and pending scenarios before sign-off.
