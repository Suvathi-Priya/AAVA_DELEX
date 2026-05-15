# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers unit test quality and coverage results for the following user stories:

- **LZ-001** — Implement Enterprise Subscription Strategy
- **BRZ-001** — Configure Batch Ingestion from On-Prem Databases
- **STG-001** — Implement Hierarchical Namespace for Data Lake

## Test Coverage Summary

### Coverage Score

| User Story ID | Title | Total Acceptance Criteria | Fully Covered Acceptance Criteria | Partially Covered Acceptance Criteria | Coverage Status | Coverage Percentage | Coverage Formula | Mapped Testcases |
|---|---|---:|---:|---:|---|---|---|---:|
| LZ-001 | Implement Enterprise Subscription Strategy | 5 | 4 | 1 | partially_covered | 🟡 90.0% | ((4 + (0.5 × 1)) / 5) × 100 = 90.0% | 15 |
| BRZ-001 | Configure Batch Ingestion from On-Prem Databases | 5 | 3 | 2 | partially_covered | 🟡 80.0% | ((3 + (0.5 × 2)) / 5) × 100 = 80.0% | 15 |
| STG-001 | Implement Hierarchical Namespace for Data Lake | 5 | 3 | 2 | partially_covered | 🟡 80.0% | ((3 + (0.5 × 2)) / 5) × 100 = 80.0% | 15 |

### Coverage Gap Details

| User Story ID | AC ID | Coverage Status | Mapped Tests | Gap Reason |
|---|---|---|---|---|
| LZ-001 | AC5 | partially_covered | UT_LZ-001_011, UT_LZ-001_012, UT_LZ-001_013 | Explicit validation for rejecting empty or null Cost Center tag values is mapped but failed in execution (UT_LZ-001_013), so the acceptance criterion is not completely validated. |
| BRZ-001 | AC1 | partially_covered | UT_BRZ-001_001, UT_BRZ-001_002, UT_BRZ-001_014 | The explicit validation for SHIR offline handling, including failure behavior, alerting, and prevention of partial writes, is mapped but failed in execution (UT_BRZ-001_002). |
| BRZ-001 | AC3 | partially_covered | UT_BRZ-001_005, UT_BRZ-001_006 | Mapped tests validate source system and file name metadata, but no mapped testcase directly validates that load timestamp is appended to every ingested record. |
| STG-001 | AC1 | partially_covered | UT_STG-001_001, UT_STG-001_002, UT_STG-001_015 | Mapped tests only explicitly reference /bronze container creation and duplicate prevention; there is no direct testcase explicitly validating creation of all three root containers /bronze, /silver, and /gold. |
| STG-001 | AC2 | partially_covered | UT_STG-001_003, UT_STG-001_004, UT_STG-001_014 | The explicit validation for handling a missing target domain folder is mapped but only partially passed in execution (UT_STG-001_004), leaving the requirement incompletely validated. |

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
| Total Passed | 36 |
| Total Failed | 4 |
| Total Partial Pass | 5 |
| Overall Unit Test Coverage Health | Moderate |
| Overall Test Coverage Rate | 🟡 83.3% |
| Overall Execution Success Rate | 🟡 80.0% |
| Test Execution Rate | 🟢 100.0% |
| Test Pass Rate | 🟡 80.0% |
| Acceptance Criteria Partial Ratio | 🟡 33.3% |
| Average Testcases Per Story | 15.0 |
| Defect Density Per Story | 2.0 |

| Execution Status | Count |
|---|---:|
| PASS | 36 |
| FAIL | 4 |
| PARTIAL_PASS | 5 |

## Defect Details

| Defect ID | User Story ID | Testcase ID | Severity | Category | Description | Impact | Status |
|---|---|---|---|---|---|---|---|
| DEF_LZ-001_008 | LZ-001 | UT_LZ-001_008 | high | network_segmentation | Dev-to-Prod connectivity was not blocked by default during execution of the connectivity control validation. | Potential cross-environment access between Dev and Prod may violate isolation and governance controls. | open |
| DEF_LZ-001_013 | LZ-001 | UT_LZ-001_013 | medium | policy_enforcement | Deployment with empty or null Cost Center tag value was not rejected as required. | Resources may be deployed without valid financial attribution, weakening governance and chargeback accuracy. | open |
| DEF_BRZ-001_002 | BRZ-001 | UT_BRZ-001_002 | high | connectivity_runtime | When SHIR was offline, expected safe failure behavior, alerting, or prevention of partial writes was not observed correctly. | On-prem ingestion reliability and operational recovery controls are weakened; risk of incomplete or inconsistent ingestion outcomes. | open |
| DEF_BRZ-001_009 | BRZ-001 | UT_BRZ-001_009 | high | retry_logic | Persistent network failure handling after 3 retries did not behave as expected, including final failure logging and alerting. | Operational monitoring and resilience controls may fail to notify support teams after repeated ingestion failures. | open |
| DEF_STG-001_004 | STG-001 | UT_STG-001_004 | medium | folder_organization | Missing target domain folder handling did not fully satisfy expected behavior for auto-create or controlled rejection. | Data may be misrouted or ingestion may fail unclearly, reducing storage organization consistency. | open |
| DEF_STG-001_011 | STG-001 | UT_STG-001_011 | critical | access_control | A Bronze-scoped user denial scenario for Gold container access did not behave as expected during execution. | Potential unauthorized access to Gold data represents a serious confidentiality and compliance risk. | open |

## Conclusion
All three user stories are in a partially_covered state. Overall unit test coverage health is Moderate. Release readiness status is not_ready. The justification provided is: All user stories remain partially covered, and open high/critical defects exist in network isolation, retry handling, runtime failure behavior, and access control.
