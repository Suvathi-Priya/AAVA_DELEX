# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 3 user stories.

These user stories form the baseline for evaluation. The scope is restricted to unit test plans, unit test execution records, and defect data mapped directly to these user stories.

Included in scope:

- Unit test cases linked to the identified user stories.
- Test execution results covering executed, not executed, passed, and failed outcomes.
- Defect data directly associated with these user stories.

Excluded from scope:

- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

The baseline reference for measuring coverage, execution success, and defect quality is limited to the following user stories: LZ-001, BRZ-001, and STG-001.

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
| LZ-001 | AC1 | Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | High | Partially Covered |
| LZ-001 | AC2 | Resource Group Alignment: Given a new project onboarding, when resources are deployed, then they must be grouped into Resource Groups based on the environment. | High | Partially Covered |
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | High | Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | High | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | High | Partially Covered |
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | High | Partially Covered |
| STG-001 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | High | Partially Covered |
| STG-001 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | High | Partially Covered |
| STG-001 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed and Customer-managed keys. | High | Partially Covered |

Coverage Score:

| User Story ID | Coverage Score | Color |
|---|---:|---|
| LZ-001 | 80.0% | 🟠 Amber |
| BRZ-001 | 70.0% | 🟠 Amber |
| STG-001 | 60.0% | 🔴 Red |

## Test Execution Summary

Total Test Cases Executed: 44

Total Test Cases Passed: 38

Total Test Cases Failed: 6

Execution Success Rate = (Total Passed / Total Executed) * 100 = 86.4%

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---|---:|---:|---:|---:|
| LZ-001 | 14 | 14 | 12 | 2 |
| BRZ-001 | 15 | 15 | 12 | 3 |
| STG-001 | 15 | 15 | 13 | 2 |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Severity | Category | Description | Impact | Status |
|---|---|---|---|---|---|---|---|
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | High | policy_enforcement | Verify that a network connection attempt from a Dev environment resource to a Pr. Defect raised for investigation and fix. | Potential for unauthorized cross-environment data access, violating security and isolation principles. | open |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | High | policy_enforcement | Validate tag enforcement when the Cost Center tag is present but has an empty or. Defect raised for investigation and fix. | Resources can be deployed without proper cost allocation, leading to financial tracking and reporting inaccuracies. | open |
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | High | reliability_failure | Validate pipeline behavior when the Self-Hosted Integration Runtime is offline d. Defect raised for investigation and fix. | Data ingestion pipeline is not resilient to IR outages, leading to data availability delays and potential data loss. | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | High | reliability_failure | Validate retry logic when network failure persists beyond 3 attempts. Defect raised for investigation and fix. | Incorrect retry logic can lead to premature pipeline failure and excessive alerting, impacting data ingestion reliability. | open |
| DEF_STG-001_004 | UT_STG-001_004 | STG-001 | Medium | functional_degradation | Validate ingestion behavior when the target domain folder within /bronze does no. Defect raised for investigation and fix. | Ingestion process may fail or misplace data if domain folders are not handled correctly, affecting data organization. | open |
| DEF_STG-001_011 | UT_STG-001_011 | STG-001 | Critical | access_control_failure | Verify that a user with only /bronze access is denied when attempting to read fr. Defect raised for investigation and fix. | Access control is not properly enforced, allowing unauthorized users to access sensitive data in the Gold layer. | open |

## Conclusion

A total of 3 user stories were reviewed. Coverage distribution shows 0 fully covered, 3 partially covered, and 0 not covered user stories. The overall test coverage rate is 70.0%, the execution success rate is 86.4%, and the current results indicate partial coverage with open defect conditions remaining.