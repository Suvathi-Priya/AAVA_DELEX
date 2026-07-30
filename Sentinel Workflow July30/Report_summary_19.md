<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 17 user stories: SCM-001 through SCM-008, and SCM-010 through SCM-019. A total of 255 test cases were identified in the uploaded unit test plans and 253 corresponding execution log entries were identified in the uploaded test logs.

Across the analyzed scope, 85 acceptance criteria (ACs) were derived from the source user story documents. Document completeness is partially satisfactory: user story, test plan, and test log documents were available for 17 user stories; no defect log documents were provided as separate uploads, so defect details were derived from defect references embedded in the test execution logs. SCM-008 file naming is inconsistent between user story and test artifacts, but inferable and readable. Two planned test cases do not have matching executable log entries: SCM-003 TP_SCM3_014 and TP_SCM3_015 are absent from the execution log. Overall unit test scope includes functional positive, negative, and edge/boundary validation coverage for all available stories.

# Test Coverage Summary

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-002 | AC2 | Resume date not explicitly validated by any mapped test case. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date not explicitly validated by any mapped test case. | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated in audit log coverage. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not explicitly validated by any mapped test case. | Partially Covered |
| SCM-003 | AC5 | Execution log missing for TP_SCM3_015 boundary scenario; threshold interpretation remains weakly evidenced. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used not explicitly validated by mapped test cases. | Partially Covered |
| SCM-005 | AC5 | No explicit positive test validates both recipients for above-threshold high-value subscription. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, and timestamp not explicitly decomposed across test coverage. | Partially Covered |
| SCM-006 | AC5 | Customer retention review not explicitly validated by any mapped test case. | Partially Covered |
| SCM-007 | AC3 | Billing change summary not explicitly validated by any mapped test case. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated; authorization reference covered only in edge scenario and failed. | Partially Covered |
| SCM-010 | AC5 | Reason code not explicitly validated by any mapped test case. | Partially Covered |
| SCM-011 | AC5 | Budget verification not explicitly validated by any mapped test case. | Partially Covered |
| SCM-012 | AC5 | Root-cause review not explicitly validated by any mapped test case. | Partially Covered |
| SCM-013 | AC5 | Quarterly business review not explicitly validated by any mapped test case. | Partially Covered |
| SCM-014 | AC5 | Reason code not explicitly validated by any mapped test case. | Partially Covered |
| SCM-019 | AC5 | Logistics scheduling not explicitly validated by any mapped test case. | Partially Covered |

# Consistency Analysis

| Test Case ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Test case exists in test plan but no execution log entry was found. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Test case exists in test plan but no execution log entry was found. | SCM-003 | AC5 | Medium |
| SCM008 artifacts | Naming Inconsistency | User story file uses SCM-008 while plan/log files use SCM008; mapping is inferable from content. | SCM-008 | NULL | Low |
| UT_SCM1_014 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_001 to UT_SCM8_015 vs TP_SCM8_001 to TP_SCM8_015 | ID Mismatch | Test plan IDs use TP prefix while execution log IDs use UT prefix; AC/story mapping is inferable but not directly consistent. | SCM-008 | Multiple | Medium |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Test case exists in test plan but no execution log entry was found. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Test case exists in test plan but no execution log entry was found. | SCM-003 | AC5 | Medium |
| SCM008 artifacts | Naming Inconsistency | User story file uses SCM-008 while plan/log files use SCM008; mapping is inferable from content. | SCM-008 | NULL | Low |
| UT_SCM1_014 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-001 | AC2 | High |
| UT_SCM1_015 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-001 | AC5 | High |
| TP_SCM2_014 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-002 | AC1 | High |
| TP_SCM2_015 | Status Inconsistency | Execution status marked Passed while actual result states test not yet executed. | SCM-002 | AC5 | High |
| UT_SCM8_001 to UT_SCM8_015 vs TP_SCM8_001 to TP_SCM8_015 | ID Mismatch | Test plan IDs use TP prefix while execution log IDs use UT prefix; AC/story mapping is inferable but not directly consistent. | SCM-008 | Multiple | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total test cases | 255 |
| Total test logs | 253 |
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

Unit test coverage is broad but not fully audit-ready due to 21.18% partially covered ACs, two missing test log entries, and multiple status/mapping inconsistencies. Remediation should prioritize correction of execution log integrity issues, closure of explicit AC coverage gaps, and resolution of the 42 reported defects before sign-off.
