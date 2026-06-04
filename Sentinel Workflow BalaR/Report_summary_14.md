# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Total User Stories:** 1

The user stories form the baseline for evaluation, and the scope is limited to unit test coverage and execution records mapped to these user stories.

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
|--------|-------|-------------|
| Fully Covered | 0 | User stories where all acceptance criteria are Fully Covered |
| Partially Covered | 1 | User stories containing one or more Partially Covered acceptance criteria |
| Not Covered | 0 | User stories where all acceptance criteria are Not Covered |

**Coverage Gap Details:**

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|-------------------|-----------------|
| SCM-007 | AC2 | No testcase explicitly validates that transfer details are included in the notification. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that the outgoing owner can view billing change summary in the customer portal. | Partially Covered |
| SCM-007 | AC3 | No testcase explicitly validates that the incoming owner can view billing change summary in the customer portal. | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| SCM-007 | 60.00% | 🔴 Red |

**Coverage Score Analysis:**

Coverage Score (%) = (Fully Covered Acceptance Criteria for the User Story / Total Acceptance Criteria in the User Story) × 100

**Description:**
Coverage Score measures the extent to which the acceptance criteria of an individual user story are validated by corresponding test cases. It indicates how completely the requirements defined within that user story are covered through testing.

**Components:**
- Covered Acceptance Criteria for the User Story: Number of acceptance criteria within the user story that have at least one mapped test case
- Total Acceptance Criteria in the User Story: Total number of acceptance criteria defined for that specific user story

**Calculation Scope:**
Coverage Score must be calculated separately for each user story using only the acceptance criteria belonging to that user story. Acceptance criteria from other user stories must not be included in the calculation.

## Test Execution Summary

**Overall Test Execution Summary:**

Total Test Cases Executed: 15

Total Test Cases Passed: 13

Total Test Cases Failed: 2

**Test Execution Summary:**

| User Story ID | Total Test Cases | Executed | Passed | Failed |
|---------------|------------------|----------|--------|--------|
| SCM-007 | 15 | 15 | 13 | 2 |

## Consistency Analysis

**Data Mapping Inconsistency Details:**

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|--------------|------------------|-------------|---------------|-------|--------------|
| TP_SCM6_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_001 | NULL | AC1 | High |
| TP_SCM6_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_002 | NULL | AC1 | High |
| TP_SCM6_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_003 | NULL | AC1 | High |
| TP_SCM6_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_004 | NULL | AC2 | High |
| TP_SCM6_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_005 | NULL | AC2 | High |
| TP_SCM6_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_006 | NULL | AC2 | High |
| TP_SCM6_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_007 | NULL | AC3 | High |
| TP_SCM6_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_008 | NULL | AC3 | High |
| TP_SCM6_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_009 | NULL | AC3 | High |
| TP_SCM6_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_010 | NULL | AC4 | High |
| TP_SCM6_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_011 | NULL | AC4 | High |
| TP_SCM6_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_012 | NULL | AC4 | High |
| TP_SCM6_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_013 | NULL | AC5 | High |
| TP_SCM6_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_014 | NULL | AC5 | High |
| TP_SCM6_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_015 | NULL | AC5 | High |

**Consistency Metrics Summary:**

| Metric | Count |
|--------|-------|
| Total Test Cases | 15 |
| Total Test Logs | 30 |
| Missing Test Cases | 15 |
| Missing Test Logs | 0 |
| Consistency Status | Mismatch Detected |

## Defect Details

**Defect Rate:** 13.33%

**Defect Rate Analysis:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**
Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_014 | SCM-007 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |

## Conclusion

Remediation is required as test case failures and defects exist in the unit test suite.
