# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 2 user stories. The scope is restricted to test plans and execution records mapped to these user stories. The analysis encompasses 5 acceptance criteria, 8 unit test cases, and associated defect data directly linked to the identified user stories.

**Scope Definition:**

The baseline for this evaluation comprises 2 user stories containing 5 acceptance criteria. The analysis is limited to unit test coverage and execution records mapped to these user stories. This report measures test case coverage against acceptance criteria, execution results, and defect identification within the defined scope.

**Inclusions:**

- Unit test cases linked to the 2 identified user stories
- Test execution results (executed, not executed, passed, failed)
- Defect data directly associated with these user stories

**Exclusions:**

- Integration tests, system tests, or performance tests
- User stories not mapped to test cases
- External or unrelated defect logs

## 2. Test Coverage Summary

**Total Use Cases:** 2

**Coverage Details:**

| Metric            | Count | Description                                                                 |
|-------------------|-------|-----------------------------------------------------------------------------|
| Fully Covered     | 1     | User stories where all acceptance criteria are covered by test cases        |
| Partially Covered | 1     | User stories containing a mix of covered and uncovered acceptance criteria  |
| Not Covered       | 0     | User stories where none of the acceptance criteria are covered by test cases|

**Coverage Gap Details:**

**User Story: US-001 - User Authentication**

| User Story ID | AC ID     | Acceptance Criteria                               | Impact Level | Coverage Status    |
|---------------|-----------|---------------------------------------------------|--------------|-------------------|
| US-001        | AC-001-2  | System displays error for invalid credentials     | medium       | Partially Covered |

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| US-001        | 100.00%        | Green |

**User Story: US-002 - Password Reset**

| User Story ID | AC ID     | Acceptance Criteria                    | Impact Level | Coverage Status    |
|---------------|-----------|----------------------------------------|--------------|-------------------|
| US-002        | AC-002-2  | Reset link expires after 24 hours      | low          | Partially Covered |

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| US-002        | 100.00%        | Green |

**Legend:**

Green (90–100%) → High coverage (meets quality expectations)

Amber (70–89%) → Moderate coverage (requires attention)

Red (<70%) → Low coverage (critical gaps present)

**Coverage Score Analysis:**

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

**Description:**

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

**Components:**

- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## 3. Test Execution Summary

**Total Test Cases Executed:** 7

**Total Test Cases Not Executed:** 1

**Total Test Cases Passed:** 6

**Total Test Cases Failed:** 1

**Execution Success Rate:** 85.70%

**Test Execution Summary Details:**

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---------------|------------------|----------|--------------|--------|--------|----------------|-----------||
| US-001        | 5                | 5        | 0            | 4      | 1      | 100.00%        | 80.00%    |
| US-002        | 3                | 2        | 1            | 2      | 0      | 66.70%         | 100.00%   |

## 4. Defect Details

**Defect Rate:** 12.50%

**Defect Rate Analysis:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Title                           | Defect Description                                                                                                                                                                                                              | Category | Severity | Status |
|-----------|--------------|---------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|----------|--------|
| DEF-001   | TC-003       | US-001        | SQL Injection Validation Failure       | Error message not displayed for SQL injection attempt in login field. Functionality Check: Invalid credential error handling. Actual Behavior: System accepted SQL injection string without proper validation or error message | security | critical | open   |

## 5. Conclusion

**Summary of Findings:**

The analysis evaluated 2 user stories comprising 5 acceptance criteria and 8 test cases. Results show 1 user story fully covered and 1 user story partially covered. The overall test coverage rate stands at 100.00%, indicating all acceptance criteria have mapped test cases. Test execution reflects 87.50% execution rate with 85.70% execution success rate. The defect rate measures 12.50% with 1 critical defect identified.

**Final Outcome Statement:**

The overall average coverage score of 100.00% demonstrates complete acceptance criteria mapping. The overall execution stability of 85.70% reflects execution gaps requiring attention. The defect severity rate of 100.00% indicates all identified defects are classified as critical severity, with 1 critical security defect affecting input validation mechanisms.

**Conclusion Statement:**

The unit test suite demonstrates complete coverage across defined acceptance criteria but requires immediate remediation due to the presence of 1 critical security defect and execution gaps before progression to subsequent testing phases.