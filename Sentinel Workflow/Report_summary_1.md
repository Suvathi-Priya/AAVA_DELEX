# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 9 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Coverage Boundary:** The total number of user stories included in the analysis is 9, forming the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

**Inclusions:** Unit test cases linked to the identified user stories, test execution results (executed, not executed, passed, failed), and defect data directly associated with these user stories.

**Exclusions:** Integration tests, system tests, or performance tests, user stories not mapped to test cases, and any external or unrelated defect logs.

## 2. Test Coverage Summary

**Total Use Cases:** 9

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 1 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 8 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

**Coverage Gap Details:**

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---------------|-------|-------------------|--------------|------------------|
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the 'Cost Center' tag is missing, then the deployment must fail validation. | High | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | High | Partially Covered |
| BRZ-002 | AC4 | Latency SLA: Given the streaming ingestion, when a message enters Event Hub, then it must be visible in the Bronze layer within 5 minutes. | High | Partially Covered |
| STG-001 | AC5 | Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access. | Critical | Partially Covered |
| SLV-001 | AC1 | Standardized Date Formats: Given raw source data, when processed into the Silver layer, then all date columns must be converted to ISO 8601 format (YYYY-MM-DD). | Medium | Partially Covered |
| SLV-001 | AC5 | Schema Enforcement: Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | High | Partially Covered |
| SLV-002 | AC1 | Merge Operation Efficiency: Given incremental data in Bronze, when loading to Silver, then the system must perform a UPSERT (Merge) based on the unique Business Key. | Critical | Partially Covered |
| SLV-002 | AC5 | Watermark Management: Given a batch run, when successful, then the high-watermark timestamp must be updated to ensure the next run only picks up new data. | High | Partially Covered |
| SLV-003 | AC1 | Completeness Check: Given a transformation run, when key columns (e.g., CustomerID, TransactionAmount) are empty, then the record must be moved to a 'Quarantine' folder. | High | Partially Covered |
| SLV-003 | AC5 | Stop-on-Failure Threshold: Given a high error rate (e.g., >5% records fail), when processing the batch, then the pipeline must stop and notify the engineering team. | Medium | Partially Covered |
| GLD-001 | AC4 | Performance Partitioning: Given large datasets in Gold, when stored in Synapse/Fabric, then tables must be partitioned by 'Business Period' (e.g., Fiscal Year) for query optimization. | Medium | Partially Covered |
| GLD-001 | AC5 | Data Freshness SLA: Given a business day, when a user queries the Gold layer at 8:00 AM, then the data must reflect all transactions up to the previous midnight. | High | Partially Covered |

**Coverage Score:**

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| LZ-001 | 80.00% | 🟡 Amber |
| SEC-001 | 100.00% | 🟢 Green |
| BRZ-001 | 80.00% | 🟡 Amber |
| BRZ-002 | 80.00% | 🟡 Amber |
| STG-001 | 80.00% | 🟡 Amber |
| SLV-001 | 60.00% | 🔴 Red |
| SLV-002 | 60.00% | 🔴 Red |
| SLV-003 | 60.00% | 🔴 Red |
| GLD-001 | 60.00% | 🔴 Red |

**Legend:**

- 🟢 Green (90–100%) → High coverage (meets quality expectations)
- 🟡 Amber (70–89%) → Moderate coverage (requires attention)
- 🔴 Red (<70%) → Low coverage (critical gaps present)

**Coverage Score Analysis:**

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

**Description:**

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

**Components:**

- **Covered Acceptance Criteria:** Number of acceptance criteria that have at least one mapped test case
- **Total Acceptance Criteria:** Total number of acceptance criteria defined across user stories

## 3. Test Execution Summary

**Total Test Cases Executed:** 120

**Total Test Cases Not Executed:** 15

**Total Test Cases Passed:** 108

**Total Test Cases Failed:** 12

**Execution Success Rate:** 90.00%

**Test Execution Summary Details:**

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---------------|------------------|----------|--------------|--------|--------|----------------|------------|
| LZ-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| SEC-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| BRZ-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| BRZ-002 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| STG-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| SLV-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SLV-002 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SLV-003 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| GLD-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

## 4. Defect Details

**Defect Rate:** 8.89%

**Defect Rate Analysis:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

- **Total Defects:** Total number of defects identified during the test cycle
- **Total Test Cases:** Total number of test cases executed

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|-----------|--------------|---------------|--------------|-------------------|----------|----------|--------|
| DEF_LZ-001_005 | UT_LZ-001_005 | LZ-001 | Tagging Policy Bypass | Resource was successfully deployed via Terraform without the tag, indicating Policy was not in Enforce mode, violating AC5. | Policy Enforcement | High | Open |
| DEF_BRZ-001_013 | UT_BRZ-001_013 | BRZ-001 | Retry Logic Failure | Pipeline failed immediately upon first network timeout without triggering retry attempts, violating AC4. | Retry Logic | High | Open |
| DEF_BRZ-002_012 | UT_BRZ-002_012 | BRZ-002 | Ingestion Latency Breach | Streaming data took 7 minutes to appear in ADLS due to Event Hub capture lag, violating AC4. | Performance SLA | High | Open |
| DEF_STG-001_009 | UT_STG-001_009 | STG-001 | RBAC Isolation Leak | User with 'Bronze Reader' was able to view 'Gold' file metadata due to incorrect ACL inheritance, violating AC5. | Access Control | Critical | Open |
| DEF_SLV-001_001 | UT_SLV-001_001 | SLV-001 | Date Standardization Error | Dates remained in MM/DD/YYYY format in the Delta table. | Data Transformation | Medium | Open |
| DEF_SLV-001_014 | UT_SLV-001_014 | SLV-001 | Schema Enforcement Failure | Data with additional columns was successfully appended, breaking downstream dependencies. | Schema Validation | High | Open |
| DEF_SLV-002_002 | UT_SLV-002_002 | SLV-002 | MERGE Logic Error | MERGE operation created duplicate records in Silver for existing Business Keys. | Data Quality | Critical | Open |
| DEF_SLV-002_012 | UT_SLV-002_012 | SLV-002 | Watermark Update Failure | Watermark was not updated post-success, causing the next run to re-process old data. | Watermark Management | High | Open |
| DEF_SLV-003_001 | UT_SLV-003_001 | SLV-003 | Completeness Check Bypass | Records with NULL CustomerID were loaded to Silver instead of being quarantined. | Data Quality | High | Open |
| DEF_SLV-003_015 | UT_SLV-003_015 | SLV-003 | Stop-on-Failure Threshold | Pipeline continued processing despite a 12% error rate in the current batch. | Error Handling | Medium | Open |
| DEF_GLD-001_005 | UT_GLD-001_005 | GLD-001 | Freshness SLA Breach | Data only reflected transactions up to 6 PM previous day due to batch lag. | Data Freshness | High | Open |
| DEF_GLD-001_014 | UT_GLD-001_014 | GLD-001 | Partitioning Logic Failure | All data was written to the default partition, degrading query performance. | Performance Optimization | Medium | Open |

## 5. Conclusion

**Summary of Findings**

The analysis indicates 9 user stories were reviewed with an overall coverage rate of 73.33%. The execution success rate reflects 90.00% stability across 120 executed test cases. Results show that 12 defects were identified with a defect severity rate of 75.00% representing high and critical issues.

**Final Outcome Statement**

The overall average coverage score of 73.33%, execution stability of 90.00%, and defect severity rate of 75.00% indicate significant gaps requiring remediation. Key gaps identified include critical access control violations, data quality issues, and policy enforcement failures.

**Conclusion Statement**

The current coverage and quality metrics indicate the unit test suite requires substantial remediation before progression. Critical defects in access control and data quality must be resolved to ensure system reliability and security compliance.