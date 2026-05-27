# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories.

The 2 user stories form the baseline reference for evaluation. The scope is restricted to unit test plans and execution records mapped to these user stories.

Included in scope:
- Unit test cases linked to the identified user stories.
- Test execution results covering executed, not executed, passed, and failed outcomes.
- Defect data directly associated with these user stories.

Excluded from scope:
- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

## Test Coverage Summary

Total Use Cases: 2

Coverage Details:

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 2 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | Medium | Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | Medium | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | High | Partially Covered |
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | Medium | Partially Covered |
| STG-001 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | Medium | Partially Covered |
| STG-001 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | High | Partially Covered |
| STG-001 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed and Customer-managed keys. | Critical | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| BRZ-001 | 70.00% | 🟠 Amber |
| STG-001 | 60.00% | 🔴 Red |

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

Total Test Cases Not Executed: 0

Total Test Cases Passed: 26

Total Test Cases Failed: 4

Execution Success Rate: 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---|---:|---:|---:|---:|---:|---:|---:|
| BRZ-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| STG-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

## Defect Details

Defect Rate: 13.33%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|---|---|---|---|---|---|---|---|
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | NULL | SHIR Offline Failure. Functionality Check: Pipeline should fail gracefully with an alert when SHIR is offline. Actual Behavior: Test failed, indicating incorrect error handling or alerting, violating AC1. | functional_validation | high | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | NULL | Incorrect Retry Count. Functionality Check: Pipeline should retry 3 times per AC4. Actual Behavior: Test failed, indicating the retry logic does not match the specified count of 3. | policy_enforcement | high | open |
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | NULL | Folder Auto-Creation Failure. Functionality Check: System should auto-create missing domain folders or reject ingestion. Actual Behavior: Test failed, suggesting data may be misplaced or ingestion fails incorrectly, violating AC2. | functional_validation | medium | open |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | NULL | Access Control Bypass. Functionality Check: User with only Bronze access must be denied access to Gold container. Actual Behavior: Test failed, indicating a severe security vulnerability where unauthorized data access is possible, violating AC5. | security | critical | open |

## Conclusion

Summary of Findings:

A total of 2 user stories were reviewed. Coverage distribution shows 0 fully covered, 2 partially covered, and 0 not covered user stories. The overall execution success rate is 86.67%, and the defect rate is 13.33%.

Final Outcome Statement:

The overall average coverage score is 65.00%, the overall execution stability is 86.70%, and the defect profile includes high and critical severity defects. Based on these reported values, the current unit test quality and coverage baseline indicates unresolved coverage gaps and open defect conditions.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps and open defects, including critical severity findings, require resolution before progression.
