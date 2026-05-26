# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the identified user story: BRZ-001.

The scope is restricted to unit test cases linked to this user story, associated test execution results (executed, not executed, passed, failed), and defect data directly associated with this user story.

This analysis excludes integration tests, system tests, performance tests, user stories not mapped to test cases, and external or unrelated defect logs.

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
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | Medium | Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | Medium | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | Medium | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| BRZ-001 | 70.00% | 🟠 Amber |

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
| BRZ-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

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
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | NULL | Validate pipeline behavior when the Self-Hosted Integration Runtime is offline d. Defect raised for investigation and fix. | Functional | High | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | NULL | Validate retry logic when network failure persists beyond 3 attempts. Defect raised for investigation and fix. | Functional | High | open |

Defect pattern summary: 2 defects were recorded for BRZ-001. Both defects are in the Functional category, both are High severity, and both remain open.

## Conclusion

Summary of Findings:

A total of 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. Execution Success Rate is 86.67%, and Defect Rate is 13.33%.

Final Outcome Statement:

The overall test coverage rate is 70.00%, the overall execution success rate is 86.70%, and recorded defect severity is High for 2 defects. Based on these reported values, the unit test suite shows Amber coverage status for BRZ-001 with open High severity defects present.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps and open High severity defects require resolution before progression.
