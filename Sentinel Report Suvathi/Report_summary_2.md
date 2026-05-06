# UNIT TEST QUALITY & COVERAGE REPORT

## 1. Scope

This report evaluates unit test coverage and quality across 8 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

The evaluation encompasses unit test cases linked to the identified user stories, test execution results (executed, not executed, passed, failed), and defect data directly associated with these user stories. Integration tests, system tests, performance tests, user stories not mapped to test cases, and external or unrelated defect logs are excluded from this analysis.

## 2. Test Coverage Summary

**Total Use Cases:** 8

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 1 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 7 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

**Coverage Gap Details:**

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---------------|-------|-------------------|--------------|-----------------||
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the 'Cost Center' tag is missing, then the deployment must fail validation. | high | Partially Covered |
| STG-001 | AC5 | Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access. | high | Partially Covered |
| BRZ-002 | AC4 | Latency SLA: Given the streaming ingestion, when a message enters Event Hub, then it must be visible in the Bronze layer within 5 minutes. | high | Partially Covered |
| SEC-001 | AC4 | Key Vault Integration: Given secret retrieval, when ADF needs a third-party API key, then it must use its identity to fetch the secret from Azure Key Vault. | high | Partially Covered |
| SLV-001 | AC1 | Standardized Date Formats: Given raw source data, when processed into the Silver layer, then all date columns must be converted to ISO 8601 format (YYYY-MM-DD). | medium | Partially Covered |
| SLV-001 | AC5 | Schema Enforcement: Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | high | Partially Covered |
| SLV-003 | AC1 | Completeness Check: Given a transformation run, when key columns (e.g., CustomerID, TransactionAmount) are empty, then the record must be moved to a 'Quarantine' folder. | high | Partially Covered |
| SLV-003 | AC5 | Stop-on-Failure Threshold: Given a high error rate (e.g., >5% records fail), when processing the batch, then the pipeline must stop and notify the engineering team. | medium | Partially Covered |
| GLD-001 | AC4 | Performance Partitioning: Given large datasets in Gold, when stored in Synapse/Fabric, then tables must be partitioned by 'Business Period' (e.g., Fiscal Year) for query optimization. | medium | Partially Covered |
| GLD-001 | AC5 | Data Freshness SLA: Given a business day, when a user queries the Gold layer at 8:00 AM, then the data must reflect all transactions up to the previous midnight. | high | Partially Covered |

**Coverage Score by User Story:**

| User Story ID | Coverage Score | Color | Icon |
|---------------|----------------|-------|------|
| LZ-001 | 80.00% | Amber | 🟠 |
| BRZ-001 | 100.00% | Green | 🟢 |
| STG-001 | 80.00% | Amber | 🟠 |
| BRZ-002 | 80.00% | Amber | 🟠 |
| SEC-001 | 80.00% | Amber | 🟠 |
| SLV-001 | 60.00% | Red | 🔴 |
| SLV-003 | 60.00% | Red | 🔴 |
| GLD-001 | 60.00% | Red | 🔴 |

**Legend:**

🟢 Green (90–100%) → High coverage (meets quality expectations)

🟠 Amber (70–89%) → Moderate coverage (requires attention)

🔴 Red (<70%) → Low coverage (critical gaps present)

**Coverage Score Analysis:**

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

**Description:**

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

**Components:**

- **Covered Acceptance Criteria:** Number of acceptance criteria that have at least one mapped test case
- **Total Acceptance Criteria:** Total number of acceptance criteria defined across user stories

## 3. Test Execution Summary

**Total Test Cases Executed:** 120

**Total Test Cases Not Executed:** 0

**Total Test Cases Passed:** 110

**Total Test Cases Failed:** 10

**Execution Success Rate:** 91.67%

**Test Execution Summary Details:**

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---------------|------------------|----------|--------------|--------|--------|----------------|-----------||
| LZ-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| BRZ-001 | 15 | 15 | 0 | 15 | 0 | 100.00% | 100.00% |
| STG-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| BRZ-002 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| SEC-001 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| SLV-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SLV-003 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| GLD-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

## 4. Defect Details

**Defect Rate:** 8.33%

**Defect Rate Analysis:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Description:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

- **Total Defects:** Total number of defects identified during the test cycle
- **Total Test Cases:** Total number of test cases executed

**Defect Details:**

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|-----------|--------------|---------------|--------------|-------------------|----------|----------|--------||
| DEF_LZ-001_005 | UT_LZ-001_005 | LZ-001 | Tagging Policy Bypass | Functionality Check: Mandatory 'Cost Center' tag. Actual Behavior: Resource was successfully deployed via Terraform without the tag, indicating Policy was not in Enforce mode, violating AC5. | policy_enforcement | high | open |
| DEF_STG-001_009 | UT_STG-001_009 | STG-001 | RBAC Isolation Leak | Functionality Check: Denial of /gold container access. Actual Behavior: User with 'Bronze Reader' was able to view 'Gold' file metadata due to incorrect ACL inheritance, violating AC5. | access_control | high | open |
| DEF_BRZ-002_012 | UT_BRZ-002_012 | BRZ-002 | Ingestion Latency Breach | Functionality Check: 5-minute visibility SLA. Actual Behavior: Streaming data took 7 minutes to appear in ADLS due to Event Hub capture lag, violating AC4. | performance | high | open |
| DEF_SEC-001_004 | UT_SEC-001_004 | SEC-001 | Key Vault Access Failure | Functionality Check: Secret retrieval using Managed Identity. Actual Behavior: ADF received 'Access Denied' because the Identity was not added to the Key Vault Access Policy, violating AC4. | authentication | high | open |
| DEF_SLV-001_001 | UT_SLV-001_001 | SLV-001 | Date Standardization Error | Functionality Check: ISO 8601 conversion. Actual Behavior: Dates remained in MM/DD/YYYY format in the Delta table. | data_transformation | medium | open |
| DEF_SLV-001_014 | UT_SLV-001_014 | SLV-001 | Schema Enforcement Failure | Functionality Check: Block write on schema mismatch. Actual Behavior: Data with additional columns was successfully appended, breaking downstream dependencies. | schema_validation | high | open |
| DEF_SLV-003_001 | UT_SLV-003_001 | SLV-003 | Completeness Check Bypass | Functionality Check: CustomerID null check. Actual Behavior: Records with NULL CustomerID were loaded to Silver instead of being quarantined. | data_quality | high | open |
| DEF_SLV-003_015 | UT_SLV-003_015 | SLV-003 | Stop-on-Failure Threshold | Functionality Check: 5% error threshold. Actual Behavior: Pipeline continued processing despite a 12% error rate in the current batch. | error_handling | medium | open |
| DEF_GLD-001_005 | UT_GLD-001_005 | GLD-001 | Freshness SLA Breach | Functionality Check: Midnight transaction availability by 8 AM. Actual Behavior: Data only reflected transactions up to 6 PM previous day due to batch lag. | data_freshness | high | open |
| DEF_GLD-001_014 | UT_GLD-001_014 | GLD-001 | Partitioning Logic Failure | Functionality Check: Fiscal Year partitioning. Actual Behavior: All data was written to the default partition, degrading query performance. | performance | medium | open |

## 5. Conclusion

**Summary of Findings**

The analysis reviewed 8 user stories with 40 total acceptance criteria. Coverage distribution shows 1 fully covered, 7 partially covered, and 0 not covered user stories. The execution success rate achieved 91.67% with a defect rate of 8.33%.

**Final Outcome Statement**

The overall coverage rate of 75.00%, execution stability of 91.67%, and defect severity rate of 70.00% indicate moderate quality levels with significant remediation requirements before progression.

**Conclusion Statement**

The current unit test suite demonstrates moderate coverage and execution stability but requires immediate attention to address critical coverage gaps and high-severity defects before proceeding to the next phase.

---

**Report Generated:** Unit Test Quality & Coverage Report

**Document Format:** Markdown (.md)

**Export Location:** GitHub Repository