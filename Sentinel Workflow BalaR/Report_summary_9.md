# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 2

The user stories SCM-003 and SCM-004 form the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Test Coverage Summary

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 2 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|-------------------|-----------------|
| SCM-003 | AC2 | No testcase explicitly validates that revised billing amount is included in the upgrade confirmation notification. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates that subscription ID is captured in the upgrade audit log. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates that upgrade date is captured in the upgrade audit log. | Partially Covered |
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in the cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that effective date is captured in the cancellation audit log. | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| SCM-003 | 60.00% 🔴 | Red |
| SCM-004 | 60.00% 🔴 | Red |

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 30

Total Test Cases Passed: 26

Total Test Cases Failed: 4

**Test Execution Summary:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| SCM-003 | 15 | 15 | 13 | 2 |
| SCM-004 | 15 | 15 | 13 | 2 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

| Detail | Value |
|--------|-------|
| Mapping inconsistency details | None |

**Consistency Metrics Summary:**

| Metric | Count |
|--------|-------|
| Total Test Cases | 30 |
| Total Test Logs | 30 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-SCM3-101 | TP_SCM3_005 | SCM-003 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_014 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |

## Conclusion

Remediation is required as test case failures and defects exist in the unit test suite.
