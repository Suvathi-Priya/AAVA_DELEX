# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 1 user story.

The baseline for this evaluation is the identified user story: BRZ-001.

The scope is restricted to unit test cases, test execution records, and defect data mapped directly to this user story.

Included in scope:
- Unit test cases linked to the identified user story.
- Test execution results covering executed, not executed, passed, and failed outcomes.
- Defect data directly associated with the mapped user story.

Excluded from scope:
- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

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
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | Medium | 🟠 Amber - Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | Medium | 🟠 Amber - Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | Medium | 🟠 Amber - Partially Covered |

Coverage Score:

| User Story ID | Coverage Score | Color |
|---|---:|---|
| BRZ-001 | 70.00% | 🟠 Amber |

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
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|---|---|---|---|---|---|---|---|
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | NULL | SHIR Offline Test Failure. Functionality Check: Pipeline should fail gracefully with an alert when SHIR is offline. Actual Behavior: The test failed, indicating an unexpected error, no alert, or partial data write, violating AC1's dependency on SHIR. | connectivity | High | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | NULL | Retry Logic Failure. Functionality Check: Pipeline should terminate and alert after a set number of retries. Actual Behavior: The test for retry logic failed, suggesting the system does not handle persistent failures as designed, violating AC4. | resilience_and_error_handling | High | open |

Defect pattern summary:
- Total defects recorded: 2.
- Severity distribution captured in scope: 2 High.
- Affected areas: connectivity and resilience_and_error_handling.

## Conclusion

Summary of Findings:

A total of 1 user story was reviewed. Coverage distribution shows 0 fully covered, 1 partially covered, and 0 not covered user stories. Execution success rate is 86.67%, and defect rate is 13.33%.

Final Outcome Statement:

The overall coverage rate is 70.00%, the overall execution success rate is 86.67%, and the recorded defects are High severity. Based on these reported values, the unit test suite shows moderate coverage with open high-severity defects.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps and open high-severity defects require resolution before progression.
