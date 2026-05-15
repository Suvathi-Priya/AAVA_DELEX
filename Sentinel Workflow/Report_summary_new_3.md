# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 3 user stories. These user stories form the baseline for evaluation.

The scope is restricted to unit test cases, test execution records, and defect-related execution outcomes mapped to these user stories. Included in this analysis are unit test cases linked to the identified user stories, test execution results (executed, not executed, passed, failed), and defect-related failed test evidence directly associated with these user stories.

Analysis excludes integration tests, system tests, performance tests, user stories not mapped to test cases, and any external or unrelated defect logs.

## 2. Test Coverage Summary

**Total Use Cases:** 3

### Coverage Details

| Metric | Count | Description |
|---|---:|---|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 3 | User stories containing a mix of fully covered and partially covered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

### Coverage Gap Details

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| LZ-001 | AC4 | AC4: Connectivity Check: Given network segmentation, when resources in Dev attempt to access Prod, then the connection must be blocked by default. | NULL | Partially Covered |
| BRZ-001 | AC1 | AC1: Connectivity Verification: Given an ADF pipeline, when connecting to an on-prem SQL database, then it must use a Self-Hosted Integration Runtime. | NULL | Partially Covered |
| BRZ-001 | AC4 | AC4: Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | NULL | Partially Covered |
| STG-001 | AC2 | AC2: Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | NULL | Partially Covered |
| STG-001 | AC5 | AC5: Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access. | NULL | Partially Covered |

### Coverage Score

| User Story ID | Coverage Score | Color |
|---|---:|---|
| LZ-001 | 90.00% | 🟢 Green |
| BRZ-001 | 80.00% | 🟠 Amber |
| STG-001 | 80.00% | 🟠 Amber |

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

- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## 3. Test Execution Summary

**Total Test Cases Executed:** 45

**Total Test Cases Not Executed:** 0

**Total Test Cases Passed:** 39

**Total Test Cases Failed:** 6

**Execution Success Rate:** 86.70%

### Test Execution Summary Details

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---|---:|---:|---:|---:|---:|---:|---:|
| LZ-001 | 15 | 15 | 0 | NULL | NULL | 100.00% | NULL |
| BRZ-001 | 15 | 15 | 0 | NULL | NULL | 100.00% | NULL |
| STG-001 | 15 | 15 | 0 | NULL | NULL | 100.00% | NULL |

## 4. Defect Details

**Defect Rate:** 13.33%

### Defect Rate Analysis

**Formula:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

### Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|---|---|---|---|---|---|---|---|
| NULL | UT_LZ-001_008 | LZ-001 | NULL | NULL | NULL | NULL | Failed |
| NULL | UT_BRZ-001_002 | BRZ-001 | NULL | NULL | NULL | NULL | Failed |
| NULL | UT_BRZ-001_009 | BRZ-001 | NULL | NULL | NULL | NULL | Failed |
| NULL | UT_STG-001_004 | STG-001 | NULL | NULL | NULL | NULL | Failed |
| NULL | UT_STG-001_011 | STG-001 | NULL | NULL | NULL | NULL | Failed |
| NULL | NULL | NULL | NULL | NULL | NULL | NULL | NULL |

## 5. Conclusion

A total of 3 user stories were reviewed. Coverage distribution is 0 fully covered, 3 partially covered, and 0 not covered user stories. The overall Test Coverage Rate is 83.30%, the Execution Success Rate is 86.70%, and the Defect Rate is 13.33%.

Based on the reported overall Test Coverage Rate of 83.30% and Execution Success Rate of 86.70%, the unit test suite shows partial coverage across all reviewed user stories. Defect severity rate is NULL.

The current unit test suite is not fully evidenced for progression because all reviewed user stories remain partially covered and failed test cases are present. Remediation is required before progression.
