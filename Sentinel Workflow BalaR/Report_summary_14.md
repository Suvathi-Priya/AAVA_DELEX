# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 4 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 4

The 4 user stories form the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

**Inclusions:**
- Unit test cases linked to the identified user stories
- Test execution results (executed, not executed, passed, failed)
- Defect data directly associated with these user stories

**Exclusions:**
- Integration tests, system tests, or performance tests
- User stories not mapped to test cases

## Test Coverage Summary

**Coverage Details:**

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 4 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in the cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that effective date is captured in the cancellation audit log. | Partially Covered |
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is included in the downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that effective date is captured in the downgrade audit log. | Partially Covered |
| SCM-007 | AC2 | No testcase explicitly validates that transfer details are included in the transfer notification. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that billing change summary is viewable in the customer portal. | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---|---:|---|
| SCM-004 | 60.00% | 🔴 Red |
| SCM-005 | 100.00% | 🟢 Green |
| SCM-006 | 60.00% | 🔴 Red |
| SCM-007 | 40.00% | 🔴 Red |

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 60

Total Test Cases Passed: 52

Total Test Cases Failed: 8

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| SCM-004 | 15 | 15 | 13 | 2 |
| SCM-005 | 15 | 15 | 13 | 2 |
| SCM-006 | 15 | 15 | 13 | 2 |
| SCM-007 | 15 | 15 | 13 | 2 |

## Consistency Analysis

| Metric | Count |
|---|---|
| Total Test Cases | 60 |
| Total Test Logs | 60 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

**Defect Rate:** 13.33%

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-102 | TP_SCM5_015 | SCM-005 | Account manager reminder not sent when subscription value exceeds threshold but account manager assignment is pending |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_014 | SCM-006 | Approval workflow bypassed when downgrade is initiated by a system administrator role |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

The report indicates that remediation is required as test case failures and defects exist across all user stories. Coverage gaps and execution failures must be addressed before progression.