# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report assesses 9 user stories (SCM-001 to SCM-009) using the uploaded user story documents, unit test plans, and unit test execution logs.

A total of 135 test cases and 133 test log entries were derived from the source documents, with 2 planned test cases not present in execution logs (SCM-003: TP_SCM3_014, TP_SCM3_015); no separate defect log documents were uploaded, so defect details were derived from defect references embedded in the execution logs. All 9 user stories contain identifiable IDs, titles, and acceptance criteria; all available test plans contain explicit AC mappings; all available test logs contain per-test execution results, though some logs show status/result inconsistencies where tests marked Passed/Pending state “not yet executed.”

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | Fraud review validation not explicitly covered by any testcase. | Fully Covered |
| SCM-002 | AC2 | Resume date required by AC not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date visibility not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date required by AC not explicitly validated in audit log testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Missing executed boundary testcase for exactly 50% increase; planned testcases TP_SCM3_014 and TP_SCM3_015 have no execution logs. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used required by AC not explicitly validated by testcase set. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount required by AC is not explicitly validated by testcase descriptions. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, credit issued, and timestamp not fully covered by testcase descriptions. | Partially Covered |
| SCM-006 | AC5 | Customer retention review required by AC not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC3 | Billing change summary visibility not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated by testcase descriptions. | Partially Covered |
| SCM-008 | AC5 | Fraud review validation not explicitly covered by any testcase. | Fully Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase exists in test plan but no execution result is present in uploaded test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase exists in test plan but no execution result is present in uploaded test log. | SCM-003 | AC5 | High |
| UT_SCM1_014 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-001 | AC2 | Medium |
| UT_SCM1_015 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-002 | AC1 | Medium |
| TP_SCM2_015 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_001 to UT_SCM8_015 | Ambiguous Mapping | Test plan uses TP_ prefix while execution log uses UT_ prefix; mappings are inferable by sequence/AC/story but not directly identical. | SCM-008 | Multiple | Medium |
| UT_SCM8_014 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-008 | AC5 | High |
| UT_SCM9_014 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-009 | AC5 | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase exists in test plan but no execution result is present in uploaded test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase exists in test plan but no execution result is present in uploaded test log. | SCM-003 | AC5 | High |
| UT_SCM1_014 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-001 | AC2 | Medium |
| UT_SCM1_015 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-002 | AC1 | Medium |
| TP_SCM2_015 | Status/Result Inconsistency | Test log status is Passed, but actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_001 to UT_SCM8_015 | Ambiguous Mapping | Test plan uses TP_ prefix while execution log uses UT_ prefix; mappings are inferable by sequence/AC/story but not directly identical. | SCM-008 | Multiple | Medium |
| UT_SCM8_014 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-008 | AC5 | High |
| UT_SCM9_014 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Testcase exists in plan and log but is marked Pending; execution incomplete. | SCM-009 | AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 135.00 |
| total_testlogs | 133.00 |
| missing_testcases | 0.00 |
| missing_testlogs | 2.00 |
| consistency_status | Partially Consistent |

Additional integrity issue noted: no standalone defect log documents were uploaded; defects were instead extracted from embedded execution log defect fields.

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

Unit test coverage is broadly established across all uploaded user stories, but the overall quality status is Partially Compliant due to execution-log inconsistencies, 2.00 missing test logs, several partially covered acceptance criteria, and open defects affecting notification content, approval workflows, audit completeness, and boundary conditions. Remediation should prioritize correcting traceability inconsistencies, executing all pending/missing boundary tests, and resolving AC-linked defects before compliance sign-off.
