# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 2 user stories.

The 2 user stories form the baseline for evaluation. The scope is restricted to unit test coverage, unit test execution records, and defect data mapped to these user stories.

Included in scope:
- Unit test cases linked to the identified user stories.
- Test execution results covering executed, not executed, passed, and failed statuses.
- Defect data directly associated with these user stories.

Excluded from scope:
- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

The user stories are the baseline reference for measuring test coverage, execution success, and defect quality.

## Test Coverage Summary

Total Use Cases: 2

Coverage Details:

| Metric | Count | Description |
|--------------------|-------|-----------------------------------------------------------------------------|
| Fully Covered | 1 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 1 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|----------------|-------|---------------------|--------------|-----------------|
| US-202 | AC3 | System should calculate total order amount correctly. | NULL | Partially Covered |

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| US-202 | 91.70% | 🟢 Green |

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

Total Test Cases Executed: 30

Total Test Cases Passed: 20

Total Test Cases Failed: 10

Execution Success Rate: 66.67%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Total Executed | Passed | Failed |
|---------------|------------------|----------------|--------|--------|
| US-101 | 15 | 15 | 10 | 5 |
| US-202 | 15 | 15 | 10 | 5 |

Data Mapping Inconsistency Details:

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---------------|------------------|-------------|----------------|-------|---------------|
| TC115 | mapping_mismatch | Testcase 'Verify UI color theme consistency' is incorrectly mapped to functional criteria 'API should reject profile creation if mandatory fields are missing.' | US-101 | AC2 | Low |
| TC113 | mapping_mismatch | Testcase 'Verify API response time under load' (Performance) is incorrectly mapped to functional criteria 'API should allow updating existing customer profiles.' | US-101 | AC3 | Medium |
| TC114 | mapping_mismatch | Testcase 'Verify database backup after profile update' (Recovery) is incorrectly mapped to functional criteria 'API should allow retrieval of customer profile using customer ID.' | US-101 | AC5 | Medium |
| TC213 | mapping_mismatch | Testcase 'Verify application dark mode compatibility' (UI) is incorrectly mapped to functional criteria 'System should update inventory after successful order placement.' | US-202 | AC4 | Low |
| TC215 | mapping_mismatch | Testcase 'Verify printer connectivity for invoices' (Hardware) is incorrectly mapped to functional criteria 'System should send order confirmation notifications.' | US-202 | AC5 | Low |
| TC214 | mapping_mismatch | Testcase 'Verify third-party analytics integration' (Integration) is incorrectly mapped to functional criteria 'System should maintain order processing logs.' | US-202 | AC6 | Medium |

Consistency Metrics Summary:

| Metric | Count |
|---------|-------|
| Total Test Cases | 30 |
| Total Test Logs | 30 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Extra Test Cases | 0 |
| Extra Test Logs | 0 |
| Consistency Status | Mismatch Detected |

## Defect Details

Defect Rate: 33.33%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:
- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Severity | Status |
|-----------|--------------|---------------|--------------|--------------------|----------|--------|
| DEF-101 | TC101 | US-101 | NULL | API fails to create a customer profile even with all mandatory fields provided. | High | open |
| DEF-104 | TC104 | US-101 | NULL | API fails to reject profile creation when the mandatory email field is missing. | High | open |
| DEF-107 | TC107 | US-101 | NULL | API does not validate email formats correctly, accepting emails without an '@' symbol. | High | open |
| DEF-110 | TC110 | US-101 | NULL | API returns an unexpected response or error when retrieving a profile with an invalid customer ID. | Medium | open |
| DEF-113 | TC113 | US-101 | NULL | API response time for profile updates exceeds the defined SLA under load. | Medium | open |
| DEF-201 | TC201 | US-202 | NULL | System fails to create an order for valid products, blocking the core purchase workflow. | Critical | open |
| DEF-204 | TC204 | US-202 | NULL | System does not reject an order when the product list is empty. | High | open |
| DEF-207 | TC207 | US-202 | NULL | Inventory is not updated after a successful order placement. | Critical | open |
| DEF-210 | TC210 | US-202 | NULL | System fails to send SMS confirmation notifications after an order is created. | Medium | open |
| DEF-213 | TC213 | US-202 | NULL | Application dark mode has rendering issues on the inventory update page. | Low | open |

## Conclusion

Summary of Findings:

A total of 2 user stories were reviewed. Coverage distribution shows 1 fully covered user story, 1 partially covered user story, and 0 not covered user stories. The overall test coverage rate is 95.80%, the execution success rate is 66.70%, and the defect rate is 33.33%.

Final Outcome Statement:

Based on the overall test coverage rate of 95.80%, overall execution success rate of 66.70%, and the presence of Critical, High, Medium, and Low severity defects, the current unit test results indicate that coverage is high, but execution stability and defect severity remain unresolved.

Conclusion Statement:

The current unit test suite is not sufficient to proceed without remediation. Defect resolution and correction of identified coverage and mapping gaps are required before progression.