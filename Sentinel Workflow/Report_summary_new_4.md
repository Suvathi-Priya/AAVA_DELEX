# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 2 user stories.

These user stories form the baseline for evaluation: LZ-001 and BRZ-001.

The scope is restricted to unit test cases linked to these user stories, associated test execution results, and defect data directly mapped to these user stories.

Included in scope:
- Unit test cases linked to the identified user stories.
- Test execution results, including executed, not executed, passed, and failed outcomes.
- Defect records directly associated with these user stories.

Excluded from scope:
- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

These user stories are the baseline reference for measuring coverage, execution success, and defect quality.

## 2. Test Coverage Summary

**Total Use Cases:** 2

### Coverage Details

| Metric | Count | Description |
|--------------------|-------|-----------------------------------------------------------------------------|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 2 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

### Coverage Gap Details

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|----------------|-------|---------------------|--------------|-----------------|
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | NULL | Partially Covered |
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | NULL | Partially Covered |

| User Story ID | Coverage Score | Color |
|----------------|----------------|-------|
| LZ-001 | 90.00% | 🟢 Green |
| BRZ-001 | 90.00% | 🟢 Green |

**Legend:**

- 🟢 Green (90–100%) → High coverage (meets quality expectations)
- 🟠 Amber (70–89%) → Moderate coverage (requires attention)
- 🔴 Red (<70%) → Low coverage (critical gaps present)

### Coverage Score Analysis

**Formula:**

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

**Description:**

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

**Components:**
- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case.
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories.

## 3. Test Execution Summary

**Total Test Cases Executed:** 30

**Total Test Cases Not Executed:** 0

**Total Test Cases Passed:** 26

**Total Test Cases Failed:** 4

**Execution Success Rate:** 86.67%

Execution results show 30.00 executed test cases out of 30.00 total test cases, with 26.00 passed and 4.00 failed. Failed executions are associated with LZ-001 and BRZ-001.

### Test Execution Summary Details

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|----------------|------------------|----------|--------------|--------|--------|----------------|-----------|
| LZ-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| BRZ-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

## 4. Defect Details

**Defect Rate:** 13.33%

### Defect Rate Analysis

**Formula:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**
- Total Defects: Total number of defects identified during the test cycle.
- Total Test Cases: Total number of test cases executed.

### Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|-----------|--------------|---------------|--------------|--------------------|----------|----------|--------|
| DEF_LZ-001_008 | UT_LZ-001_008 | LZ-001 | Dev-to-Prod connection blocking not observed | Dev-to-Prod connection blocking was not observed as expected during execution. | network_segmentation | high | open |
| DEF_LZ-001_013 | UT_LZ-001_013 | LZ-001 | Cost Center tag enforcement for empty or null value not observed | Cost Center tag enforcement for empty or null value was not observed as expected during execution. | policy_enforcement | high | open |
| DEF_BRZ-001_002 | UT_BRZ-001_002 | BRZ-001 | SHIR offline failure handling and alerting not observed | Expected SHIR offline failure handling, alerting, and prevention of partial writes were not observed during execution. | integration_runtime_connectivity | high | open |
| DEF_BRZ-001_009 | UT_BRZ-001_009 | BRZ-001 | Retry termination after 3 attempts with alerting not observed | Expected termination after 3 retries with detailed alerting was not observed during execution. | retry_logic | high | open |

All 4.00 recorded defects are high severity and remain open. Defects are distributed across both user stories and affect network segmentation, policy enforcement, integration runtime connectivity, and retry logic.

## 5. Conclusion

A total of 2 user stories were reviewed. Coverage distribution is 0 fully covered, 2 partially covered, and 0 not covered. The overall unit test coverage rate is 90.00%, the execution success rate is 86.67%, and the defect rate is 13.33%.

Based on the reported overall coverage rate of 90.00%, release readiness status of At Risk, execution success rate of 86.67%, and 4.00 open high-severity defects, remediation is required before progression.

The current unit test suite is not sufficient to proceed without remediation. Coverage gaps and open high-severity defects should be resolved before progression.
