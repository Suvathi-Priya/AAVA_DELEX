# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories.

These 2 user stories form the baseline reference for evaluation.

The scope is restricted to unit test cases, unit test execution records, and defect data directly mapped to these user stories.

Included in this analysis:

- Unit test cases linked to the identified user stories.
- Test execution results, including executed, not executed, passed, and failed status records.
- Defect data directly associated with these user stories.

Excluded from this analysis:

- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

## Test Coverage Summary

Total Use Cases: 2

Coverage Details:

| Metric | Count | Description |
|--------------------|-------|-----------------------------------------------------------------------------|
| Fully Covered | 2 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 0 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---------------|-------|---------------------|--------------|-----------------|
| NULL | NULL | NULL | NULL | NULL |

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| LZ-001 | 100.00% | 🟢 Green |
| STG-001 | 100.00% | 🟢 Green |

Legend:

- 🟢 Green (90–100%) → High coverage (meets quality expectations)
- 🟠 Amber (70–89%) → Moderate coverage (requires attention)
- 🔴 Red (<70%) → Low coverage (critical gaps present)

Coverage Score Analysis:

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

Description:

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

Components:

- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## Test Execution Summary

Total Test Cases Executed: 30

Total Test Cases Passed: 26

Total Test Cases Failed: 4

Execution Success Rate = (Test Cases Passed / Test Cases Executed) × 100 = 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---------------|------------------|----------------|--------|--------|
| LZ-001 | 14 | 15 | 13 | 2 |
| STG-001 | 15 | 15 | 13 | 2 |

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---------------|------------------|-------------|----------------|-------|---------------|
| UT_LZ-001_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_LZ-001_014 | LZ-001 | AC2 | High |
| UT_LZ-001_014 | extra_testlog | Extra execution log exists without corresponding testcase definition: UT_LZ-001_014 | LZ-001 | AC2 | Medium |

Consistency Metrics Summary:

| Metric | Count |
|---------|-------|
| Total Test Cases | 29 |
| Total Test Logs | 30 |
| Missing Test Cases | 1 |
| Missing Test Logs | 0 |
| Extra Test Cases | 0 |
| Extra Test Logs | 1 |
| Consistency Status | Mismatch Detected |

## Defect Details

Defect Rate: 13.33%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:

- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Severity | Status |
|-----------|--------------|---------------|--------------|--------------------|----------|--------|
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | NULL | Verify that a network connection attempt from a Dev environment resource to a Pr. Defect raised for investigation and fix. | NULL | NULL |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | NULL | Validate tag enforcement when the Cost Center tag is present but has an empty or. Defect raised for investigation and fix. | NULL | NULL |
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | NULL | Validate ingestion behavior when the target domain folder within /bronze does no. Defect raised for investigation and fix. | NULL | NULL |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | NULL | Verify that a user with only /bronze access is denied when attempting to read fr. Defect raised for investigation and fix. | NULL | NULL |

## Conclusion

Summary of Findings:

A total of 2 user stories were reviewed. Coverage distribution shows 2 fully covered, 0 partially covered, and 0 not covered user stories. The execution success rate is 86.67%, and the defect rate is 13.33%.

Final Outcome Statement:

The reported data shows an overall coverage rate of 100.00%, execution stability of 86.67%, and defect severity rate of NULL. Coverage is Green based on the defined scoring rules, while execution results and recorded defects indicate open quality issues in the current unit test cycle.

Conclusion Statement:

The current unit test suite demonstrates complete mapped coverage for the evaluated user stories, but remediation is required for failed executions, recorded defects, and mapping inconsistencies before progression.
