# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers unit test quality and coverage for the following user stories:

- **LZ-001** — Implement Enterprise Subscription Strategy
- **BRZ-001** — Configure Batch Ingestion from On-Prem Databases
- **STG-001** — Implement Hierarchical Namespace for Data Lake

## Test Coverage Summary

### Coverage Score

| User Story ID | Title | Total Acceptance Criteria | Fully Covered Acceptance Criteria | Partially Covered Acceptance Criteria | Coverage Status | Coverage Percentage | Coverage Formula | Mapped Testcases | Coverage Indicator |
|---|---|---:|---:|---:|---|---|---|---:|---|
| LZ-001 | Implement Enterprise Subscription Strategy | 5 | 4 | 1 | partially_covered | 90.0% | ((4 + (0.5 × 1)) / 5) × 100 = 90.0% | 15 | 🟡 partially_covered |
| BRZ-001 | Configure Batch Ingestion from On-Prem Databases | 5 | 3 | 2 | partially_covered | 70.0% | ((3 + (0.5 × 2)) / 5) × 100 = 70.0% | 15 | 🟡 partially_covered |
| STG-001 | Implement Hierarchical Namespace for Data Lake | 5 | 3 | 2 | partially_covered | 70.0% | ((3 + (0.5 × 2)) / 5) × 100 = 70.0% | 15 | 🟡 partially_covered |

### Coverage Gap Details

| User Story ID | AC ID | AC Description | Coverage Status | Mapped Tests | Gap Reason | Coverage Indicator |
|---|---|---|---|---|---|---|
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | partially_covered | UT_LZ-001_011, UT_LZ-001_012, UT_LZ-001_013 | Execution evidence shows the empty/null Cost Center boundary validation failed in UT_LZ-001_013, so explicit rejection of invalid tag values is not completely satisfied. | 🟡 partially_covered |
| BRZ-001 | AC1 | Connectivity Verification: Given an ADF pipeline, when connecting to an on-prem SQL database, then it must use a Self-Hosted Integration Runtime. | partially_covered | UT_BRZ-001_001, UT_BRZ-001_002, UT_BRZ-001_014 | Although direct validation exists, execution evidence shows SHIR offline handling failed in UT_BRZ-001_002, so the explicit connectivity failure validation is incomplete. | 🟡 partially_covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | partially_covered | UT_BRZ-001_005, UT_BRZ-001_006 | Mapped tests validate source system and file name handling, but explicit direct validation of load timestamp append behavior is not clearly covered by any mapped testcase. | 🟡 partially_covered |
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | partially_covered | UT_STG-001_001, UT_STG-001_002, UT_STG-001_015 | Mapped tests directly validate /bronze creation and hierarchical namespace enablement, but do not explicitly validate creation of /silver and /gold root containers. | 🟡 partially_covered |

## Test Execution Summary

| Metric | Value |
|---|---|
| Total User Stories | 3 |
| Total Acceptance Criteria | 15 |
| Fully Covered Acceptance Criteria | 10 |
| Partially Covered Acceptance Criteria | 5 |
| Total Testcases | 45 |
| Total Executed | 45 |
| Total Not Executed | 0 |
| Total Passed | 39 |
| Total Failed | 6 |
| Overall Unit Test Coverage Health | Moderate |
| Release Readiness | Not Ready |
| Overall Test Coverage Rate | 83.3% |
| Overall Execution Success Rate | 86.7% |
| Test Execution Rate | 100.0% |
| Test Pass Rate | 86.7% |
| Acceptance Criteria Partial Ratio | 33.3% |
| Average Testcases Per Story | 15.0 |
| Defect Density Per Story | 2.0 |
| Security Defect Count | 3 |

## Defect Details

| Defect ID | User Story ID | Testcase ID | Severity | Category | Description | Impact | Status |
|---|---|---|---|---|---|---|---|
| DEF_LZ-001_008 | LZ-001 | UT_LZ-001_008 | high | network_segmentation | Dev-to-Prod connection blocking did not behave as expected during connectivity validation. | Potential unauthorized cross-environment access between Dev and Prod, violating isolation controls. | open |
| DEF_LZ-001_013 | LZ-001 | UT_LZ-001_013 | medium | policy_enforcement | Empty or null Cost Center tag value was not rejected as expected during deployment validation. | Resources may be deployed without valid financial attribution, weakening governance and chargeback accuracy. | open |
| DEF_BRZ-001_002 | BRZ-001 | UT_BRZ-001_002 | high | connectivity_runtime | Pipeline behavior when Self-Hosted Integration Runtime was offline did not match expected failure-handling behavior. | On-prem ingestion reliability and operational alerting are compromised during runtime outages. | open |
| DEF_BRZ-001_009 | BRZ-001 | UT_BRZ-001_009 | high | retry_logic | Pipeline did not correctly terminate after 3 retries and alert with expected details under persistent network failure. | Failure recovery controls and incident response visibility are weakened, risking delayed remediation and unstable ingestion. | open |
| DEF_STG-001_004 | STG-001 | UT_STG-001_004 | medium | data_organization | Ingestion behavior for missing target domain folder did not match expected auto-create or controlled rejection behavior. | Files may land in incorrect locations or ingestion may fail inconsistently, reducing data lake organization integrity. | open |
| DEF_STG-001_011 | STG-001 | UT_STG-001_011 | critical | access_control | User with only Bronze access was not denied Gold container access as expected. | Unauthorized access to Gold data is possible, creating a significant confidentiality and compliance risk. | open |

## Conclusion
The report reflects the validated input data across Scope, Test Coverage Summary, Test Execution Summary, Defect Details and Conclusion. Coverage status breakdown shows 3 partially_covered user stories. Overall unit test coverage health is Moderate, and release readiness is Not Ready.