# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 3 user stories.

The 3 user stories form the baseline reference for evaluation. The scope is restricted to unit test cases, execution records, and defect data mapped directly to these user stories.

Included in scope:
- Unit test cases linked to the identified user stories.
- Test execution results covering executed, not executed, passed, and failed records.
- Defect data directly associated with these user stories.

Excluded from scope:
- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

The analysis excludes non-unit test activities and unrelated defect categories.

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
| LZ-001 | AC1 | Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | Medium | Partially Covered |
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | Medium | Partially Covered |
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | Medium | Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | Medium | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | High | Partially Covered |
| BRZ-001 | AC5 | Schema Drift Handling: Given a change in source table schema, when the ingestion runs, then the pipeline must not fail and should capture the new columns. | Medium | Partially Covered |
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | Medium | Partially Covered |
| STG-001 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | High | Partially Covered |
| STG-001 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | Medium | Partially Covered |
| STG-001 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed and Customer-managed keys. | High | Partially Covered |

Coverage Score:

| User Story ID | Coverage Score | Color |
|---|---|---|
| LZ-001 | 80.00% | 🟠 Amber |
| BRZ-001 | 60.00% | 🔴 Red |
| STG-001 | 60.00% | 🔴 Red |

Legend:
- 🟢 Green (90–100%)
- 🟠 Amber (70–89%)
- 🔴 Red (<70%)

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
| UT_LZ-001_014 | extra_testlog | Extra execution log exists without corresponding testcase definition: UT_LZ-001_014 | LZ-001 | AC5 | Medium |

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
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | NULL | Network Security Bypass. Functionality Check: Block Dev-to-Prod connections. Actual Behavior: Connection was not blocked, violating network segmentation rules (AC4). | Critical | open |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | NULL | Tagging Policy Bypass. Functionality Check: Mandatory 'Cost Center' tag. Actual Behavior: Resource was deployed with a null 'Cost Center' tag, violating AC5. | High | open |
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | NULL | Ingestion Pipeline Failure. Functionality Check: Pipeline should fail with an alert if SHIR is offline. Actual Behavior: Pipeline did not fail as expected, violating AC1. | High | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | NULL | Incorrect Retry Logic. Functionality Check: System must retry 3 times. Actual Behavior: The system retried only once before failing, violating AC4. | High | open |
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | NULL | Incorrect Data Organization. Functionality Check: Auto-create domain folder or reject. Actual Behavior: Data was ingested into an incorrect path, violating AC2. | High | open |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | NULL | Unauthorized Access to Gold Layer. Functionality Check: Deny access to Gold for Bronze users. Actual Behavior: A user with only Bronze access was able to access the Gold container, violating AC5. | Critical | open |

## Conclusion

Summary of Findings:

A total of 3 user stories were reviewed. Coverage distribution shows 0 fully covered, 3 partially covered, and 0 not covered user stories. The overall Test Coverage Rate is 66.70%, the Execution Success Rate is 86.70%, and the Defect Rate is 13.33%.

Final Outcome Statement:

The overall Test Coverage Rate is 66.70%, which aligns to Red based on the defined coverage scoring rules. The overall Execution Success Rate is 86.70%, and the defect profile includes Critical and High severity defects.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps, execution failures, and open Critical and High severity defects require corrective action before progression.
