# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 3 user stories.

These 3 user stories form the baseline for evaluation. The scope is restricted to unit test plans, unit test execution records, and defect data mapped directly to these user stories.

Included in scope:
- Unit test cases linked to the identified user stories.
- Test execution results covering executed, not executed, passed, and failed outcomes.
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
| LZ-001 | AC1 | AC1: Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | NULL | Partially Covered |
| LZ-001 | AC5 | AC5: Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | NULL | Partially Covered |
| BRZ-001 | AC2 | AC2: Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | NULL | Partially Covered |
| BRZ-001 | AC3 | AC3: Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | NULL | Partially Covered |
| BRZ-001 | AC4 | AC4: Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | NULL | Partially Covered |
| BRZ-001 | AC5 | AC5: Schema Drift Handling: Given a change in source table schema, when the ingestion runs, then the pipeline must not fail and should capture the new columns. | NULL | Partially Covered |
| STG-001 | AC1 | AC1: Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | NULL | Partially Covered |
| STG-001 | AC2 | AC2: Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | NULL | Partially Covered |
| STG-001 | AC3 | AC3: Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | NULL | Partially Covered |
| STG-001 | AC4 | AC4: Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed and Customer-managed keys. | NULL | Partially Covered |

Coverage Score:

| User Story ID | Coverage Score | Color |
|---|---:|---|
| LZ-001 | 80.00% | 🟠 Amber |
| BRZ-001 | 60.00% | 🔴 Red |
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

Total Test Cases Executed: 45.00

Total Test Cases Passed: 39.00

Total Test Cases Failed: 6.00

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| LZ-001 | 14 | 15 | 13 | 2 |
| BRZ-001 | 15 | 15 | 13 | 2 |
| STG-001 | 15 | 15 | 13 | 2 |

Execution Success Rate = (Test cases Passed / Test Cases Executed) × 100

Execution Success Rate: 86.67%

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_LZ-001_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_LZ-001_014 | LZ-001 | AC2 | High |
| UT_LZ-001_014 | extra_testlog | Extra execution log exists without corresponding testcase definition: UT_LZ-001_014 | LZ-001 | AC2 | Medium |

Consistency Metrics Summary:

| Metric | Count |
|---|---|
| Total Test Cases | 44 |
| Total Test Logs | 45 |
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
|---|---|---|---|---|---|---|
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | NULL | Network Security Bypass. Functionality Check: Block Dev-to-Prod connections. Actual Behavior: Connection was not blocked, violating network segmentation policy and AC4. | Critical | open |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | NULL | Tagging Policy Bypass. Functionality Check: Mandatory 'Cost Center' tag. Actual Behavior: Resource was successfully deployed via Terraform with an empty tag, indicating Policy was not in Enforce mode, violating AC5. | High | open |
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | NULL | Ingestion Pipeline Failure. Functionality Check: Fail gracefully when SHIR is offline. Actual Behavior: Pipeline did not fail with a clear IR connectivity error, violating AC1. | High | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | NULL | Retry Logic Failure. Functionality Check: Terminate and alert after 3 retries. Actual Behavior: Pipeline did not terminate as expected after persistent network failure, violating AC4. | High | open |
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | NULL | Incorrect Data Ingestion Path. Functionality Check: Auto-create domain folder or reject. Actual Behavior: Data was ingested into the root of the /bronze container, violating AC2. | Medium | open |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | NULL | Privilege Escalation. Functionality Check: Deny /gold access to /bronze users. Actual Behavior: A user with only /bronze permissions was able to access the /gold container, violating AC5. | Critical | open |

## Conclusion

Summary of Findings:

A total of 3 user stories were reviewed. Coverage distribution shows 0 fully covered, 3 partially covered, and 0 not covered user stories. The overall test coverage rate is 66.70%, the execution success rate is 86.67%, and the defect rate is 13.33%.

Final Outcome Statement:

Based on the overall test coverage rate of 66.70%, overall execution success rate of 86.70%, and the presence of Critical and High severity defects, the current unit test quality and coverage results indicate unresolved coverage gaps and open defect exposure.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps, mapping inconsistencies, and open Critical and High severity defects require resolution before progression.
