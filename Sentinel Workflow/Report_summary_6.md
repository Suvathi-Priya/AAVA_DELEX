# UNIT TEST QUALITY & COVERAGE REPORT

---

## 1. Scope

This report evaluates unit test coverage and quality across 9 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

### Coverage Boundary

The analysis encompasses 9 user stories containing 45 acceptance criteria, forming the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

### Inclusions

- Unit test cases linked to the identified user stories
- Test execution results (executed, not executed, passed, failed)
- Defect data directly associated with these user stories

### Exclusions

- Integration tests, system tests, or performance tests
- User stories not mapped to test cases
- External or unrelated defect logs

---

## 2. Test Coverage Summary

**Total User Stories:** 9

**Coverage Details:**

| Metric | Count | Description |
|--------|-------|-------------|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 9 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

### Coverage Gap Details

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---------------|-------|---------------------|--------------|------------------|
| LZ-001 | AC1 | Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | High | Partially Covered |
| LZ-001 | AC2 | Resource Group Alignment: Given a new project onboarding, when resources are deployed, then they must be grouped into Resource Groups based on the environment. | High | Partially Covered |
| LZ-001 | AC3 | Naming Convention Validation: Given resource creation, when a name is assigned, then it must follow the defined enterprise naming standards or be blocked by policy. | High | Partially Covered |
| LZ-001 | AC4 | Connectivity Check: Given network segmentation, when resources in Dev attempt to access Prod, then the connection must be blocked by default. | High | Partially Covered |
| LZ-001 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | High | Partially Covered |
| BRZ-001 | AC1 | Connectivity Verification: Given an ADF pipeline, when connecting to an on-prem SQL database, then it must use a Self-Hosted Integration Runtime. | High | Partially Covered |
| BRZ-001 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | High | Partially Covered |
| BRZ-001 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | Medium | Partially Covered |
| BRZ-001 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | High | Partially Covered |
| BRZ-001 | AC5 | Schema Drift Handling: Given a change in source table schema, when the ingestion runs, then the pipeline must not fail and should capture the new columns. | High | Partially Covered |
| STG-001 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | High | Partially Covered |
| STG-001 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | Medium | Partially Covered |
| STG-001 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | Medium | Partially Covered |
| STG-001 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed or Customer-managed keys. | Critical | Partially Covered |
| STG-001 | AC5 | Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access. | Critical | Partially Covered |
| BRZ-002 | AC1 | Event Capture: Given an Event Hub stream, when data is received, then it must be automatically captured into ADLS Gen2 in Avro/Parquet format. | High | Partially Covered |
| BRZ-002 | AC2 | Partitioning: Given high-volume streams, when data is stored, then it must be partitioned by year/month/day/hour for performance. | High | Partially Covered |
| BRZ-002 | AC3 | Schema Validation: Given an incoming JSON payload, when it does not match the registered schema, then it must be routed to a "dead-letter" folder for review. | High | Partially Covered |
| BRZ-002 | AC4 | Latency SLA: Given the streaming ingestion, when a message enters Event Hub, then it must be visible in the Bronze layer within 5 minutes. | High | Partially Covered |
| BRZ-002 | AC5 | Scaling: Given a spike in event volume, when throughput exceeds limits, then the Event Hub must auto-scale to prevent data loss. | High | Partially Covered |
| SEC-001 | AC1 | Identity Creation: Given a new ADF instance, when deployed, then a System-Assigned Managed Identity must be enabled. | Critical | Partially Covered |
| SEC-001 | AC2 | RBAC Assignment: Given the ADF identity, when accessing ADLS Gen2, then it must be assigned the "Storage Blob Data Contributor" role. | Critical | Partially Covered |
| SEC-001 | AC3 | No-Key Policy: Given a Linked Service configuration, when connecting to Azure SQL or Storage, then the "Managed Identity" authentication method must be selected. | Critical | Partially Covered |
| SEC-001 | AC4 | Key Vault Integration: Given secret retrieval, when ADF needs a third-party API key, then it must use its identity to fetch the secret from Azure Key Vault. | High | Partially Covered |
| SEC-001 | AC5 | Audit Trail: Given an access attempt, when the ADF identity requests a resource, then the action must be logged in the Azure Activity Log with the Identity ID. | High | Partially Covered |
| SLV-001 | AC1 | Standardized Date Formats: Given raw source data, when processed into the Silver layer, then all date columns must be converted to ISO 8601 format (YYYY-MM-DD). | High | Partially Covered |
| SLV-001 | AC5 | Schema Enforcement: Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | Critical | Partially Covered |
| SLV-002 | AC1 | Merge Operation Efficiency: Given incremental data in Bronze, when loading to Silver, then the system must perform a UPSERT (Merge) based on the unique Business Key. | High | Partially Covered |
| SLV-002 | AC2 | Hard Delete Handling: Given a record is deleted in the source system, when the CDC pipeline runs, then the corresponding record in the Silver Delta table must be logically or physically deleted. | High | Partially Covered |
| SLV-002 | AC3 | Audit Column Updates: Given a record update, when the Merge occurs, then the 'UpdateTimestamp' and 'SourceSystem' metadata columns must be refreshed. | Medium | Partially Covered |
| SLV-002 | AC4 | Processing Log: Given a pipeline execution, when the CDC logic completes, then the number of inserted, updated, and deleted rows must be logged in the monitoring table. | Medium | Partially Covered |
| SLV-002 | AC5 | Watermark Management: Given a batch run, when successful, then the high-watermark timestamp must be updated to ensure the next run only picks up new data. | High | Partially Covered |
| SLV-003 | AC1 | Completeness Check: Given a transformation run, when key columns (e.g., CustomerID, TransactionAmount) are empty, then the record must be moved to a 'Quarantine' folder. | High | Partially Covered |
| SLV-003 | AC2 | Range and Boundary Validation: Given numeric fields (e.g., Age, Price), when values fall outside of predefined logical ranges, then an alert must be triggered. | High | Partially Covered |
| SLV-003 | AC3 | Referential Integrity: Given a transaction record, when the associated Master Key (e.g., ProductID) does not exist in the reference table, then the record must be flagged as an orphan. | High | Partially Covered |
| SLV-003 | AC4 | Automated DQ Reporting: Given the completion of a Silver load, when quality checks finish, then a summary report (Pass/Fail counts) must be generated for the dashboard. | Medium | Partially Covered |
| SLV-003 | AC5 | Stop-on-Failure Threshold: Given a high error rate (e.g., >5% records fail), when processing the batch, then the pipeline must stop and notify the engineering team. | High | Partially Covered |
| GLD-001 | AC4 | Performance Partitioning: Given large datasets in Gold, when stored in Synapse/Fabric, then tables must be partitioned by 'Business Period' (e.g., Fiscal Year) for query optimization. | High | Partially Covered |
| GLD-001 | AC5 | Data Freshness SLA: Given a business day, when a user queries the Gold layer at 8:00 AM, then the data must reflect all transactions up to the previous midnight. | High | Partially Covered |

### Coverage Score

| User Story ID | Coverage Score | Color Indicator |
|---------------|----------------|------------------|
| LZ-001 | 0.00% | 🔴 Red |
| BRZ-001 | 0.00% | 🔴 Red |
| STG-001 | 0.00% | 🔴 Red |
| BRZ-002 | 0.00% | 🔴 Red |
| SEC-001 | 0.00% | 🔴 Red |
| SLV-001 | 60.00% | 🔴 Red |
| SLV-002 | 0.00% | 🔴 Red |
| SLV-003 | 0.00% | 🔴 Red |
| GLD-001 | 60.00% | 🔴 Red |

**Legend:**

- 🟢 Green (90–100%) → High coverage (meets quality expectations)
- 🟡 Amber (70–89%) → Moderate coverage (requires attention)
- 🔴 Red (<70%) → Low coverage (critical gaps present)

### Coverage Score Analysis

**Formula:**

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

**Definition:**

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

**Components:**

- **Covered Acceptance Criteria:** Number of acceptance criteria that have at least one mapped test case
- **Total Acceptance Criteria:** Total number of acceptance criteria defined across user stories

---

## 3. Test Execution Summary

**Total Test Cases Executed:** 30

**Total Test Cases Not Executed:** 105

**Total Test Cases Passed:** 26

**Total Test Cases Failed:** 4

**Execution Success Rate:** 86.67%

### Test Execution Summary Details

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---------------|------------------|----------|--------------|--------|--------|----------------|------------|
| LZ-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| BRZ-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| STG-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| BRZ-002 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| SEC-001 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| SLV-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| SLV-002 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| SLV-003 | 15 | 0 | 15 | 0 | 0 | 0.00% | 0.00% |
| GLD-001 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |

---

## 4. Defect Details

**Defect Rate:** 3.00%

### Defect Rate Analysis

**Formula:**

Defect Rate = (Total Defects / Total Test Cases) × 100

**Definition:**

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

**Components:**

- **Total Defects:** Total number of defects identified during the test cycle
- **Total Test Cases:** Total number of test cases executed

### Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|-----------|--------------|---------------|--------------|-------------------|----------|----------|--------|
| DEF_SLV-001_001 | UT_SLV-001_001 | SLV-001 | Date Standardization Error | Date Standardization Error. Functionality Check: ISO 8601 conversion. Actual Behavior: Dates remained in MM/DD/YYYY format in the Delta table. | Data Transformation | High | Open |
| DEF_SLV-001_014 | UT_SLV-001_014 | SLV-001 | Schema Enforcement Failure | Schema Enforcement Failure. Functionality Check: Block write on schema mismatch. Actual Behavior: Data with additional columns was successfully appended, breaking downstream dependencies. | Schema Enforcement | Critical | Open |
| DEF_GLD-001_005 | UT_GLD-001_005 | GLD-001 | Freshness SLA Breach | Freshness SLA Breach. Functionality Check: Midnight transaction availability by 8 AM. Actual Behavior: Data only reflected transactions up to 6 PM previous day due to batch lag. | Data Freshness | High | Open |
| DEF_GLD-001_014 | UT_GLD-001_014 | GLD-001 | Partitioning Logic Failure | Partitioning Logic Failure. Functionality Check: Fiscal Year partitioning. Actual Behavior: All data was written to the default partition, degrading query performance. | Performance Optimization | High | Open |

---

## 5. Conclusion

### Summary of Findings

The analysis indicates 9 user stories reviewed with 45 total acceptance criteria. Coverage distribution shows 0 fully covered, 9 partially covered, and 0 not covered user stories. The execution success rate reflects 86.67% with a defect rate of 3.00%.

### Final Outcome Statement

Results show that the overall average coverage score of 13.33%, overall execution stability of 86.67%, and defect severity rate of 100.00% indicate critical gaps in test coverage and functional defects requiring immediate attention.

### Conclusion Statement

The current coverage and quality are insufficient to proceed. Remediation is required before progression due to low coverage rates and critical functional defects in data transformation and schema enforcement.

---

**Report Generated:** Unit Test Quality & Coverage Report

**Document Version:** 1.0

**Status:** Final

---