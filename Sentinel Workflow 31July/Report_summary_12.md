<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 4 user stories (SCM-001 to SCM-004), 20 acceptance criteria, 58 planned unit test cases, and 57 available test log entries derived directly from the uploaded source documents. All 4 user story documents contain identifiable story IDs, titles, and acceptance criteria; all 4 test plan documents contain test case IDs and acceptance-criteria mappings; all 4 test log documents contain execution results per test case, though SCM-003 is missing one logged test case execution (TP_SCM3_015), and no separate defect log documents were provided, so defect details were derived from the defect fields embedded within the test log documents.

# Test Coverage Summary

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | No testcase mapped for fraud review obligation. | Partially Covered |
| SCM-002 | AC2 | No testcase mapped for resume date inclusion in notification. | Partially Covered |
| SCM-002 | AC3 | No testcase mapped for scheduled resume date visibility in portal. | Partially Covered |
| SCM-002 | AC4 | Testcase does not explicitly validate pause start date field in audit log. | Partially Covered |
| SCM-003 | AC3 | No testcase mapped for next billing cycle changes visibility in portal. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase present in plan but missing from execution log; boundary wording in plan conflicts with AC threshold definition. | Partially Covered |
| SCM-004 | AC5 | Boundary testcase wording conflicts with AC threshold definition (“greater than $500” vs “exactly $500”). | Partially Covered |

# Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_SCM1_001 to UT_SCM1_015 | Direct | All SCM-001 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-001 | AC1-AC5 | Low |
| TP_SCM2_001 to TP_SCM2_015 | Direct | All SCM-002 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-002 | AC1-AC5 | Low |
| TP_SCM3_001 to TP_SCM3_014 | Direct | Logged SCM-003 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-003 | AC1-AC5 | Low |
| TP_SCM3_015 | Missing Test Log | Test case exists in plan and is mapped to AC5, but no corresponding execution result is present in the provided test log. | SCM-003 | AC5 | Medium |
| TP_SCM3_015 | Ambiguous | Boundary testcase states “exactly 50% triggers manager approval,” while AC5 states approval is required only when increase is greater than 50%. | SCM-003 | AC5 | High |
| TP_SCM4_001 to TP_SCM4_015 | Direct | All SCM-004 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-004 | AC1-AC5 | Low |
| TP_SCM4_015 | Ambiguous | Boundary testcase states “exactly $500 triggers finance approval,” while AC5 states approval is required only when outstanding balance is greater than $500. | SCM-004 | AC5 | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_SCM1_001 to UT_SCM1_015 | Direct | All SCM-001 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-001 | AC1-AC5 | Low |
| TP_SCM2_001 to TP_SCM2_015 | Direct | All SCM-002 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-002 | AC1-AC5 | Low |
| TP_SCM3_001 to TP_SCM3_014 | Direct | Logged SCM-003 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-003 | AC1-AC5 | Low |
| TP_SCM3_015 | Missing Test Log | Test case exists in plan and is mapped to AC5, but no corresponding execution result is present in the provided test log. | SCM-003 | AC5 | Medium |
| TP_SCM3_015 | Ambiguous | Boundary testcase states “exactly 50% triggers manager approval,” while AC5 states approval is required only when increase is greater than 50%. | SCM-003 | AC5 | High |
| TP_SCM4_001 to TP_SCM4_015 | Direct | All SCM-004 test cases are explicitly mapped to valid acceptance criteria and story ID. | SCM-004 | AC1-AC5 | Low |
| TP_SCM4_015 | Ambiguous | Boundary testcase states “exactly $500 triggers finance approval,” while AC5 states approval is required only when outstanding balance is greater than $500. | SCM-004 | AC5 | High |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 58.00 |
| Total test logs | 57.00 |
| Missing test cases | 0.00 |
| Missing test logs | 1.00 |
| consistency status | Partially Consistent due to one missing execution record and two AC-to-test boundary interpretation inconsistencies. |

# Defect Details

Defect Details:

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

# Conclusion

Overall unit test coverage is materially strong, but remediation is required for uncovered requirement elements in SCM-001 AC5, SCM-002 AC2/AC3/AC4, and SCM-003 AC3, as well as for the missing SCM-003 execution log and the AC boundary-mapping inconsistencies in SCM-003 and SCM-004. Defects affecting notification content, approval workflows, and audit completeness should be resolved and the impacted test cases re-executed before considering the test set fully compliant and complete.
