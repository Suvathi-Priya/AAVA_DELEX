<div align="center">

**UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 17 user stories: SCM-001 to SCM-007 and SCM-010 to SCM-019. For these user stories, 51 source documents were validated and read directly from the uploaded files, comprising 17 user story documents, 17 unit test plan documents, and 17 unit test execution log documents; no standalone defect log documents were provided, so defect details were derived from the execution logs.

Document completeness and integrity status is Partially Complete. All reviewed user story documents contained an identifiable user story ID, title, and acceptance criteria. All reviewed test plan documents contained test case IDs and explicit acceptance-criteria mappings. All reviewed test log documents contained execution results per test case. No unreadable files were encountered in the reviewed set. The uploaded file list indicates SCM-005_User_Story.docx, SCM-006_User_Story.docx, and SCM-004_User_Story.docx are present, but SCM-008 and SCM-009 document sets are not present, and no defect log files were supplied. Total derived metrics for the reviewed scope are: 255.00 planned test cases, 253.00 executed test logs, 0.00 missing test cases, 2.00 missing test logs, and 32.00 derived defects.

# Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC5 | Fraud review obligation not directly validated by any testcase. | Partially Covered |
| SCM-002 | AC2 | Resume date inclusion not directly validated by any testcase. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date visibility not directly validated by any testcase. | Partially Covered |
| SCM-002 | AC4 | Pause start date not explicitly validated in audit log testcase. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes not directly validated by any testcase. | Partially Covered |
| SCM-003 | AC5 | Boundary testcase exists for exactly 50%, but no execution log was provided for TP_SCM3_014 and TP_SCM3_015. | Partially Covered |
| SCM-004 | AC5 | Exact-threshold boundary testcase exists, but no execution log was provided for TP_SCM4_014 and TP_SCM4_015. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used are not directly validated by any testcase. | Partially Covered |
| SCM-005 | AC5 | Positive testcase for notifying both parties above threshold is missing; only boundary and sub-threshold scenarios are present. | Partially Covered |
| SCM-006 | AC2 | Adjusted billing amount is not directly covered by a dedicated testcase; test evidence shows failure against notification content. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, and timestamp are not directly validated by explicit testcase wording. | Partially Covered |
| SCM-006 | AC5 | Customer retention review obligation not directly validated by any testcase. | Partially Covered |
| SCM-007 | AC2 | Transfer details are not explicitly validated as a distinct notification content element. | Partially Covered |
| SCM-007 | AC3 | Billing change summary visibility not directly validated by any testcase. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp are not directly validated by explicit testcase wording. | Partially Covered |
| SCM-010 | AC5 | Reason code obligation not directly validated by any testcase. | Partially Covered |
| SCM-011 | AC5 | Budget verification obligation not directly validated by any testcase. | Partially Covered |
| SCM-012 | AC5 | Root-cause review obligation not directly validated by any testcase. | Partially Covered |
| SCM-013 | AC5 | Quarterly business review obligation not directly validated by any testcase. | Partially Covered |
| SCM-014 | AC5 | Reason code obligation not directly validated by any testcase. | Partially Covered |
| SCM-001 | AC5 | Require manager approval and fraud review for refunds above $1000 | Partially Covered |
| SCM-002 | AC2 | Send pause confirmation with pause start date and resume date | Partially Covered |
| SCM-002 | AC3 | View pause status, pause history, and scheduled resume date in portal | Partially Covered |

# Consistency Analysis

Mapping consistency was derived by checking whether each testcase in the test plan had a clear user story and acceptance criterion mapping and whether each planned testcase had a corresponding execution result in the test log. Most mappings are direct and explicit. The primary inconsistencies identified are missing execution log entries and several testcase/result status wording inconsistencies where status is recorded as "Passed" but the actual result text states "not yet executed."

# Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Testcase present in test plan but no corresponding execution result found in test log. | SCM-003 | AC1 | High |
| TP_SCM3_015 | Missing Test Log | Testcase present in test plan but no corresponding execution result found in test log. | SCM-003 | AC5 | High |
| TP_SCM2_014 | Execution Status Ambiguity | Status recorded as Passed, but actual result states test not yet executed. | SCM-002 | AC1 | Medium |
| TP_SCM2_015 | Execution Status Ambiguity | Status recorded as Passed, but actual result states test not yet executed. | SCM-002 | AC5 | Medium |
| UT_SCM1_014 | Execution Status Ambiguity | Status recorded as Passed, but actual result states test not yet executed. | SCM-001 | AC2 | Medium |
| UT_SCM1_015 | Execution Status Ambiguity | Status recorded as Passed, but actual result states test not yet executed. | SCM-001 | AC5 | Medium |

# Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 255.00 |
| Total Test Logs | 253.00 |
| Missing Test Cases | 0.00 |
| Missing Test Logs | 2.00 |
| Consistency Status | Partially Consistent |

# Defect Details

Defect details were derived from execution logs because no separate defect log files were provided.

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | NULL | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | NULL | Refund workflow synchronization error |
| DEF-SCM2-101 | TP_SCM2_008 | SCM-002 | NULL | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | SCM-002 | NULL | Activation allowed without completed approval |
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | NULL | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | NULL | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | NULL | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | NULL | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | NULL | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | NULL | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | NULL | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | NULL | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | NULL | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | NULL | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | NULL | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM7-101 | TP_SCM7_005 | SCM-007 | NULL | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM7-102 | TP_SCM7_012 | SCM-007 | NULL | Compliance approval workflow not initiated for transfers involving tax jurisdiction change only without entity change |
| DEF-SCM7-103 | TP_SCM7_014 | SCM-007 | NULL | Audit log authorization reference field empty when transfer initiated via bulk admin API |
| DEF-SCM7-101 | TP_SCM7_015 | SCM-007 | NULL | New owner transfer notification not triggered when transfer is initiated via bulk admin API endpoint |
| DEF-SCM10-001 | UT_SCM10_005 | SCM-010 | NULL | Alert content template renders incorrect quantity field |
| DEF-SCM10-002 | UT_SCM10_009 | SCM-010 | NULL | Approval workflow fails to trigger for bulk adjustments processed in the same batch |
| DEF-SCM11-001 | UT_SCM11_005 | SCM-011 | NULL | Notification template does not populate requestor details field |
| DEF-SCM11-002 | UT_SCM11_009 | SCM-011 | NULL | Director approval routing fails when requestor and approver are in different cost centers |
| DEF-SCM12-001 | UT_SCM12_005 | SCM-012 | NULL | Notification content omits carrier name for multi-leg shipments |
| DEF-SCM12-002 | UT_SCM12_009 | SCM-012 | NULL | Escalation event not raised when delay spans a carrier handoff |
| DEF-SCM13-001 | UT_SCM13_005 | SCM-013 | NULL | Notification omits prior score for comparison in change summary |
| DEF-SCM13-002 | UT_SCM13_009 | SCM-013 | NULL | Corrective action plan workflow does not trigger for suppliers with missing cost metric |
| DEF-SCM14-001 | UT_SCM14_005 | SCM-014 | NULL | Notification fails to include picker ID for multi-picker orders |
| DEF-SCM14-002 | UT_SCM14_009 | SCM-014 | NULL | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order |
| DEF-SCM15-001 | UT_SCM15_005 | SCM-015 | NULL | Notification template renders incorrect item SKU for bundled returns |
| DEF-SCM15-002 | UT_SCM15_009 | SCM-015 | NULL | QC inspection workflow fails to trigger for multi-item returns totaling above $500 |
| DEF-SCM16-001 | UT_SCM16_005 | SCM-016 | NULL | Notification content shows stale forecast value from prior run |
| DEF-SCM16-002 | UT_SCM16_009 | SCM-016 | NULL | Planner review workflow does not trigger when variance calculation crosses a category re-mapping |
| DEF-SCM17-001 | UT_SCM17_005 | SCM-017 | NULL | Notification omits PO number when invoice references multiple line items |
| DEF-SCM17-002 | UT_SCM17_009 | SCM-017 | NULL | Manager review workflow fails to trigger when discrepancy results from a currency conversion rounding difference |
| DEF-SCM18-001 | UT_SCM18_005 | SCM-018 | NULL | Notification fails to send when SKU has an associated substitute item mapping |
| DEF-SCM18-002 | UT_SCM18_009 | SCM-018 | NULL | Escalation workflow does not trigger when backorder is partially fulfilled before day 14 |
| DEF-SCM19-001 | UT_SCM19_005 | SCM-019 | NULL | Notification fails to identify destination warehouse manager when transfer spans regions |
| DEF-SCM19-002 | UT_SCM19_009 | SCM-019 | NULL | Regional manager approval workflow not triggered when transfer is split across multiple shipments |

# Conclusion

Overall unit test coverage is substantial but not fully compliant for release confidence because 23.00 acceptance criteria are only partially covered, 2.00 planned tests lack execution evidence, and 32.00 defects were identified across the reviewed scope. Remediation should prioritize closing missing business-obligation gaps in approval, audit, review, and notification criteria, correcting ambiguous execution records, and resolving all workflow and notification defects before sign-off.
