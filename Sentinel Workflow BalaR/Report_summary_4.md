# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 2

The 2 user stories form the baseline for evaluation, and the scope is limited to unit test coverage and execution records mapped to these user stories.

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
| SCM-004 | AC2 | No testcase explicitly validates that applicable refund details are included in the cancellation confirmation notification. | Partially Covered |
| SCM-004 | AC4 | No testcase explicitly validates that the effective date is captured in the cancellation audit log. | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| SCM-004 | 60.00% | 🔴 Red |
| SCM-005 | 100.00% | 🟢 Green |

**Legend:**

Green (90–100%) → High coverage (meets quality expectations)

Amber (70–89%) → Moderate coverage (requires attention)

Red (<70%) → Low coverage (critical gaps present)

**Coverage Score Analysis:**

Coverage Score (%) = (Fully Covered Acceptance Criteria for the User Story / Total Acceptance Criteria in the User Story) × 100

**Description:**

Coverage Score measures the extent to which the acceptance criteria of an individual user story are validated by corresponding test cases. It indicates how completely the requirements defined within that user story are covered through testing.

**Components:**

Covered Acceptance Criteria for the User Story: Number of acceptance criteria within the user story that have at least one mapped test case.

Total Acceptance Criteria in the User Story: Total number of acceptance criteria defined for that specific user story.

**Calculation Scope:**

Coverage Score must be calculated separately for each user story using only the acceptance criteria belonging to that user story. Acceptance criteria from other user stories must not be included in the calculation.

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 30

Total Test Cases Passed: 26

Total Test Cases Failed: 4

**Test Execution Summary:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| SCM-004 | 15 | 15 | 13 | 2 |
| SCM-005 | 15 | 15 | 13 | 2 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

No data available.

**Consistency Metrics Summary:**

| Metric | Count |
|--------|-------|
| Total Test Cases | 30 |
| Total Test Logs | 30 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

## Defect Details

**Defect Rate:** 13.33%

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

## Conclusion

Remediation is required as test case failures and defects exist in the unit test suite.
