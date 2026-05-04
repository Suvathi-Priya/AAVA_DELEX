# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 10 user stories. These user stories form the baseline for evaluation and are limited to unit test coverage and execution records mapped to these user stories.

The scope includes unit test cases linked to the identified user stories, test execution results (executed, not executed, passed, failed), and defect data directly associated with these user stories.

The analysis excludes integration tests, system tests, performance tests, user stories not mapped to test cases, and any external or unrelated defect logs.

## 2. Test Coverage Summary

**Total User Stories:** 10

### Coverage Details:

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 1 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 9 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

### Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---------------|-------|-------------------|--------------|------------------|
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the 'Cost Center' tag is missing, then the deployment must fail validation. | High | Partially Covered |
| STG-001 | AC5 | Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access. | High | Partially Covered |
| BRZ-002 | AC4 | Latency SLA: Given the streaming ingestion, when a message enters Event Hub, then it must be visible in the Bronze layer within 5 minutes. | High | Partially Covered |
| SEC-001 | AC4 | Key Vault Integration: Given secret retrieval, when ADF needs a third-party API key, then it must use its identity to fetch the secret from Azure Key Vault. | High | Partially Covered |
| SLV-001 | AC1 | Standardized Date Formats: Given raw source data, when processed into the Silver layer, then all date columns must be converted to ISO 8601 format (YYYY-MM-DD). | Medium | Partially Covered |
| SLV-001 | AC5 | Schema Enforcement: Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | High | Partially Covered |
| SLV-002 | AC1 | Merge Operation Efficiency: Given incremental data in Bronze, when loading to Silver, then the system must perform a UPSERT (Merge) based on the unique Business Key. | High | Partially Covered |
| SLV-002 | AC5 | Watermark Management: Given a batch run, when successful, then the high-watermark timestamp must be updated to ensure the next run only picks up new data. | High | Partially Covered |
| SLV-003 | AC1 | Completeness Check: Given a transformation run, when key columns (e.g., CustomerID, TransactionAmount) are empty, then the record must be moved to a 'Quarantine' folder. | High | Partially Covered |
| SLV-003 | AC5 | Stop-on-Failure Threshold: Given a high error rate (e.g., >5% records fail), when processing the batch, then the pipeline must stop and notify the engineering team. | High | Partially Covered |
| GLD-001 | AC4 | Performance Partitioning: Given large datasets in Gold, when stored in Synapse/Fabric, then tables must be partitioned by 'Business Period' (e.g., Fiscal Year) for query optimization. | Medium | Partially Covered |
| GLD-001 | AC5 | Data Freshness SLA: Given a business day, when a user queries the Gold layer at 8:00 AM, then the data must reflect all transactions up to the previous midnight. | High | Partially Covered |
| SEC-002 | AC2 | PII Data Masking: Given columns identified as PII (e.g., SSN, Email), when queried by non-authorized users, then the data must be masked (e.g., XXX-XX-1234). | High | Partially Covered |
| SEC-002 | AC3 | Row-Level Security (RLS): Given a global sales report, when a regional manager logs in, then they must only see data associated with their specific region. | High | Partially Covered |

### Coverage Score by User Story:

| User Story ID | Coverage Score | Color |
|---------------|----------------|-------|
| LZ-001 | 80.00% | 🟠 Amber |
| BRZ-001 | 100.00% | 🟢 Green |
| STG-001 | 80.00% | 🟠 Amber |
| BRZ-002 | 80.00% | 🟠 Amber |
| SEC-001 | 80.00% | 🟠 Amber |
| SLV-001 | 60.00% | 🔴 Red |
| SLV-002 | 60.00% | 🔴 Red |
| SLV-003 | 60.00% | 🔴 Red |
| GLD-001 | 60.00% | 🔴 Red |
| SEC-002 | 60.00% | 🔴 Red |

### Legend:

- 🟢 **Green (90–100%)** → High coverage (meets quality expectations)
- 🟠 **Amber (70–89%)** → Moderate coverage (requires attention)
- 🔴 **Red (<70%)** → Low coverage (critical gaps present)

### Coverage Score Analysis:

**Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100**

**Description:**

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

**Components:**

- **Covered Acceptance Criteria:** Number of acceptance criteria that have at least one mapped test case
- **Total Acceptance Criteria:** Total number of acceptance criteria defined across user stories

## 3. Test Execution Summary

**Total Test Cases Executed:** 150

**Total Test Cases Not Executed:** 0

**Total Test Cases Passed:** 137

**Total Test Cases Failed:** 13

**Execution Success Rate:** 91.33%

### Test Execution Summary Details:

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---------------|------------------|----------|--------------|--------|--------|----------------|------------|
| LZ-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| BRZ-001 | 15 | 15 | 0 | 15 | 0 | 100.00% | 100.00% |
| STG-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| BRZ-002 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| SEC-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| SLV-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SLV-002 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SLV-003 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| GLD-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SEC-002 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

### Test Execution Analysis:

Execution success rate indicates stable coverage across most user stories with 100% execution rate achieved across all test cases. Failures are concentrated in data transformation, schema validation, and security enforcement areas. The Silver layer user stories (SLV-001, SLV-002, SLV-003) and Gold layer aggregations (GLD-001) show consistent failure patterns in boundary condition validations and data quality enforcement.

## 4. Defect Details

**Defect Rate:** 8.67%

### Defect Rate Analysis:

**Defect Rate = (Total Defects / Total Test Cases) × 100**

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

- **Total Defects:** Total number of defects identified during the test cycle
- **Total Test Cases:** Total number of test cases executed

### Defect Details:

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|-----------|--------------|---------------|--------------|-------------------|----------|----------|--------|
| DEF_LZ-001_005 | UT_LZ-001_005 | LZ-001 | Tagging Policy Bypass | Resource was successfully deployed via Terraform without the tag, indicating Policy was not in Enforce mode, violating AC5. | policy_enforcement | High | Open |
| DEF_STG-001_009 | UT_STG-001_009 | STG-001 | RBAC Isolation Leak | User with 'Bronze Reader' was able to view 'Gold' file metadata due to incorrect ACL inheritance, violating AC5. | access_control | High | Open |
| DEF_BRZ-002_012 | UT_BRZ-002_012 | BRZ-002 | Ingestion Latency Breach | Streaming data took 7 minutes to appear in ADLS due to Event Hub capture lag, violating AC4. | performance_sla | High | Open |
| DEF_SEC-001_004 | UT_SEC-001_004 | SEC-001 | Key Vault Access Failure | ADF received 'Access Denied' because the Identity was not added to the Key Vault Access Policy, violating AC4. | identity_management | High | Open |
| DEF_SLV-001_001 | UT_SLV-001_001 | SLV-001 | Date Standardization Error | Dates remained in MM/DD/YYYY format in the Delta table. | data_transformation | Medium | Open |
| DEF_SLV-001_014 | UT_SLV-001_014 | SLV-001 | Schema Enforcement Failure | Data with additional columns was successfully appended, breaking downstream dependencies. | schema_validation | High | Open |
| DEF_SLV-002_002 | UT_SLV-002_002 | SLV-002 | MERGE Logic Error | MERGE operation created duplicate records in Silver for existing Business Keys. | data_quality | High | Open |
| DEF_SLV-002_012 | UT_SLV-002_012 | SLV-002 | Watermark Update Failure | Watermark was not updated post-success, causing the next run to re-process old data. | metadata_management | High | Open |
| DEF_SLV-003_001 | UT_SLV-003_001 | SLV-003 | Completeness Check Bypass | Records with NULL CustomerID were loaded to Silver instead of being quarantined. | data_quality | High | Open |
| DEF_SLV-003_015 | UT_SLV-003_015 | SLV-003 | Stop-on-Failure Threshold | Pipeline continued processing despite a 12% error rate in the current batch. | error_handling | High | Open |
| DEF_GLD-001_005 | UT_GLD-001_005 | GLD-001 | Freshness SLA Breach | Data only reflected transactions up to 6 PM previous day due to batch lag. | data_freshness | High | Open |
| DEF_GLD-001_014 | UT_GLD-001_014 | GLD-001 | Partitioning Logic Failure | All data was written to the default partition, degrading query performance. | performance_optimization | Medium | Open |
| DEF_SEC-002_002 | UT_SEC-002_002 | SEC-002 | PII Masking Failure | SSN was visible in plain text for users in 'Marketing_Analyst' group. | data_security | Critical | Open |
| DEF_SEC-002_003 | UT_SEC-002_003 | SEC-002 | RLS Logic Error | Regional managers could see global data due to missing filter predicate in the view. | access_control | Critical | Open |

## 5. Conclusion

### Summary of Findings

This analysis reviewed 10 user stories with 50 total acceptance criteria. Coverage distribution shows 1 fully covered, 9 partially covered, and 0 not covered user stories. The execution success rate is 91.33% with a defect rate of 8.67%. Key gaps are observed in data transformation, security enforcement, and performance optimization areas.

### Final Outcome Statement

The overall average coverage score is 72.00%, overall execution stability is 91.33%, and defect severity rate shows Critical: 14.3%, High: 71.4%, Medium: 14.3%, Low: 0.0%. Based on the amber coverage score and high-severity defect concentration, remediation is required before progression.

### Conclusion Statement

The current unit test suite requires immediate attention to address critical security defects and high-severity data quality issues before proceeding to production deployment. Coverage gaps in 9 out of 10 user stories indicate insufficient validation of acceptance criteria.