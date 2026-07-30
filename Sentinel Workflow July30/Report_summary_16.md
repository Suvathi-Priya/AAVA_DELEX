# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report covers 5 user stories (SCM-001 to SCM-005), 75 planned unit test cases, and 73 corresponding test log entries identified from the uploaded source documents. Document completeness is partially valid: all 5 user story documents, all 5 test plan documents, and all 5 test log documents were readable; no defect log documents were separately provided, therefore defect details were derived from the defect fields embedded in the test log files.

The analyzed scope includes 25 acceptance criteria across refund management, subscription pause management, upgrade processing, cancellation workflow, and renewal reminder service. Based on the source documents, all user stories contained identifiable IDs, titles, and acceptance criteria; all test plans contained test case IDs with explicit AC mappings; all test logs contained execution results per logged test case, with two planned test cases missing execution log entries in SCM-003 and SCM-004.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | Fraud review obligation not explicitly validated by any testcase. | Fully Covered |
| SCM-002 | AC2 | Resume date required by AC is not validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date visibility is not validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date required by AC is not explicitly validated in the audit log testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes visibility is not validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase TP_SCM3_015 is planned but missing from test log; approval behavior at exact 50.00% threshold not fully executed. | Partially Covered |
| SCM-004 | AC5 | Boundary testcase TP_SCM4_015 is planned but missing from test log; approval behavior at exact $500.00 threshold not fully executed. | Partially Covered |
| SCM-005 | AC4 | Reminder date, channel used, and full delivery status capture are not fully validated; only customer/subscription IDs and failed delivery scenario are partially covered. | Partially Covered |

## Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Test case exists in test plan for SCM-003 AC5 but no execution result is present in the test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Missing Test Log | Test case exists in test plan for SCM-004 AC5 but no execution result is present in the test log. | SCM-004 | AC5 | Medium |
| UT_SCM1_014 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-002 | AC5 | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_015 | Missing Test Log | Test case exists in test plan for SCM-003 AC5 but no execution result is present in the test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_015 | Missing Test Log | Test case exists in test plan for SCM-004 AC5 but no execution result is present in the test log. | SCM-004 | AC5 | Medium |
| UT_SCM1_014 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Wording Ambiguity | Logged status is Passed, but actual result states test not yet executed, creating inconsistency in execution evidence. | SCM-002 | AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 75 |
| Total Test Logs | 73 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Partially Consistent |

## Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-001 | AC2 | DEF-SCM1-001 | UT_SCM1_005 | Notification template rendering issue |
| SCM-001 | AC5 | DEF-SCM1-002 | UT_SCM1_009 | Refund workflow synchronization error |
| SCM-002 | AC4 | DEF-SCM2-101 | TP_SCM2_008 | Pause reason not captured consistently |
| SCM-002 | AC5 | DEF-SCM2-102 | TP_SCM2_009 | Activation allowed without completed approval |
| SCM-003 | AC2 | DEF-SCM3-101 | TP_SCM3_004 | Revised billing amount not included in upgrade confirmation notification |
| SCM-003 | AC5 | DEF-SCM3-102 | TP_SCM3_009 | Manager approval workflow not initiated when price increase equals exactly 50.00% |
| SCM-004 | AC2 | DEF-SCM4-101 | TP_SCM4_004 | Applicable refund details not included in cancellation confirmation notification |
| SCM-004 | AC5 | DEF-SCM4-102 | TP_SCM4_009 | Finance team approval workflow fails for mixed currency outstanding balances |
| SCM-005 | AC2 | DEF-SCM5-101 | TP_SCM5_005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| SCM-005 | AC1 | DEF-SCM5-103 | TP_SCM5_011 | System sends reminder even when subscription expiry date is NULL |
| SCM-005 | AC5 | DEF-SCM5-104 | TP_SCM5_013 | Boundary condition error: $10,000.00 subscription flagged as high-value instead of requiring value > $10,000.00 |
| SCM-005 | AC4 | DEF-SCM5-105 | TP_SCM5_015 | Reminder log delivery status remains blank when notification channel fails |

## Conclusion

Unit test coverage is broadly established across all 25 acceptance criteria, but the quality posture is not fully compliant due to partial coverage on 7 ACs, 12 logged defects, 2 missing execution records, and 4 execution evidence inconsistencies. Remediation is required to complete missing boundary executions, correct ambiguous test logs, and add tests for omitted business obligations before this test set can be considered fully reliable for audit-quality coverage evidence.
