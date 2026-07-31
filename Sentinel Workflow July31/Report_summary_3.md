<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 19 user stories (SCM-001 through SCM-019) based on the uploaded user story, unit test plan, and unit test execution log documents. A total of 285 test cases and 283 test log entries were derived from source files; 2 planned test cases do not have corresponding executable log entries due to missing execution rows in SCM-003 for TP_SCM3_014 and TP_SCM3_015. All 19 user stories contain identifiable IDs, titles, and acceptance criteria; test plans contain test case IDs and AC mappings; test logs contain per-test execution results, though several rows use inconsistent status terminology and some rows are marked Pass/Passed while stating “not yet executed” or “Pending,” creating execution record integrity concerns.

No standalone defect log documents were provided; defect details were derived from defect references embedded in the test log files. Overall scope includes 95 acceptance criteria across 19 user stories.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date required by AC is not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date required by AC is not explicitly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date required by AC is not explicitly validated in audit log testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes required by AC are not explicitly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase for exactly 50% increase exists in plan but no corresponding test log entry. | Partially Covered |
| SCM-005 | AC4 | Reminder log AC requires channel used and delivery status; only IDs and failed delivery status are explicitly validated, positive validation of channel used is missing. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount required by AC is not explicitly covered in planned testcase wording and is evidenced by execution failure. | Partially Covered |
| SCM-006 | AC4 | Audit log AC requires previous plan, downgraded plan, effective date, credit issued, and timestamp; planned audit testcase validates only customer ID and subscription ID, with separate edge validation for $0 credit. | Partially Covered |
| SCM-006 | AC5 | Customer retention review required by AC is not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC3 | Billing change summary required by AC is not explicitly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Audit log AC requires subscription ID, transfer date, authorization reference, and timestamp; planned coverage explicitly validates owner IDs and authorization reference for bulk API, but full field completeness is not directly evidenced. | Partially Covered |

# Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Test case exists in test plan but no corresponding execution row in test log. | SCM-003 | AC1 | High |
| TP_SCM3_015 | Missing Test Log | Test case exists in test plan but no corresponding execution row in test log. | SCM-003 | AC5 | High |
| UT_SCM1_014 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_001 to UT_SCM8_015 vs TP_SCM8_001 to TP_SCM8_015 | ID Mismatch | Test plan uses TP_ prefix while test log uses UT_ prefix for the same SCM-008 story, causing inferable but non-direct mapping. | SCM-008 | Multiple | Medium |
| UT_SCM8_014 | Pending Execution | Test log explicitly shows Pending for zero-point redemption boundary test. | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Pending Execution | Test log explicitly shows Pending for exact 5000-point approval boundary test. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Pending Execution | Edge case testcase present in log but marked Pending. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Edge case testcase present in log but marked Pending. | SCM-009 | AC5 | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Test case exists in test plan but no corresponding execution row in test log. | SCM-003 | AC1 | High |
| TP_SCM3_015 | Missing Test Log | Test case exists in test plan but no corresponding execution row in test log. | SCM-003 | AC5 | High |
| UT_SCM1_014 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Execution Status Conflict | Logged as Passed, but actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_001 to UT_SCM8_015 vs TP_SCM8_001 to TP_SCM8_015 | ID Mismatch | Test plan uses TP_ prefix while test log uses UT_ prefix for the same SCM-008 story, causing inferable but non-direct mapping. | SCM-008 | Multiple | Medium |
| UT_SCM8_014 | Pending Execution | Test log explicitly shows Pending for zero-point redemption boundary test. | SCM-008 | AC2 | Medium |
| UT_SCM8_015 | Pending Execution | Test log explicitly shows Pending for exact 5000-point approval boundary test. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Pending Execution | Edge case testcase present in log but marked Pending. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Pending Execution | Edge case testcase present in log but marked Pending. | SCM-009 | AC5 | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 285 |
| Total test logs | 283 |
| Missing test cases | 0 |
| Missing test logs | 2 |
| Consistency status | Partially Consistent |

# Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
| SCM-001 | AC2 | DEF-SCM1-001 | UT_SCM1_005 | Notification template rendering issue |
| SCM-001 | AC5 | DEF-SCM1-002 | UT_SCM1_009 | Refund workflow synchronization error |
| SCM-002 | AC4 | DEF-SCM2-101 | TP_SCM2_008 | Pause reason not captured consistently |
| SCM-002 | AC5 | DEF-SCM2-102 | TP_SCM2_009 | Activation allowed without completed approval |
| SCM-003 | AC2 | DEF-SCM3-101 | TP_SCM3_004 | Revised billing amount not included in upgrade confirmation notification |
| SCM-003 | AC5 | DEF-SCM3-102 | TP_SCM3_009 | Manager approval workflow not initiated when price increase equals exactly 50% |
| SCM-004 | AC2 | DEF-SCM4-101 | TP_SCM4_004 | Applicable refund details not included in cancellation confirmation notification |
| SCM-004 | AC5 | DEF-SCM4-102 | TP_SCM4_009 | Finance team approval workflow fails for mixed currency outstanding balances |
| SCM-005 | AC2 | DEF-SCM5-101 | TP_SCM5_005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| SCM-005 | AC1 | DEF-SCM5-103 | TP_SCM5_011 | System sends reminder even when subscription expiry date is null |
| SCM-005 | AC5 | DEF-SCM5-104 | TP_SCM5_013 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| SCM-005 | AC4 | DEF-SCM5-105 | TP_SCM5_015 | Reminder log delivery status remains blank when notification channel fails |
| SCM-006 | AC2 | DEF-SCM6-101 | TP_SCM6_005 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| SCM-006 | AC4 | DEF-SCM6-102 | TP_SCM6_012 | Audit log not created when downgrade results in zero credit amount |
| SCM-006 | AC5 | DEF-SCM6-103 | TP_SCM6_015 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| SCM-007 | AC2 | DEF-SCM7-101 | TP_SCM7_005 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| SCM-007 | AC5 | DEF-SCM7-102 | TP_SCM7_012 | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| SCM-007 | AC4 | DEF-SCM7-103 | TP_SCM7_014 | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| SCM-007 | AC2 | DEF-SCM7-101 | TP_SCM7_015 | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| SCM-008 | AC1 | DEF-SCM8-001 | UT_SCM8_003 | Points posting service delay |
| SCM-008 | AC3 | DEF-SCM8-002 | UT_SCM8_007 | Balance refresh cache issue |
| SCM-008 | AC5 | DEF-SCM8-003 | UT_SCM8_009 | Redemption workflow synchronization issue |
| SCM-009 | AC2 | DEF-SCM9-001 | UT_SCM9_004 | SMS gateway timeout prevents delivery |
| SCM-009 | AC3 | DEF-SCM9-002 | UT_SCM9_012 | Push notification service ignores user preference flag |
| SCM-010 | AC2 | DEF-SCM10-001 | UT_SCM10_005 | Alert content template renders incorrect quantity field |
| SCM-010 | AC5 | DEF-SCM10-002 | UT_SCM10_009 | Approval workflow fails to trigger for bulk adjustments processed in the same batch |
| SCM-011 | AC2 | DEF-SCM11-001 | UT_SCM11_005 | Notification template does not populate requestor details field |
| SCM-011 | AC5 | DEF-SCM11-002 | UT_SCM11_009 | Director approval routing fails when requestor and approver are in different cost centers |
| SCM-012 | AC2 | DEF-SCM12-001 | UT_SCM12_005 | Notification content omits carrier name for multi-leg shipments |
| SCM-012 | AC5 | DEF-SCM12-002 | UT_SCM12_009 | Escalation event not raised when delay spans a carrier handoff |
| SCM-013 | AC2 | DEF-SCM13-001 | UT_SCM13_005 | Notification omits prior score for comparison in change summary |
| SCM-013 | AC5 | DEF-SCM13-002 | UT_SCM13_009 | Corrective action plan workflow does not trigger for suppliers with missing cost metric |
| SCM-014 | AC2 | DEF-SCM14-001 | UT_SCM14_005 | Notification fails to include picker ID for multi-picker orders |
| SCM-014 | AC5 | DEF-SCM14-002 | UT_SCM14_009 | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order |
| SCM-015 | AC2 | DEF-SCM15-001 | UT_SCM15_005 | Notification template renders incorrect item SKU for bundled returns |
| SCM-015 | AC5 | DEF-SCM15-002 | UT_SCM15_009 | QC inspection workflow fails to trigger for multi-item returns totaling above $500 |
| SCM-016 | AC2 | DEF-SCM16-001 | UT_SCM16_005 | Notification content shows stale forecast value from prior run |
| SCM-016 | AC5 | DEF-SCM16-002 | UT_SCM16_009 | Planner review workflow does not trigger when variance calculation crosses a category re-mapping |
| SCM-017 | AC2 | DEF-SCM17-001 | UT_SCM17_005 | Notification omits PO number when invoice references multiple line items |
| SCM-017 | AC5 | DEF-SCM17-002 | UT_SCM17_009 | Manager review workflow fails to trigger when discrepancy results from a currency conversion rounding difference |
| SCM-018 | AC2 | DEF-SCM18-001 | UT_SCM18_005 | Notification fails to send when SKU has an associated substitute item mapping |
| SCM-018 | AC5 | DEF-SCM18-002 | UT_SCM18_009 | Escalation workflow does not trigger when backorder is partially fulfilled before day 14 |
| SCM-019 | AC2 | DEF-SCM19-001 | UT_SCM19_005 | Notification fails to identify destination warehouse manager when transfer spans regions |
| SCM-019 | AC5 | DEF-SCM19-002 | UT_SCM19_009 | Regional manager approval workflow not triggered when transfer is split across multiple shipments |

# Conclusion

Unit test coverage is broadly strong at 88.42% fully covered ACs, but the test set is not fully audit-ready due to 11 partially covered ACs, 2 missing execution logs, multiple execution status conflicts, and 43 unique defects across all 19 user stories. Remediation should prioritize correcting execution record integrity, completing missing and pending boundary test evidence, and resolving AC2/AC5 workflow and notification defects before declaring the suite compliant.
