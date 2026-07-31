# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

The assessment covers 14 user stories identified from the uploaded source documents: SCM-001, SCM-002, SCM-003, SCM-004, SCM-010, SCM-011, SCM-012, SCM-013, SCM-014, SCM-015, SCM-016, SCM-017, SCM-018, and SCM-019. A total of 70 acceptance criteria were derived from available user story documents, with 210 test cases and 206 executable test log entries analyzed from corresponding test plan and test log documents; SCM-005 user story document is missing, therefore its acceptance criteria and requirement baseline are unreadable and excluded from formal per-AC coverage derivation, though its available plan/log files were integrity-reviewed and flagged. Document integrity is largely complete for the analyzed set, with explicit testcase-to-AC mappings present in the test plans and execution results present in the logs; however, 4 planned test cases have no corresponding execution log entries, and 4 executed results are effectively inconsistent because they are marked Passed while the actual result states "not yet executed."

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date required by AC not validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date required by AC not validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date required by AC not explicitly validated in audit log testcase set. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes required by AC not validated by any testcase. | Partially Covered |
| SCM-003 | AC4 | Upgrade date field not explicitly validated separately from generic date/timestamp wording. | Partially Covered |
| SCM-010 | AC2 | Test coverage does not explicitly validate reminder is sent at least 7 days prior to renewal date. | Partially Covered |
| SCM-010 | AC4 | Payment method used and renewal amount required by AC not validated by any testcase. | Partially Covered |
| SCM-011 | AC5 | Finance team review before refund issuance not explicitly validated by any testcase. | Partially Covered |
| SCM-012 | AC4 | Prorated amount and effective date required by AC not explicitly validated in audit log testcase set. | Partially Covered |
| SCM-013 | AC3 | License expiration view required by AC not validated by any testcase. | Partially Covered |
| SCM-013 | AC5 | Administrator notification of license limit is not explicitly validated by any testcase. | Partially Covered |
| SCM-014 | AC4 | Approver field is required only when applicable and is not explicitly validated by testcase set. | Partially Covered |
| SCM-015 | AC2 | Reminder lead time is unspecified in tests; AC requires reminder a specified number of days before expiry. | Partially Covered |
| SCM-016 | AC3 | Total subscription cost view required by AC not validated by any testcase. | Partially Covered |
| SCM-016 | AC5 | Regional regulation exception for retroactive refund not validated by any testcase. | Partially Covered |
| SCM-017 | AC4 | Old payment method reference required by AC not validated by any testcase. | Partially Covered |
| SCM-017 | AC5 | Immediate retry using new payment method not validated; only pending retry state confirmed. | Partially Covered |
| SCM-018 | AC3 | Outstanding balance display required by AC not validated by any testcase. | Partially Covered |
| SCM-018 | AC5 | Defined SLA restoration timing not validated by any testcase. | Partially Covered |
| SCM-019 | AC4 | Old price and new price fields required by AC not explicitly validated in audit log testcase set. | Partially Covered |
| SCM-005 | NULL | User story document missing; ID/title/acceptance criteria cannot be validated. Formal AC-to-test coverage derivation cannot be completed. | Not Covered |

## Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Present in test plan for SCM-003 but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_014 | Missing Test Log | Present in test plan for SCM-004 but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Present in test plan for SCM-004 but no execution result found in test log. | SCM-004 | AC5 | Medium |
| TP_SCM11_005 | Ambiguous/Unreadable | Test log actual result is misaligned with testcase intent; output states effective date while testcase intent validates final billing details. | SCM-011 | AC2 | Medium |
| UT_SCM1_014 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-002 | AC5 | High |
| SCM-005 | Missing User Story | Test plan and test log exist, but user story source document is absent; mapped ACs cannot be traced back to approved requirements baseline. | SCM-005 | NULL | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Present in test plan for SCM-003 but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_014 | Missing Test Log | Present in test plan for SCM-004 but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Present in test plan for SCM-004 but no execution result found in test log. | SCM-004 | AC5 | Medium |
| TP_SCM11_005 | Ambiguous/Unreadable | Test log actual result is misaligned with testcase intent; output states effective date while testcase intent validates final billing details. | SCM-011 | AC2 | Medium |
| UT_SCM1_014 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Status Conflict | Marked Passed in status column but actual result states not yet executed. | SCM-002 | AC5 | High |
| SCM-005 | Missing User Story | Test plan and test log exist, but user story source document is absent; mapped ACs cannot be traced back to approved requirements baseline. | SCM-005 | NULL | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 210 |
| Total Test Logs | 206 |
| Missing Test Cases | 0 |
| Missing Test Logs | 4 |
| Consistency Status | Partially Consistent |

## Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-001 | AC2 | DEF-SCM1-001 | UT_SCM1_005 | Notification template rendering issue |
| SCM-001 | AC5 | DEF-SCM1-002 | UT_SCM1_009 | Refund workflow synchronization error |
| SCM-002 | AC4 | DEF-SCM2-101 | TP_SCM2_008 | Pause reason not captured consistently |
| SCM-002 | AC5 | DEF-SCM2-102 | TP_SCM2_009 | Activation allowed without completed approval |
| SCM-003 | AC2 | DEF-SCM3-101 | TP_SCM3_004 | Revised billing amount not included in upgrade confirmation notification |
| SCM-003 | AC5 | DEF-SCM3-102 | TP_SCM3_009 | Manager approval workflow not initiated when price increase equals exactly 50% |
| SCM-004 | AC2 | DEF-SCM4-101 | TP_SCM4_004 | Applicable refund details not included in cancellation confirmation notification |
| SCM-004 | AC5 | DEF-SCM4-102 | TP_SCM4_009 | Finance team approval workflow fails for mixed currency outstanding balances |
| SCM-005 | NULL | DEF-SCM5-101 | TP_SCM5_005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| SCM-005 | NULL | DEF-SCM5-103 | TP_SCM5_011 | System sends reminder even when subscription expiry date is null |
| SCM-005 | NULL | DEF-SCM5-104 | TP_SCM5_013 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| SCM-005 | NULL | DEF-SCM5-105 | TP_SCM5_015 | Reminder log delivery status remains blank when notification channel fails |
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

Unit testing demonstrates broad requirement coverage across the available user stories, but the quality baseline is not fully compliant due to 21 partially covered acceptance criteria, 32 logged defects, 4 missing test logs, 4 execution-status conflicts, and the missing SCM-005 user story source document. Remediation should prioritize closure of approval, billing, notification, and audit-log defects, completion/correction of inconsistent execution evidence, and creation of missing tests for uncovered AC elements before sign-off.
