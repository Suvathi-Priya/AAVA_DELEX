# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the identified user story: SLV-001.

The scope is restricted to unit test plans and execution records mapped to this user story.

Included within scope are unit test cases linked to the identified user story, test execution results (executed, not executed, passed, failed), and defect data directly associated with this user story.

Excluded from scope are integration tests, system tests, performance tests, user stories not mapped to test cases, and external or unrelated defect logs.

## Test Coverage Summary

Total Use Cases: 1

Coverage Details:

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 1 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| SLV-001 | AC3 | AC3: Deduplication Logic Given multiple records with the same Primary Key, when loading into Delta tables, then only the latest record based on the 'LoadTimestamp' must be retained. | Medium | Partially Covered |
| SLV-001 | AC5 | AC5: Schema Enforcement Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | High | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| SLV-001 | 80.00% | 🟠 Amber |

Legend:

🟢 Green (90–100%) → High coverage (meets quality expectations)

🟠 Amber (70–89%) → Moderate coverage (requires attention)

🔴 Red (<70%) → Low coverage (critical gaps present)

Coverage Score Analysis:

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

Description:

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

Components:

Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case

Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## Test Execution Summary

Total Test Cases Executed: 15

Total Test Cases Not Executed: 0

Total Test Cases Passed: 13

Total Test Cases Failed: 2

Execution Success Rate: 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---|---:|---:|---:|---:|---:|---:|---:|
| SLV-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

## Defect Details

Defect Rate: 13.33%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:

Total Defects: Total number of defects identified during the test cycle

Total Test Cases: Total number of test cases executed

Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|---|---|---|---|---|---|---|---|
| DEF_SLV-001_003 | UT_SLV-001_003 | SLV-001 | NULL | Failure to correctly quarantine or flag records with unparseable date values, violating AC1. This poses a risk of silent data corruption in the Silver layer. | Data Integrity | High | open |
| DEF_SLV-001_011 | UT_SLV-001_011 | SLV-001 | NULL | Schema enforcement failed to reject a write operation with a mismatched schema, violating AC5. The test failure indicates the operation did not fail as required. | Policy Enforcement | Critical | open |

## Conclusion

A total of 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. Execution success rate is 86.67%, and defect rate is 13.33%.

The overall coverage rate is 80.00%, the overall execution stability is 86.70%, and the recorded defect severity includes High and Critical open defects.

The current unit test suite requires remediation before progression. Coverage remains partial, execution includes failures, and open High and Critical defects are present.