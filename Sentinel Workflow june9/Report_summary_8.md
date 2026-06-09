# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 4 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories. The 4 user stories form the baseline for evaluation, covering unit test cases linked to the identified user stories and defect data directly associated with these user stories.

## Test Coverage Summary

| User Story ID | Title | Total Acceptance Criterias | Fully Covered Acceptance Criterias | Partially Covered Acceptance Criterias | Not Covered Acceptance Criterias | Coverage Score Percentage | Total Test Cases in Test Plan | Total Test Cases in Test Logs | Total Passed | Total Failed | Total Defects |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| SCM-004 | Subscription Cancellation Workflow | 5 | 3 | 2 | 0 | 60.00 | 15 | 15 | 13 | 2 | 2 |
| SCM-005 | Subscription Renewal Reminder Service | 5 | 5 | 0 | 0 | 100.00 | 15 | 15 | 13 | 2 | 2 |
| SCM-006 | Subscription Downgrade Management | 5 | 3 | 2 | 0 | 60.00 | 15 | 13 | 12 | 1 | 1 |
| SCM-007 | Subscription Transfer and Ownership Change | 5 | 2 | 3 | 0 | 40.00 | 13 | 15 | 14 | 1 | 1 |

### Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in the cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that effective date is captured in the cancellation audit log. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is included in the downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that effective date is captured in the downgrade audit log. | Partially Covered |
| SCM-007 | AC2 | No testcase explicitly validates that transfer details are included in the transfer notification. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that billing change summary is viewable in the customer portal. | Partially Covered |

## Test Execution Summary

| Metric | Value |
|---|---:|
| Total Test Cases in All Test Plan | 58 |
| Total Test Cases in All Test Logs | 58 |
| Total Passed in All Test Logs | 52 |
| Total Failed in All Test Logs | 6 |
| Total Defects in All Test Logs | 6 |
| Overall Defect Rate Percentage | 10.34 |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM6_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_014 | SCM-006 | AC5 | Medium |
| TP_SCM6_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_015 | SCM-006 | AC5 | Medium |
| TP_SCM7_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_014 | SCM-007 | AC5 | High |
| TP_SCM7_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_015 | SCM-007 | AC5 | High |

### Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 58 |
| Total Test Logs | 58 |
| Missing Test Cases | 2 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-102 | TP_SCM5_015 | SCM-005 | Account manager reminder not sent when subscription value exceeds threshold but account manager assignment is pending |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Remediation is required as multiple test cases have failed and defects exist across all user stories. The report indicates outstanding coverage gaps and execution issues that must be addressed before progression.
