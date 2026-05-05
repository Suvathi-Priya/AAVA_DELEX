# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 5 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

The baseline for evaluation consists of 5 user stories containing 25 acceptance criteria and 75 unit test cases. The scope is limited to unit test coverage and execution records mapped to these user stories.

## 2. Test Coverage Summary

**Total Use Cases:** 5

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 4 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 1 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

**Coverage Gap Details:**

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---------------|-------|-------------------|--------------|------------------|
| SEC-002 | AC2 | PII Data Masking: Given columns identified as PII (e.g., SSN, Email), when queried by non-authorized users, then the data must be masked (e.g., XXX-XX-1234). | High | Partially Covered |
| SEC-002 | AC3 | Row-Level Security (RLS): Given a global sales report, when a regional manager logs in, then they must only see data associated with their specific region. | High | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| SEC-001 | 100.00% | 🟢 Green |
| GOV-001 | 100.00% | 🟢 Green |
| MON-001 | 100.00% | 🟢 Green |
| SEC-002 | 60.00% | 🔴 Red |
| BKP-001 | 100.00% | 🟢 Green |

**Legend:**

🟢 Green (90–100%) → High coverage (meets quality expectations)

🟡 Amber (70–89%) → Moderate coverage (requires attention)

🔴 Red (<70%) → Low coverage (critical gaps present)

**Coverage Score Analysis:**

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

Components:
- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## 3. Test Execution Summary

**Total Test Cases Executed:** 15

**Total Test Cases Not Executed:** 60

**Total Test Cases Passed:** 13

**Total Test Cases Failed:** 2

**Execution Success Rate:** 86.67%

**Test Execution Summary Details:**

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---------------|------------------|----------|--------------|--------|--------|----------------|------------|
| SEC-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| GOV-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| MON-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| SEC-002 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| BKP-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |

## 4. Defect Details

**Defect Rate:** 13.33%

**Defect Rate Analysis:**

Defect Rate = (Total Defects / Total Test Cases) × 100

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|-----------|--------------|---------------|--------------|-------------------|----------|----------|--------|
| DEF_SEC-002_002 | UT_SEC-002_002 | SEC-002 | PII Masking Failure | PII Masking Failure. Functionality Check: SSN column masking. Actual Behavior: SSN was visible in plain text for users in 'Marketing_Analyst' group. | data_masking | high | open |
| DEF_SEC-002_003 | UT_SEC-002_003 | SEC-002 | RLS Logic Error | RLS Logic Error. Functionality Check: Regional Sales filtering. Actual Behavior: Regional managers could see global data due to missing filter predicate in the view. | row_level_security | high | open |

## 5. Conclusion

**Summary of Findings**

The analysis indicates 5 user stories were reviewed with 92.00% overall coverage rate. Coverage distribution shows 4 user stories fully covered and 1 user story partially covered. The execution success rate is 86.67% with a defect rate of 13.33%.

**Final Outcome Statement**

Results show that the overall average coverage score of 92.00%, overall execution stability of 86.67%, and defect severity rate of 100.00% indicate critical gaps in security-related functionality. Key gaps identified include PII data masking failures and row-level security implementation defects.

**Conclusion Statement**

The current coverage and quality are insufficient to proceed due to high-severity defects in security controls. Remediation is required before progression to address data masking and row-level security failures.