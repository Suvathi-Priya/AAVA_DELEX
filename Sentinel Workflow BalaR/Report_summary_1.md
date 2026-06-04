# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 2

The user stories SCM-006 and SCM-007 form the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

**Coverage Details:**

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 2 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is detailed in the downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that effective date is captured in downgrade audit logs. | Partially Covered |
| SCM-007 | AC2 | No testcase explicitly validates that transfer details are included in the transfer notification. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that outgoing owner can view billing change summary in the customer portal. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that incoming owner can view billing change summary in the customer portal. | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---|---:|---|
| SCM-006 | 60.00% | 🔴 Red |
| SCM-007 | 60.00% | 🔴 Red |

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 30

Total Test Cases Passed: 26

Total Test Cases Failed: 4

**Test Execution Summary:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| SCM-006 | 15 | 15 | 13 | 2 |
| SCM-007 | 15 | 15 | 13 | 2 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

No inconsistency details provided.

**Consistency Metrics Summary:**

| Metric | Count |
|---|---|
| Total Test Cases | 30 |
| Total Test Logs | 30 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_014 | SCM-006 | Approval workflow bypassed when downgrade is initiated by a system administrator role |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Remediation is required as test case failures and defects exist in the unit test suite.
