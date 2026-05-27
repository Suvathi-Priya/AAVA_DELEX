# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the following user story:
- SLV-001

The scope is restricted to unit test cases, test execution records, and defect data mapped to this user story.

Included in scope:
- Unit test cases linked to the identified user story
- Test execution results covering executed, not executed, passed, and failed outcomes
- Defect data directly associated with the identified user story

Excluded from scope:
- Integration tests, system tests, and performance tests
- User stories not mapped to test cases
- External or unrelated defect logs

The identified user story forms the baseline reference for measuring test coverage, execution success, and defect quality.

## Test Coverage Summary

Total Use Cases: 1

Coverage Details:

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 1 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | NULL | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| SLV-001 | AC3 | Given multiple records with the same Primary Key, when loading into Delta tables, then only the latest record based on the 'LoadTimestamp' must be retained. | NULL | Partially Covered |
| SLV-001 | AC5 | Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | NULL | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| SLV-001 | 80.00% | 🟠 Amber |

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

Total Test Cases Executed: 15

Total Test Cases Passed: 13

Total Test Cases Failed: 2

Execution Success Rate = (Test Cases Passed / Test Cases Executed) × 100 = (13 / 15) × 100 = 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| SLV-001 | 15 | 15 | 13 | 2 |

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | NULL | NULL | NULL | NULL | NULL |

Consistency Metrics Summary:

| Metric | Count |
|---|---|
| Total Test Cases | 15 |
| Total Test Logs | 15 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Extra Test Cases | 0 |
| Extra Test Logs | 0 |
| Consistency Status | Matched |

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
|---|---|---|---|---|---|---|
| DEF_SLV-001_003 | UT_SLV-001_003 | SLV-001 | NULL | Validate behavior when a date column contains an unparseable value that cannot be converted to ISO 8601. Defect raised for investigation and fix. | High | open |
| DEF_SLV-001_011 | UT_SLV-001_011 | SLV-001 | NULL | Verify that a Delta table write operation fails when the incoming data schema does not match the Silver table definition. Defect raised for investigation and fix. | High | open |

Defect pattern summary:
- Total defects identified: 2
- Severity present: High
- Affected areas: functional_validation, policy_enforcement

## Conclusion

Summary of Findings:
- Total user stories reviewed: 1
- Coverage distribution: 0 fully covered, 1 partially covered, NULL not covered
- Execution success rate: 86.67%
- Defect rate: 13.33%

Final Outcome Statement:
The overall test coverage rate is 80.00%, the overall execution success rate is 86.70%, and the identified defect severity is High. Based on these reported values, the unit test suite shows partial coverage with open high-severity defects.

Conclusion Statement:
The current unit test suite is not sufficient to proceed without remediation. Coverage alignment gaps and open high-severity defects require correction before progression.
