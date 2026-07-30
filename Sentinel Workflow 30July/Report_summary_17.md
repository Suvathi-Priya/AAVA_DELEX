# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 9 user stories (SCM-001 to SCM-009) and evaluates unit test quality and requirement coverage using the uploaded user story, test plan, and test log documents. A total of 135 test cases and 133 executable test log entries were identified from the source files; 2 planned test cases do not have executed results in a valid execution status sense because they are marked Pending/not yet executed, and no standalone defect log documents were provided, so defect details were derived only from the defect references embedded in the test log files.

Document integrity review indicates that all 9 user stories contain identifiable IDs, titles, and acceptance criteria. All available test plans contain test case IDs with explicit AC mapping, and all available test logs contain per-test execution results; however, SCM-003, SCM-004, SCM-006, and SCM-007 each present only 13 logged executions against 15 planned tests, and SCM-008 shows a testcase ID naming inconsistency between plan (`TP_SCM8_xxx`) and log (`UT_SCM8_xxx`). Overall scope includes 45 acceptance criteria across the 9 user stories.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC1 | NULL | Fully Covered |
| SCM-001 | AC2 | Execution log quality issue: UT_SCM1_014 marked Passed but actual result states not yet executed | Fully Covered |
| SCM-001 | AC3 | NULL | Fully Covered |
| SCM-001 | AC4 | NULL | Fully Covered |
| SCM-001 | AC5 | Execution log quality issue: UT_SCM1_015 marked Passed but actual result states not yet executed; fraud review not explicitly validated by a distinct testcase | Fully Covered |
| SCM-002 | AC1 | Execution log quality issue: TP_SCM2_014 marked Passed but actual result states not yet executed | Fully Covered |
| SCM-002 | AC2 | Resume date not explicitly validated by any testcase | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not explicitly validated by any testcase | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated in audit log testcase | Partially Covered |
| SCM-002 | AC5 | Execution log quality issue: TP_SCM2_015 marked Passed but actual result states not yet executed | Fully Covered |
| SCM-003 | AC1 | Missing executed log for TP_SCM3_014; past-date edge scenario not evidenced in execution log | Partially Covered |
| SCM-003 | AC2 | NULL | Fully Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any testcase | Partially Covered |
| SCM-003 | AC4 | NULL | Fully Covered |
| SCM-003 | AC5 | Boundary testcase TP_SCM3_015 missing from execution log; ambiguity between AC wording (>50%) and testcase expecting exactly 50% to trigger approval | Partially Covered |
| SCM-004 | AC1 | NULL | Fully Covered |
| SCM-004 | AC2 | Edge testcase TP_SCM4_014 missing from execution log | Partially Covered |
| SCM-004 | AC3 | NULL | Fully Covered |
| SCM-004 | AC4 | NULL | Fully Covered |
| SCM-004 | AC5 | Boundary testcase TP_SCM4_015 missing from execution log; ambiguity between AC wording (> $500) and testcase expecting exactly $500 to trigger approval | Partially Covered |
| SCM-005 | AC1 | NULL | Fully Covered |
| SCM-005 | AC2 | NULL | Fully Covered |
| SCM-005 | AC3 | NULL | Fully Covered |
| SCM-005 | AC4 | Reminder date and channel used not explicitly validated by testcase set | Partially Covered |
| SCM-005 | AC5 | No positive testcase explicitly validates customer and account manager both receive reminders for value > $10,000 | Partially Covered |
| SCM-006 | AC1 | NULL | Fully Covered |
| SCM-006 | AC2 | Adjusted billing amount not explicitly validated by testcase description despite AC obligation | Partially Covered |
| SCM-006 | AC3 | NULL | Fully Covered |
| SCM-006 | AC4 | Current testcase validates only IDs and $0 credit case; previous plan, downgraded plan, effective date, and timestamp not explicitly validated; TP_SCM6_012 failed | Partially Covered |
| SCM-006 | AC5 | Customer retention review not explicitly validated by any testcase | Partially Covered |
| SCM-007 | AC1 | NULL | Fully Covered |
| SCM-007 | AC2 | Transfer details not explicitly validated as a separate obligation | Partially Covered |
| SCM-007 | AC3 | Billing change summary not explicitly validated by any testcase | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated by testcase descriptions; authorization reference testcase failed | Partially Covered |
| SCM-007 | AC5 | NULL | Fully Covered |
| SCM-008 | AC1 | Mapping inconsistency: plan uses TP_SCM8_xxx while log uses UT_SCM8_xxx | Fully Covered |
| SCM-008 | AC2 | Mapping inconsistency: plan uses TP_SCM8_xxx while log uses UT_SCM8_xxx; execution log quality issue: UT_SCM8_014 pending/not executed | Fully Covered |
| SCM-008 | AC3 | Mapping inconsistency: plan uses TP_SCM8_xxx while log uses UT_SCM8_xxx | Fully Covered |
| SCM-008 | AC4 | Mapping inconsistency: plan uses TP_SCM8_xxx while log uses UT_SCM8_xxx | Fully Covered |
| SCM-008 | AC5 | Mapping inconsistency: plan uses TP_SCM8_xxx while log uses UT_SCM8_xxx; execution log quality issue: UT_SCM8_015 pending/not executed; fraud review not explicitly validated by a distinct testcase | Fully Covered |
| SCM-009 | AC1 | NULL | Fully Covered |
| SCM-009 | AC2 | Execution log quality issue: UT_SCM9_014 pending/not executed | Fully Covered |
| SCM-009 | AC3 | NULL | Fully Covered |
| SCM-009 | AC4 | NULL | Fully Covered |
| SCM-009 | AC5 | Execution log quality issue: UT_SCM9_015 pending/not executed | Fully Covered |

## Consistency Analysis
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-003 | AC5 | High |
| TP_SCM4_014 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-004 | AC5 | High |
| TP_SCM6_012 | Direct but Partial Requirement Validation | Testcase directly maps to AC4 but validates only partial audit field set | SCM-006 | AC4 | Medium |
| TP_SCM6_015 | Direct but Partial Requirement Validation | Testcase validates approval hold but not customer retention review obligation | SCM-006 | AC5 | High |
| TP_SCM7_010 | Direct but Partial Requirement Validation | Audit log testcase validates owner IDs only, not full AC4 field set | SCM-007 | AC4 | Medium |
| TP_SCM8_001 to TP_SCM8_015 / UT_SCM8_001 to UT_SCM8_015 | Ambiguous / ID Naming Inconsistency | Test plan uses TP prefix while execution log uses UT prefix, preventing strict deterministic one-to-one ID matching without inference | SCM-008 | Multiple | Medium |
| UT_SCM1_014 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-001 | AC2 | Medium |
| UT_SCM1_015 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-002 | AC1 | Medium |
| TP_SCM2_015 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-002 | AC5 | High |
| UT_SCM8_014 | Pending Execution | Testcase exists in log but not executed | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Pending Execution | Testcase exists in log but not executed | SCM-008 | AC5 | High |
| UT_SCM9_014 | Pending Execution | Testcase exists in log but not executed | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Testcase exists in log but not executed | SCM-009 | AC5 | High |
| TP_SCM3_015 | Requirement-to-Test Ambiguity | AC states price increase greater than 50%, but testcase expects exactly 50% to trigger approval | SCM-003 | AC5 | High |
| TP_SCM4_015 | Requirement-to-Test Ambiguity | AC states outstanding balance greater than $500, but testcase expects exactly $500 to trigger approval | SCM-004 | AC5 | High |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-003 | AC5 | High |
| TP_SCM4_014 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase present in test plan but not found in execution log | SCM-004 | AC5 | High |
| TP_SCM6_012 | Direct but Partial Requirement Validation | Testcase directly maps to AC4 but validates only partial audit field set | SCM-006 | AC4 | Medium |
| TP_SCM6_015 | Direct but Partial Requirement Validation | Testcase validates approval hold but not customer retention review obligation | SCM-006 | AC5 | High |
| TP_SCM7_010 | Direct but Partial Requirement Validation | Audit log testcase validates owner IDs only, not full AC4 field set | SCM-007 | AC4 | Medium |
| TP_SCM8_001 to TP_SCM8_015 / UT_SCM8_001 to UT_SCM8_015 | Ambiguous / ID Naming Inconsistency | Test plan uses TP prefix while execution log uses UT prefix, preventing strict deterministic one-to-one ID matching without inference | SCM-008 | Multiple | Medium |
| UT_SCM1_014 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-001 | AC2 | Medium |
| UT_SCM1_015 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-002 | AC1 | Medium |
| TP_SCM2_015 | Execution Status Inconsistency | Status marked Passed while actual result states test not yet executed | SCM-002 | AC5 | High |
| UT_SCM8_014 | Pending Execution | Testcase exists in log but not executed | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Pending Execution | Testcase exists in log but not executed | SCM-008 | AC5 | High |
| UT_SCM9_014 | Pending Execution | Testcase exists in log but not executed | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Testcase exists in log but not executed | SCM-009 | AC5 | High |
| TP_SCM3_015 | Requirement-to-Test Ambiguity | AC states price increase greater than 50%, but testcase expects exactly 50% to trigger approval | SCM-003 | AC5 | High |
| TP_SCM4_015 | Requirement-to-Test Ambiguity | AC states outstanding balance greater than $500, but testcase expects exactly $500 to trigger approval | SCM-004 | AC5 | High |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 135 |
| Total Test Logs | 133.00 |
| Missing Test Cases | 0 |
| Missing Test Logs | 4.00 |
| Consistency Status | Partially Consistent |

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
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | Audit log authorization reference field empty when transfer initiated via bulk admin API | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM8-001 | UT_SCM8_003 | SCM-008 | Points posting service delay | Points posting service delay |
| DEF-SCM8-002 | UT_SCM8_007 | SCM-008 | Balance refresh cache issue | Balance refresh cache issue |
| DEF-SCM8-003 | UT_SCM8_009 | SCM-008 | Redemption workflow synchronization issue | Redemption workflow synchronization issue |
| DEF-SCM9-001 | UT_SCM9_004 | SCM-009 | SMS gateway timeout prevents delivery | SMS gateway timeout prevents delivery |
| DEF-SCM9-002 | UT_SCM9_012 | SCM-009 | Push notification service ignores user preference flag | Push notification service ignores user preference flag |

## Conclusion
Overall unit test coverage is broadly implemented across the 9 user stories, but the evidence is not fully audit-ready due to 23 recorded defects, 4 missing execution log entries, partial validation of several multi-part acceptance criteria, and multiple traceability inconsistencies. Remediation is required to execute and correctly log pending/boundary tests, align testcase identifiers and requirement thresholds, and add explicit tests for omitted AC obligations such as resume dates, billing change summaries, full audit-field validation, fraud review, and retention review.