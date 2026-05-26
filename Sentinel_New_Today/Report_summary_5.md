# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 3 user stories.

These 3 user stories form the baseline for evaluation. The scope is restricted to unit test plans, unit test execution records, and defect data mapped directly to these user stories.

Included in scope:

- Unit test cases linked to the identified user stories.
- Test execution results covering executed, not executed, passed, and failed records.
- Defect data directly associated with these user stories.

Excluded from scope:

- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

The baseline reference for measuring coverage, execution success, and defect quality is limited to the mapped user stories: LZ-001, BRZ-001, and STG-001.

## Test Coverage Summary

Total Use Cases: 3

Coverage Details:

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 3 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| LZ-001 | AC1 | Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | NULL | Partially Covered |
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | NULL | Partially Covered |
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | NULL | Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | NULL | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | NULL | Partially Covered |
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | NULL | Partially Covered |
| STG-001 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | NULL | Partially Covered |
| STG-001 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | NULL | Partially Covered |
| STG-001 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed and Customer-managed keys. | NULL | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| LZ-001 | 80.00% | 🟠 Amber |
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

Total Test Cases Executed: 45

Total Test Cases Passed: 39

Total Test Cases Failed: 6

Execution Success Rate = (Test cases Passed / Test Cases Executed) × 100 = 86.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| LZ-001 | 14 | 15 | 13 | 2 |
| BRZ-001 | 15 | 15 | 13 | 2 |
| STG-001 | 15 | 15 | 13 | 2 |

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_LZ-001_014 | extra_testlog | Extra execution log exists without corresponding testcase definition: UT_LZ-001_014 | NULL | NULL | Medium |

Consistency Metrics Summary:

| Metric | Count |
|---|---|
| Total Test Cases | 44 |
| Total Test Logs | 45 |
| Missing Test Cases | 0 |
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

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Severity | Status |
|---|---|---|---|---|---|---|
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | NULL | Network Connectivity Failure. Functionality Check: Dev to Prod connection block. Actual Behavior: Connection was not blocked, violating AC4. | High | open |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | NULL | Tag Validation Failure. Functionality Check: Empty tag value rejection. Actual Behavior: Policy did not reject deployment with an empty tag value, violating AC5. | Medium | open |
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | NULL | SHIR Offline Failure. Functionality Check: Pipeline failure on IR offline. Actual Behavior: Pipeline did not fail gracefully when SHIR was offline, violating AC1. | High | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | NULL | Retry Logic Failure. Functionality Check: 3 retries on failure. Actual Behavior: Pipeline did not retry 3 times as required, violating AC4. | High | open |
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | NULL | Folder Creation Failure. Functionality Check: Auto-creation of domain folder. Actual Behavior: System did not auto-create the missing domain folder, violating AC2. | Medium | open |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | NULL | Access Control Failure. Functionality Check: Deny access to Gold container. Actual Behavior: User with only Bronze access was not denied access to the Gold container, violating AC5. | Critical | open |

Defect pattern summary:

- Total defects: 6
- Severity distribution includes 1 Critical, 3 High, and 2 Medium defects.
- Affected user stories: LZ-001, BRZ-001, and STG-001.
- Defect categories present include policy enforcement, incorrect validation behavior, retry reliability failure, organizational pathing issue, and access control failure.

## Conclusion

Summary of Findings:

A total of 3 user stories were reviewed. Coverage distribution shows 0 fully covered, 3 partially covered, and 0 not covered user stories. Overall test coverage rate is 70.00%, execution success rate is 86.70%, and defect rate is 13.33%.

Final Outcome Statement:

Based on the overall test coverage rate of 70.00%, overall execution success rate of 86.70%, and the presence of Critical, High, and Medium severity defects, the current unit test results indicate partial coverage with open defect conditions remaining.

Conclusion Statement:

The current unit test suite is not sufficient for progression without remediation. Coverage gaps, mapping inconsistency, and open defects require resolution before proceeding.
