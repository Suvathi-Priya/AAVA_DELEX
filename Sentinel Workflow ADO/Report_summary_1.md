# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 10 user stories.

These user stories form the baseline for evaluation. The scope is restricted to unit test coverage, unit test execution records, and defect data directly mapped to these user stories.

Included in scope:

- Unit test cases linked to the identified user stories.
- Test execution results, including executed, not executed, passed, and failed records.
- Defect data directly associated with these user stories.

Excluded from scope:

- Integration tests, system tests, and performance tests.
- User stories not mapped to test cases.
- External or unrelated defect logs.

The baseline reference for measuring coverage, execution success, and defect quality is the set of 10 user stories included in the input data.

## Test Coverage Summary

Total Use Cases: 10

Coverage Details:

| Metric | Count | Description |
|--------------------|-------|-----------------------------------------------------------------------------|
| Fully Covered | 0 | User stories where all acceptance criteria are covered by test cases |
| Partially Covered | 10 | User stories containing a mix of covered and uncovered acceptance criteria |
| Not Covered | 0 | User stories where none of the acceptance criteria are covered by test cases |

Coverage Gap Details:

| User Story ID | AC ID | Acceptance Criteria | Impact Level | Coverage Status |
|---|---|---|---|---|
| 1844 | AC1 | Connectivity Verification: Given an ADF pipeline, when connecting to an on-prem SQL database, then it must use a Self-Hosted Integration Runtime. | Medium | Partially Covered |
| 1844 | AC2 | Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro). | Medium | Partially Covered |
| 1844 | AC3 | Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended. | Medium | Partially Covered |
| 1844 | AC4 | Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert. | High | Partially Covered |
| 1844 | AC5 | Schema Drift Handling: Given a change in source table schema, when the ingestion runs, then the pipeline must not fail and should capture the new columns. | Medium | Partially Covered |
| 1858 | AC1 | Completeness Check Given a transformation run, when key columns (e.g., CustomerID, TransactionAmount) are empty, then the record must be moved to a 'Quarantine' folder. | High | Partially Covered |
| 1858 | AC2 | Range and Boundary Validation Given numeric fields (e.g., Age, Price), when values fall outside of predefined logical ranges, then an alert must be triggered. | Medium | Partially Covered |
| 1858 | AC3 | Referential Integrity Given a transaction record, when the associated Master Key (e.g., ProductID) does not exist in the reference table, then the record must be flagged as an orphan. | Medium | Partially Covered |
| 1858 | AC4 | Automated DQ Reporting Given the completion of a Silver load, when quality checks finish, then a summary report (Pass/Fail counts) must be generated for the dashboard. | Medium | Partially Covered |
| 1858 | AC5 | Stop-on-Failure Threshold Given a high error rate (e.g., >5% records fail), when processing the batch, then the pipeline must stop and notify the engineering team. | High | Partially Covered |
| 1846 | AC1 | Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created. | Medium | Partially Covered |
| 1846 | AC2 | Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance). | Medium | Partially Covered |
| 1846 | AC3 | Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy. | Medium | Partially Covered |
| 1846 | AC4 | Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed or Customer-managed keys. | Critical | Partially Covered |
| 1846 | AC5 | Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access. | Critical | Partially Covered |
| 1850 | AC1 | Identity Creation: Given a new ADF instance, when deployed, then a System-Assigned Managed Identity must be enabled. | Critical | Partially Covered |
| 1850 | AC2 | RBAC Assignment: Given the ADF identity, when accessing ADLS Gen2, then it must be assigned the "Storage Blob Data Contributor" role. | Critical | Partially Covered |
| 1850 | AC3 | No-Key Policy: Given a Linked Service configuration, when connecting to Azure SQL or Storage, then the "Managed Identity" authentication method must be selected. | Critical | Partially Covered |
| 1850 | AC4 | Key Vault Integration: Given secret retrieval, when ADF needs a third-party API key, then it must use its identity to fetch the secret from Azure Key Vault. | Critical | Partially Covered |
| 1850 | AC5 | Audit Trail: Given an access attempt, when the ADF identity requests a resource, then the action must be logged in the Azure Activity Log with the Identity ID. | Critical | Partially Covered |
| 1860 | AC1 | Merge Operation Efficiency Given incremental data in Bronze, when loading to Silver, then the system must perform a UPSERT (Merge) based on the unique Business Key. | Medium | Partially Covered |
| 1860 | AC2 | Hard Delete Handling Given a record is deleted in the source system, when the CDC pipeline runs, then the corresponding record in the Silver Delta table must be logically or physically deleted. | Medium | Partially Covered |
| 1860 | AC3 | Audit Column Updates Given a record update, when the Merge occurs, then the 'UpdateTimestamp' and 'SourceSystem' metadata columns must be refreshed. | Medium | Partially Covered |
| 1860 | AC4 | Processing Log Given a pipeline execution, when the CDC logic completes, then the number of inserted, updated, and deleted rows must be logged in the monitoring table. | Medium | Partially Covered |
| 1860 | AC5 | Watermark Management Given a batch run, when successful, then the high-watermark timestamp must be updated to ensure the next run only picks up new data. | Medium | Partially Covered |
| 1854 | AC1 | Star Schema Implementation Given cleansed Silver data, when modeled in the Gold layer, then it must be structured into Fact and Dimension tables. | Medium | Partially Covered |
| 1854 | AC2 | Calculated KPI Measures Given sales data, when loaded to Gold, then standard KPIs (e.g., Year-to-Date Revenue, Margin %) must be pre-calculated. | Medium | Partially Covered |
| 1854 | AC3 | Customer 360 View Given multiple source domains (Sales, Support, Marketing), when joined in Gold, then a unified 'Customer 360' view must be available. | Medium | Partially Covered |
| 1854 | AC4 | Performance Partitioning Given large datasets in Gold, when stored in Synapse/Fabric, then tables must be partitioned by 'Business Period' (e.g., Fiscal Year) for query optimization. | Medium | Partially Covered |
| 1854 | AC5 | Data Freshness SLA Given a business day, when a user queries the Gold layer at 8:00 AM, then the data must reflect all transactions up to the previous midnight | Medium | Partially Covered |
| 1852 | AC1 | Standardized Date Formats Given raw source data, when processed into the Silver layer, then all date columns must be converted to ISO 8601 format (YYYY-MM-DD). | Medium | Partially Covered |
| 1852 | AC2 | Null Value Handling Given mandatory business fields, when a null value is detected, then the record must be flagged or assigned a default 'Unknown' value based on the data dictionary. | Medium | Partially Covered |
| 1852 | AC3 | Deduplication Logic Given multiple records with the same Primary Key, when loading into Delta tables, then only the latest record based on the 'LoadTimestamp' must be retained. | Medium | Partially Covered |
| 1852 | AC4 | Unit of Measure Conversion Given disparate source systems, when currency or measurements are ingested, then they must be converted to the enterprise standard (e.g., USD, Metric) in the Silver layer. | Medium | Partially Covered |
| 1852 | AC5 | Schema Enforcement Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption. | High | Partially Covered |
| 1836 | AC1 | Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod. | Medium | Partially Covered |
| 1836 | AC2 | Resource Group Alignment: Given a new project onboarding, when resources are deployed, then they must be grouped into Resource Groups based on the environment. | Medium | Partially Covered |
| 1836 | AC3 | Naming Convention Validation: Given resource creation, when a name is assigned, then it must follow the defined enterprise naming standards or be blocked by policy. | High | Partially Covered |
| 1836 | AC4 | Connectivity Check: Given network segmentation, when resources in Dev attempt to access Prod, then the connection must be blocked by default. | High | Partially Covered |
| 1836 | AC5 | Cost Center Tagging: Given any resource deployment, when the "Cost Center" tag is missing, then the deployment must fail validation. | High | Partially Covered |
| 1856 | AC1 | RBAC Group Assignment Given the Gold environment, when a user requests access, then permissions must be granted via Microsoft Entra ID groups (e.g., 'Finance_Analyst' vs 'HR_Admin'). | Critical | Partially Covered |
| 1856 | AC2 | PII Data Masking Given columns identified as PII (e.g., SSN, Email), when queried by non-authorized users, then the data must be masked (e.g., XXX-XX-1234). | Critical | Partially Covered |
| 1856 | AC3 | Row-Level Security (RLS) Given a global sales report, when a regional manager logs in, then they must only see data associated with their specific region. | Critical | Partially Covered |
| 1856 | AC4 | Key Vault Secret Rotation Given application secrets, when accessed by the reporting layer, then they must be retrieved from Azure Key Vault with no hardcoded values. | Critical | Partially Covered |
| 1856 | AC5 | Audit Logging for Sensitive Access Given a query on 'Confidential' data, when executed, then the User ID, Timestamp, and Query string must be logged for compliance audit. | Critical | Partially Covered |
| 1848 | AC1 | Event Capture: Given an Event Hub stream, when data is received, then it must be automatically captured into ADLS Gen2 in Avro/Parquet format. | Medium | Partially Covered |
| 1848 | AC2 | Partitioning: Given high-volume streams, when data is stored, then it must be partitioned by year/month/day/hour for performance. | Medium | Partially Covered |
| 1848 | AC3 | Schema Validation: Given an incoming JSON payload, when it does not match the registered schema, then it must be routed to a "dead-letter" folder for review. | High | Partially Covered |
| 1848 | AC4 | Latency SLA: Given the streaming ingestion, when a message enters Event Hub, then it must be visible in the Bronze layer within 5 minutes. | Medium | Partially Covered |
| 1848 | AC5 | Scaling: Given a spike in event volume, when throughput exceeds limits, then the Event Hub must auto-scale to prevent data loss. | Medium | Partially Covered |

| User Story ID | Coverage Score | Color |
|---|---:|---|
| 1844 | 50.00% | 🔴 Red |
| 1858 | 50.00% | 🔴 Red |
| 1846 | 50.00% | 🔴 Red |
| 1850 | 50.00% | 🔴 Red |
| 1860 | 50.00% | 🔴 Red |
| 1854 | 50.00% | 🔴 Red |
| 1852 | 50.00% | 🔴 Red |
| 1836 | 50.00% | 🔴 Red |
| 1856 | 50.00% | 🔴 Red |
| 1848 | 50.00% | 🔴 Red |

Legend:

- 🟢 Green (90–100%) → High coverage
- 🟠 Amber (70–89%) → Moderate coverage
- 🔴 Red (<70%) → Low coverage

Coverage Score Analysis:

Coverage % = (Covered Acceptance Criteria / Total Acceptance Criteria) × 100

Description:

Coverage Percentage measures the extent to which acceptance criteria are validated by corresponding test cases. It indicates how completely the defined requirements are covered through testing.

Components:

- Covered Acceptance Criteria: Number of acceptance criteria that have at least one mapped test case
- Total Acceptance Criteria: Total number of acceptance criteria defined across user stories

## Test Execution Summary

Total Test Cases Executed: 150

Total Test Cases Not Executed: 0

Total Test Cases Passed: 135

Total Test Cases Failed: 15

Execution Success Rate: 90.00%

Test Execution Summary Details:

| User Story ID | Total Test Cases | Executed | Not Executed | Passed | Failed | Execution Rate | Pass Rate |
|---|---:|---:|---:|---:|---:|---:|---:|
| 1844 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| 1858 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| 1846 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| 1850 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| 1860 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| 1854 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| 1852 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| 1836 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |
| 1856 | 15 | 15 | 0 | 13 | 2 | 100.00% | 86.67% |
| 1848 | 15 | 15 | 0 | 14 | 1 | 100.00% | 93.33% |

## Defect Details

Defect Rate: 10.00%

Defect Rate Analysis:

Defect Rate = (Total Defects / Total Test Cases) × 100

Description:

Defect Rate measures the proportion of defects identified during testing relative to the total number of test cases executed. It is a key quality metric used to evaluate system stability and testing effectiveness.

Components:

- Total Defects: Total number of defects identified during the test cycle
- Total Test Cases: Total number of test cases executed

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description | Category | Severity | Status |
|---|---|---|---|---|---|---|---|
| DEF_SEC-002_002 | UT_SEC-002_002 | 1856 | PII Masking Failure | PII Masking Failure. Functionality Check: SSN column masking. Actual Behavior: SSN was visible in plain text for users in 'Marketing_Analyst' group. | security_compliance | critical | open |
| DEF_SEC-002_003 | UT_SEC-002_003 | 1856 | RLS Logic Error | RLS Logic Error. Functionality Check: Regional Sales filtering. Actual Behavior: Regional managers could see global data due to missing filter predicate in the view. | security_compliance | critical | open |
| DEF_SLV-003_001 | UT_SLV-003_001 | 1858 | Completeness Check Bypass | Completeness Check Bypass. Functionality Check: CustomerID null check. Actual Behavior: Records with NULL CustomerID were loaded to Silver instead of being quarantined. | policy_enforcement | high | open |
| DEF_SLV-003_015 | UT_SLV-003_015 | 1858 | Stop-on-Failure Threshold | Stop-on-Failure Threshold. Functionality Check: 5% error threshold. Actual Behavior: Pipeline continued processing despite a 12% error rate in the current batch. | policy_enforcement | high | open |
| DEF_SLV-002_002 | UT_SLV-002_002 | 1860 | MERGE Logic Error | MERGE Logic Error. Functionality Check: Duplicate avoidance. Actual Behavior: MERGE operation created duplicate records in Silver for existing Business Keys. | functional | medium | open |
| DEF_SLV-002_012 | UT_SLV-002_012 | 1860 | Watermark Update Failure | Watermark Update Failure. Functionality Check: High-watermark timestamp. Actual Behavior: Watermark was not updated post-success, causing the next run to re-process old data. | functional | medium | open |
| DEF_LZ-001_005 | UT_LZ-001_005 | 1836 | Tagging Policy Bypass | Tagging Policy Bypass. Functionality Check: Mandatory 'Cost Center' tag. Actual Behavior: Resource was successfully deployed via Terraform without the tag, indicating Policy was not in Enforce mode, violating AC5. | policy_enforcement | high | open |
| DEF_BRZ-001_013 | UT_BRZ-001_013 | 1844 | Retry Logic Failure | Retry Logic Failure. Functionality Check: 3x Automated Retries. Actual Behavior: Pipeline failed immediately upon first network timeout without triggering retry attempts, violating AC4. | policy_enforcement | high | open |
| DEF_STG-001_009 | UT_STG-001_009 | 1846 | RBAC Isolation Leak | RBAC Isolation Leak. Functionality Check: Denial of /gold container access. Actual Behavior: User with 'Bronze Reader' was able to view 'Gold' file metadata due to incorrect ACL inheritance, violating AC5. | security_compliance | critical | open |
| DEF_BRZ-002_012 | UT_BRZ-002_012 | 1848 | Ingestion Latency Breach | Ingestion Latency Breach. Functionality Check: 5-minute visibility SLA. Actual Behavior: Streaming data took 7 minutes to appear in ADLS due to Event Hub capture lag, violating AC4. | functional | medium | open |
| DEF_SEC-001_004 | UT_SEC-001_004 | 1850 | Key Vault Access Failure | Key Vault Access Failure. Functionality Check: Secret retrieval using Managed Identity. Actual Behavior: ADF received 'Access Denied' because the Identity was not added to the Key Vault Access Policy, violating AC4. | security_compliance | critical | open |
| DEF_SLV-001_001 | UT_SLV-001_001 | 1852 | Date Standardization Error | Date Standardization Error. Functionality Check: ISO 8601 conversion. Actual Behavior: Dates remained in MM/DD/YYYY format in the Delta table. | functional | medium | open |
| DEF_SLV-001_014 | UT_SLV-001_014 | 1852 | Schema Enforcement Failure | Schema Enforcement Failure. Functionality Check: Block write on schema mismatch. Actual Behavior: Data with additional columns was successfully appended, breaking downstream dependencies. | policy_enforcement | high | open |
| DEF_GLD-001_005 | UT_GLD-001_005 | 1854 | Freshness SLA Breach | Freshness SLA Breach. Functionality Check: Midnight transaction availability by 8 AM. Actual Behavior: Data only reflected transactions up to 6 PM previous day due to batch lag. | functional | medium | open |
| DEF_GLD-001_014 | UT_GLD-001_014 | 1854 | Partitioning Logic Failure | Partitioning Logic Failure. Functionality Check: Fiscal Year partitioning. Actual Behavior: All data was written to the default partition, degrading query performance. | functional | medium | open |

## Conclusion

Summary of Findings:

A total of 10 user stories were reviewed. Coverage distribution shows 0 fully covered, 10 partially covered, and 0 not covered user stories. The overall Test Coverage Rate is 50.00%, the Execution Success Rate is 90.00%, and the Defect Rate is 10.00%.

Final Outcome Statement:

Based on the reported overall Test Coverage Rate of 50.00%, overall Execution Success Rate of 90.00%, and the presence of critical and high severity open defects, the current unit test results indicate incomplete coverage and unresolved defect exposure within the evaluated baseline.

Conclusion Statement:

The current unit test suite is not sufficient to support progression without remediation. Coverage alignment gaps and open defects require correction before progression.