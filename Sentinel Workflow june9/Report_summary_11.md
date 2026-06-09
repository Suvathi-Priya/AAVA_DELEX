# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 5 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories. The total number of user stories included in the analysis is 5, which form the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

### Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM002 | AC2 | No testcase explicitly validates that resume date is included in pause confirmation notification. | Partially Covered |
| SCM002 | AC3 | No testcase explicitly validates that customers can view scheduled resume date in the customer portal. | Partially Covered |
| SCM002 | AC4 | No testcase explicitly validates that pause start date is captured in pause audit logs. | Partially Covered |
| SCM002 | AC4 | No testcase explicitly validates that timestamp is captured in pause audit logs. | Partially Covered |
| SCM002 | AC5 | No testcase explicitly validates that manager approval is required before the pause is activated. | Partially Covered |
| SCM-003 | AC2 | No testcase explicitly validates that revised billing amount is included in upgrade confirmation notification. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates that subscription ID is captured in upgrade audit logs. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates that upgrade date is captured in upgrade audit logs. | Partially Covered |
| SCM-003 | AC5 | No testcase explicitly validates that manager approval is required before the upgrade is activated. | Partially Covered |
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that effective date is captured in cancellation audit logs. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is detailed in downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that effective date is captured in downgrade audit logs. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates that account manager approval is required for enterprise-tier plan downgrades. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates that customer retention review is required for enterprise-tier plan downgrades. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates that approval and review are required before enterprise-tier downgrade is processed. | Partially Covered |

## Test Execution Summary

| Metric | Count |
|---|---|
| Total Test Cases in All Test Plan | 75 |
| Total Test Cases in All Test Logs | 73 |
| Total Passed in All Test Logs | 66 |
| Total Failed in All Test Logs | 7 |
| Total Defects in All Test Logs | 7 |
| Overall Defect Rate Percentage | 9.33 |
| Overall Defect Rate Formula | (Total Defects / Total Test Cases) × 100 |
| Overall Defect Rate Calculation | (7 / 75) × 100 = 9.33 |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM6_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_014 | SCM-006 | AC5 | Medium |
| TP_SCM6_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_015 | SCM-006 | AC5 | Medium |

### Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 75 |
| Total Test Logs | 73 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM-101 | TP_SCM_012 | SCM002 | Pause reason not captured consistently |
| DEF-SCM-102 | TP_SCM_015 | SCM002 | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_005 | SCM-003 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_014 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-102 | TP_SCM5_015 | SCM-005 | Account manager reminder not sent when subscription value exceeds threshold but account manager assignment is pending |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |

## Conclusion

Remediation is required as test case failures and defects exist in the unit test suite.
