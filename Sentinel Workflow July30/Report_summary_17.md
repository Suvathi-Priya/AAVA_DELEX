# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 9 user stories: SCM-001 through SCM-009. Across the uploaded source documents, 135 test cases were identified in the unit test plans and 132 executable test log entries were identified in the test logs. The uploaded set includes complete user story, test plan, and test log coverage for SCM-001, SCM-002, SCM-003, SCM-004, SCM-005, SCM-006, SCM-007, SCM-008, and SCM-009, with no defect log files provided separately; therefore, defect details were derived only from the defect references embedded in the test log documents.

A total of 45 acceptance criteria were analyzed. Based on document-derived mappings and execution evidence, 34 acceptance criteria are Fully Covered, 11 are Partially Covered, and 0 are Not Covered. Missing or integrity observations noted during validation: SCM-008 and SCM-009 filenames are not fully consistent with the SCM-00X naming convention, no standalone defect log documents were uploaded, and three planned test cases do not have matching execution log entries: TP_SCM3_014, TP_SCM3_015, and TP_SCM4_015.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date not explicitly validated by any mapped testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not explicitly validated by any mapped testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated in audit log testcase; defect observed in pause reason capture consistency. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any mapped testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary/approval behavior inconsistency observed; planned edge testcase missing execution log for exactly 50% scenario. | Partially Covered |
| SCM-004 | AC5 | Planned boundary testcase for exactly $500 has no execution log; approval workflow defect observed for mixed currency balances. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used are not explicitly validated by any mapped testcase; failed delivery status defect observed. | Partially Covered |
| SCM-005 | AC5 | No testcase explicitly validates both recipients are notified for a value greater than $10,000; boundary behavior defect observed at exactly $10,000. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount validation failed in execution. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, and timestamp not explicitly validated by mapped testcases; zero-credit audit logging defect observed. | Partially Covered |
| SCM-006 | AC5 | Customer retention review not explicitly validated; downgrade processed before approval in one executed testcase. | Partially Covered |
| SCM-007 | AC3 | Billing change summary not explicitly validated by any mapped testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated; authorization reference defect observed for bulk API transfers. | Partially Covered |
| SCM-009 | AC2 | Planned international SMS edge testcase has no execution log; delivery defect observed. | Partially Covered |
| SCM-009 | AC5 | Planned exact 3rd retry boundary testcase has no execution log. | Partially Covered |

## Consistency Analysis
| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-004 | AC5 | Medium |
| UT_SCM8_001 to UT_SCM8_015 vs TP_SCM8_001 to TP_SCM8_015 | Ambiguous ID Mapping | Test plan uses TP_ prefix while test log uses UT_ prefix; AC and story mapping remain inferable but testcase IDs are not directly consistent. | SCM-008 | Multiple | Medium |
| SCM008_Test_Plan_upd.xlsx / SCM008_Test_Log_upd.xlsx | Naming Inconsistency | File naming omits hyphen compared with SCM-008 user story naming convention, but document linkage remains inferable. | SCM-008 | NULL | Low |
| SCM-009_User_Story_v2.docx | Versioned Artifact | User story file includes version suffix; no conflicting alternate file provided, so mapping remains inferable. | SCM-009 | NULL | Low |
| UT_SCM1_014 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_014 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-009 | AC5 | Medium |
| SCM-001 to SCM-009 | Missing Defect Log Documents | No standalone defect log uploaded; defects were derived from embedded test log references only. | Multiple | NULL | Medium |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase present in test plan but no execution result found in test log. | SCM-004 | AC5 | Medium |
| UT_SCM8_001 to UT_SCM8_015 vs TP_SCM8_001 to TP_SCM8_015 | Ambiguous ID Mapping | Test plan uses TP_ prefix while test log uses UT_ prefix; AC and story mapping remain inferable but testcase IDs are not directly consistent. | SCM-008 | Multiple | Medium |
| SCM008_Test_Plan_upd.xlsx / SCM008_Test_Log_upd.xlsx | Naming Inconsistency | File naming omits hyphen compared with SCM-008 user story naming convention, but document linkage remains inferable. | SCM-008 | NULL | Low |
| SCM-009_User_Story_v2.docx | Versioned Artifact | User story file includes version suffix; no conflicting alternate file provided, so mapping remains inferable. | SCM-009 | NULL | Low |
| UT_SCM1_014 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Status Ambiguity | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_014 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Execution Status Ambiguity | Testcase exists in plan and log, but execution status is Pending rather than executed result. | SCM-009 | AC5 | Medium |
| SCM-001 to SCM-009 | Missing Defect Log Documents | No standalone defect log uploaded; defects were derived from embedded test log references only. | Multiple | NULL | Medium |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 135 |
| Total Test Logs | 132 |
| Missing Test Cases | 0 |
| Missing Test Logs | 3 |
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
| SCM-005 | AC2 | DEF-SCM5-101 | TP_SCM5_005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| SCM-005 | AC1 | DEF-SCM5-103 | TP_SCM5_011 | System sends reminder even when subscription expiry date is null |
| SCM-005 | AC5 | DEF-SCM5-104 | TP_SCM5_013 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| SCM-005 | AC4 | DEF-SCM5-105 | TP_SCM5_015 | Reminder log delivery status remains blank when notification channel fails |
| SCM-006 | AC2 | DEF-SCM6-101 | TP_SCM6_005 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| SCM-006 | AC4 | DEF-SCM6-102 | TP_SCM6_012 | Audit log not created when downgrade results in zero credit amount |
| SCM-006 | AC5 | DEF-SCM6-103 | TP_SCM6_015 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| SCM-007 | AC2 | DEF-SCM7-101 | TP_SCM7_005 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| SCM-007 | AC5 | DEF-SCM7-102 | TP_SCM7_012 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| SCM-007 | AC4 | DEF-SCM7-103 | TP_SCM7_014 | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| SCM-007 | AC2 | DEF-SCM7-101 | TP_SCM7_015 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| SCM-008 | AC1 | DEF-SCM8-001 | UT_SCM8_003 | Points posting service delay |
| SCM-008 | AC3 | DEF-SCM8-002 | UT_SCM8_007 | Balance refresh cache issue |
| SCM-008 | AC5 | DEF-SCM8-003 | UT_SCM8_009 | Redemption workflow synchronization issue |
| SCM-009 | AC2 | DEF-SCM9-001 | UT_SCM9_004 | SMS gateway timeout prevents delivery |
| SCM-009 | AC3 | DEF-SCM9-002 | UT_SCM9_012 | Push notification service ignores user preference flag |

## Conclusion
Unit test coverage is broadly established across all uploaded user stories, but the overall quality posture is Partially Consistent due to 11 partially covered acceptance criteria, 3 missing execution logs, execution-status ambiguities, and multiple open defects affecting notification, approval, logging, and boundary-condition behavior. Remediation should prioritize closure of high-impact defects and re-execution of missing or ambiguously logged testcases before considering the unit test evidence fully audit-ready.
