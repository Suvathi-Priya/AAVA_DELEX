# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

{
  "user_stories": [
    {
      "user_story_id": "LZ-001",
      "title": "Implement Enterprise Subscription Strategy",
      "description": "As an Azure Cloud Architect, I want to establish a multi-subscription strategy, so that workloads are isolated and managed according to enterprise governance standards.",
      "acceptance_criteria": [
        "AC1: Subscription Separation: Given the landing zone setup, when environments are created, then separate subscriptions must be used for Dev, QA, and Prod.",
        "AC2: Resource Group Alignment: Given a new project onboarding, when resources are deployed, then they must be grouped into Resource Groups based on the environment.",
        "AC3: Naming Convention Validation: Given resource creation, when a name is assigned, then it must follow the defined enterprise naming standards or be blocked by policy.",
        "AC4: Connectivity Check: Given network segmentation, when resources in Dev attempt to access Prod, then the connection must be blocked by default.",
        "AC5: Cost Center Tagging: Given any resource deployment, when the \"Cost Center\" tag is missing, then the deployment must fail validation."
      ]
    },
    {
      "user_story_id": "BRZ-001",
      "title": "Configure Batch Ingestion from On-Prem Databases",
      "description": "As a Data Engineer, I want to ingest raw data from on-premises databases into the Bronze ADLS Gen2 layer, so that data is available for downstream transformation.",
      "acceptance_criteria": [
        "AC1: Connectivity Verification: Given an ADF pipeline, when connecting to an on-prem SQL database, then it must use a Self-Hosted Integration Runtime.",
        "AC2: Raw Format Preservation: Given the ingestion process, when data is landed in ADLS Gen2, then it must be stored in its source format (e.g., Parquet or Avro).",
        "AC3: Metadata Capture: Given a successful ingestion, when the record is saved, then metadata (source system, load timestamp, file name) must be appended.",
        "AC4: Retry Logic: Given a transient network failure, when the ingestion fails, then the system must automatically retry 3 times before triggering an alert.",
        "AC5: Schema Drift Handling: Given a change in source table schema, when the ingestion runs, then the pipeline must not fail and should capture the new columns."
      ]
    },
    {
      "user_story_id": "STG-001",
      "title": "Implement Hierarchical Namespace for Data Lake",
      "description": "As a Data Architect, I want to configure ADLS Gen2 with a hierarchical namespace, so that data is organized into logical Bronze, Silver, and Gold zones.",
      "acceptance_criteria": [
        "AC1: Zone Creation: Given a new Data Lake account, when initialized, then separate root containers for /bronze, /silver, and /gold must be created.",
        "AC2: Domain Organization: Given the /bronze container, when data is ingested, then it must be organized by domain folders (e.g., /sales, /finance).",
        "AC3: Tiered Storage Policy: Given files in the /bronze layer, when they exceed 90 days of age, then they must automatically move to Cool storage via lifecycle policy.",
        "AC4: Encryption Validation: Given data landing in any zone, when stored at rest, then it must be encrypted using Microsoft-managed or Customer-managed keys.",
        "AC5: Access Control (ACL): Given the folder structure, when a user lacks specific permissions, then they must be denied access to the Gold container even if they have Bronze access."
      ]
    },
    {
      "user_story_id": "BRZ-002",
      "title": "Ingest Streaming Data via Azure Event Hubs",
      "description": "As a Data Engineer, I want to capture real-time streaming data from IoT or SaaS sources, so that time-sensitive data is landed in the Bronze layer immediately.",
      "acceptance_criteria": [
        "AC1: Event Capture: Given an Event Hub stream, when data is received, then it must be automatically captured into ADLS Gen2 in Avro/Parquet format.",
        "AC2: Partitioning: Given high-volume streams, when data is stored, then it must be partitioned by year/month/day/hour for performance.",
        "AC3: Schema Validation: Given an incoming JSON payload, when it does not match the registered schema, then it must be routed to a \"dead-letter\" folder for review.",
        "AC4: Latency SLA: Given the streaming ingestion, when a message enters Event Hub, then it must be visible in the Bronze layer within 5 minutes.",
        "AC5: Scaling: Given a spike in event volume, when throughput exceeds limits, then the Event Hub must auto-scale to prevent data loss."
      ]
    },
    {
      "user_story_id": "SEC-001",
      "title": "Configure Managed Identities for ADF Access",
      "description": "As a Security Engineer, I want to use System-Assigned Managed Identities for Azure Data Factory, so that pipelines can access storage without using hardcoded keys.",
      "acceptance_criteria": [
        "AC1: Identity Creation: Given a new ADF instance, when deployed, then a System-Assigned Managed Identity must be enabled.",
        "AC2: RBAC Assignment: Given the ADF identity, when accessing ADLS Gen2, then it must be assigned the \"Storage Blob Data Contributor\" role.",
        "AC3: No-Key Policy: Given a Linked Service configuration, when connecting to Azure SQL or Storage, then the \"Managed Identity\" authentication method must be selected.",
        "AC4: Key Vault Integration: Given secret retrieval, when ADF needs a third-party API key, then it must use its identity to fetch the secret from Azure Key Vault.",
        "AC5: Audit Trail: Given an access attempt, when the ADF identity requests a resource, then the action must be logged in the Azure Activity Log with the Identity ID."
      ]
    },
    {
      "user_story_id": "SLV-001",
      "title": "",
      "description": "As a Data Engineer, I want to apply cleansing and standardization rules using PySpark in Databricks, so that the data is consistent and reliable for business analysis.",
      "acceptance_criteria": [
        "AC1: Standardized Date Formats",
        "Given raw source data, when processed into the Silver layer, then all date columns must be converted to ISO 8601 format (YYYY-MM-DD).",
        "AC2: Null Value Handling",
        "Given mandatory business fields, when a null value is detected, then the record must be flagged or assigned a default 'Unknown' value based on the data dictionary.",
        "AC3: Deduplication Logic",
        "Given multiple records with the same Primary Key, when loading into Delta tables, then only the latest record based on the 'LoadTimestamp' must be retained.",
        "AC4: Unit of Measure Conversion",
        "Given disparate source systems, when currency or measurements are ingested, then they must be converted to the enterprise standard (e.g., USD, Metric) in the Silver layer.",
        "AC5: Schema Enforcement",
        "Given a Delta table write operation, when the incoming data schema does not match the Silver table definition, then the operation must fail to prevent data corruption."
      ]
    },
    {
      "user_story_id": "SLV-002",
      "title": "",
      "description": "As a Data Engineer, I want to implement CDC logic using Delta Lake 'MERGE' operations, so that the Silver layer accurately reflects the current state of source system changes.",
      "acceptance_criteria": [
        "AC1: Merge Operation Efficiency",
        "Given incremental data in Bronze, when loading to Silver, then the system must perform a UPSERT (Merge) based on the unique Business Key.",
        "AC2: Hard Delete Handling",
        "Given a record is deleted in the source system, when the CDC pipeline runs, then the corresponding record in the Silver Delta table must be logically or physically deleted.",
        "AC3: Audit Column Updates",
        "Given a record update, when the Merge occurs, then the 'UpdateTimestamp' and 'SourceSystem' metadata columns must be refreshed.",
        "AC4: Processing Log",
        "Given a pipeline execution, when the CDC logic completes, then the number of inserted, updated, and deleted rows must be logged in the monitoring table.",
        "AC5: Watermark Management",
        "Given a batch run, when successful, then the high-watermark timestamp must be updated to ensure the next run only picks up new data."
      ]
    },
    {
      "user_story_id": "SLV-003",
      "title": "",
      "description": "As a Data Quality Analyst, I want to execute automated quality checks during the Silver layer transformation, so that sub-standard data is quarantined before reaching the Gold layer.",
      "acceptance_criteria": [
        "AC1: Completeness Check",
        "Given a transformation run, when key columns (e.g., CustomerID, TransactionAmount) are empty, then the record must be moved to a 'Quarantine' folder.",
        "AC2: Range and Boundary Validation",
        "Given numeric fields (e.g., Age, Price), when values fall outside of predefined logical ranges, then an alert must be triggered.",
        "AC3: Referential Integrity",
        "Given a transaction record, when the associated Master Key (e.g., ProductID) does not exist in the reference table, then the record must be flagged as an orphan.",
        "AC4: Automated DQ Reporting",
        "Given the completion of a Silver load, when quality checks finish, then a summary report (Pass/Fail counts) must be generated for the dashboard.",
        "AC5: Stop-on-Failure Threshold",
        "Given a high error rate (e.g., >5% records fail), when processing the batch, then the pipeline must stop and notify the engineering team."
      ]
    },
    {
      "user_story_id": "GLD-001",
      "title": "",
      "description": "As a Business Analyst, I want to access aggregated and modeled data in the Gold layer, so that I can generate KPIs for Sales and Finance without complex joins.",
      "acceptance_criteria": [
        "AC1: Star Schema Implementation",
        "Given cleansed Silver data, when modeled in the Gold layer, then it must be structured into Fact and Dimension tables.",
        "AC2: Calculated KPI Measures",
        "Given sales data, when loaded to Gold, then standard KPIs (e.g., Year-to-Date Revenue, Margin %) must be pre-calculated.",
        "AC3: Customer 360 View",
        "Given multiple source domains (Sales, Support, Marketing), when joined in Gold, then a unified 'Customer 360' view must be available.",
        "AC4: Performance Partitioning",
        "Given large datasets in Gold, when stored in Synapse/Fabric, then tables must be partitioned by 'Business Period' (e.g., Fiscal Year) for query optimization.",
        "AC5: Data Freshness SLA",
        "Given a business day, when a user queries the Gold layer at 8:00 AM, then the data must reflect all transactions up to the previous midnight."
      ]
    },
    {
      "user_story_id": "SEC-002",
      "title": "",
      "description": "As a Security Officer, I want to restrict access to sensitive data in the Gold layer using RBAC and Data Masking, so that PII data is only visible to authorized personnel.",
      "acceptance_criteria": [
        "AC1: RBAC Group Assignment",
        "Given the Gold environment, when a user requests access, then permissions must be granted via Microsoft Entra ID groups (e.g., 'Finance_Analyst' vs 'HR_Admin').",
        "AC2: PII Data Masking",
        "Given columns identified as PII (e.g., SSN, Email), when queried by non-authorized users, then the data must be masked (e.g., XXX-XX-1234).",
        "AC3: Row-Level Security (RLS)",
        "Given a global sales report, when a regional manager logs in, then they must only see data associated with their specific region.",
        "AC4: Key Vault Secret Rotation",
        "Given application secrets, when accessed by the reporting layer, then they must be retrieved from Azure Key Vault with no hardcoded values.",
        "AC5: Audit Logging for Sensitive Access",
        "Given a query on 'Confidential' data, when executed, then the User ID, Timestamp, and Query string must be logged for compliance audit."
      ]
    }
  ]
}

## Test Coverage Summary

No input data provided.

## Test Execution Summary

No input data provided.

## Defect Details

No input data provided.

## Conclusion

No input data provided.
