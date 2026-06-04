# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Coverage Boundary:** The total number of user stories included in the analysis is 2, which form the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

**Inclusions:** Unit test cases linked to the identified user stories, test execution results (executed, not executed, passed, failed), and defect data directly associated with these user stories.

**Exclusions:** Integration tests, system tests, performance tests, and user stories not mapped to test cases.

**Baseline Definition:** The 2 user stories serve as the baseline reference for measuring coverage, execution success, and defect quality.

## Test Coverage Summary

**Total User Stories:** 2

### Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-003 | AC2 | No testcase explicitly validates revised billing amount inclusion in notification. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates subscription ID capture in upgrade audit log. | Partially Covered |
| SCM-003 | AC4 | No testcase explicitly validates upgrade date capture in upgrade audit log. | Partially Covered |
| SCM-004 | AC2 | No testcase explicitly validates refund details inclusion in cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates effective date capture in cancellation audit log. | Partially Covered |

### Coverage Score

| User Story ID | Coverage Score | Color |
|---|---:|---|
| SCM-003 | 60.00% | 🔴 Red |
| SCM-004 | 60.00% | 🔴 Red |

## Test Execution Summary

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| SCM-003 | 15 | 15 | 13 | 2 |
| SCM-004 | 15 | 15 | 13 | 2 |

## Consistency Analysis

### Data Mapping Inconsistency Details

No inconsistencies reported.

### Consistency Metrics Summary

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
| DEF-SCM3-101 | TP_SCM3_005 | SCM-003 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_014 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_005 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_014 | SCM-004 | Finance team approval workflow fails to initiate for accounts with mixed currency outstanding balances |

## Conclusion

The report indicates that remediation is required as test cases have failed and defects exist in the system.
