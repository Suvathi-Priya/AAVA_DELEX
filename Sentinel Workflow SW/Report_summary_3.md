# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 4 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 4

The user stories included in this analysis form the baseline for evaluation:
- SCM-004: Subscription Cancellation Workflow
- SCM-005: Subscription Renewal Reminder Service  
- SCM-006: Subscription Downgrade Management
- SCM-007: Subscription Transfer and Ownership Change

The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 4 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|-------------------|-----------------|
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in the cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that the effective date is captured in the cancellation audit log. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates that the adjusted billing amount is detailed in the downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that the effective date is captured in the downgrade audit log. | Partially Covered |
| SCM-007 | AC2 | No testcase explicitly validates that transfer details are included in the transfer notification. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that the billing change summary is viewable in the customer portal. | Partially Covered |
| SCM-007 | AC5 | No testcase explicitly validates that compliance team approval is required for subscription transfers involving a change in billing entity or tax jurisdiction. | Partially Covered |
| SCM-007 | AC5 | No testcase explicitly validates that approval is required before the transfer is completed. | Partially Covered |

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 56

Total Test Cases Passed: 50

Total Test Cases Failed: 6

**Test Execution Summary Details:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| SCM-004 | 15 | 15 | 13 | 2 |
| SCM-005 | 15 | 15 | 13 | 2 |
| SCM-006 | 15 | 13 | 12 | 1 |
| SCM-007 | 13 | 13 | 12 | 1 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|--------------|------------------|-------------|---------------|-------|--------------|
| TP_SCM6_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_014 | SCM-006 | AC5 | Medium |
| TP_SCM6_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_015 | SCM-006 | AC5 | Medium |

**Consistency Metrics Summary:**

| Metric | Count |
|--------|-------|
| Total Test Cases | 58 |
| Total Test Logs | 56 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

**Defect Rate:** 10.34%

**Defect Rate Analysis:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

Total Defects: Total number of defects identified during the test cycle

Total Test Cases: Total number of test cases executed

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-102 | TP_SCM5_015 | SCM-005 | Account manager reminder not sent when subscription value exceeds threshold but account manager assignment is pending |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Remediation is required as test case failures and defects exist in the system. The report identifies 6 failed test cases and 6 defects across all user stories, along with coverage gaps in critical acceptance criteria that require immediate attention before progression.
