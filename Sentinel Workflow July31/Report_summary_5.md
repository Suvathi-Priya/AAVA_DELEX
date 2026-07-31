# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 10 user stories: SCM-001, SCM-010, SCM-011, SCM-012, SCM-013, SCM-014, SCM-015, SCM-016, SCM-017, SCM-018, and SCM-019 were requested in the file list, but only 10 complete user story/test plan/test log sets were available for analysis in the readable tool output: SCM-001 and SCM-010 through SCM-019. Across these 10 user stories, 50 acceptance criteria were identified, 150 planned unit test cases were defined, and 150 test log entries were available, indicating 100.00% test log availability against planned test cases.

All analyzed user stories contained identifiable ID, title, and acceptance criteria. All test plans contained test case IDs with explicit AC mappings, and all test logs contained execution results per test case. No separate defect log documents were provided; therefore, defect details were derived from the defect fields embedded in the test log files. Overall unit test scope includes positive, negative, and edge-case validation for each acceptance criterion, with coverage inferred from mapped test plan content and execution evidence.

## Coverage Gap Details
No structural coverage gaps were identified from the available test plan and log mappings; however, execution failures were observed and are detailed in the Defect Details section.

## Consistency Analysis
| Testcase ID / Group | Consistency Type | Description | Mapped User Story ID | Mapped Acceptance Criteria ID | Impact Level |
|---|---|---|---|---|---|
| SCM-001 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-001 in both plan and log | SCM-001 | AC1-AC5 | Low |
| SCM-010 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-010 in both plan and log | SCM-010 | AC1-AC5 | Low |
| SCM-011 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-011 in both plan and log | SCM-011 | AC1-AC5 | Low |
| SCM-012 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-012 in both plan and log | SCM-012 | AC1-AC5 | Low |
| SCM-013 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-013 in both plan and log | SCM-013 | AC1-AC5 | Low |
| SCM-014 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-014 in both plan and log | SCM-014 | AC1-AC5 | Low |
| SCM-015 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-015 in both plan and log | SCM-015 | AC1-AC5 | Low |
| SCM-016 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-016 in both plan and log | SCM-016 | AC1-AC5 | Low |
| SCM-017 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-017 in both plan and log | SCM-017 | AC1-AC5 | Low |
| SCM-018 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-018 in both plan and log | SCM-018 | AC1-AC5 | Low |
| SCM-019 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-019 in both plan and log | SCM-019 | AC1-AC5 | Low |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| SCM-001 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-001 in both plan and log | SCM-001 | AC1-AC5 | Low |
| SCM-010 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-010 in both plan and log | SCM-010 | AC1-AC5 | Low |
| SCM-011 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-011 in both plan and log | SCM-011 | AC1-AC5 | Low |
| SCM-012 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-012 in both plan and log | SCM-012 | AC1-AC5 | Low |
| SCM-013 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-013 in both plan and log | SCM-013 | AC1-AC5 | Low |
| SCM-014 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-014 in both plan and log | SCM-014 | AC1-AC5 | Low |
| SCM-015 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-015 in both plan and log | SCM-015 | AC1-AC5 | Low |
| SCM-016 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-016 in both plan and log | SCM-016 | AC1-AC5 | Low |
| SCM-017 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-017 in both plan and log | SCM-017 | AC1-AC5 | Low |
| SCM-018 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-018 in both plan and log | SCM-018 | AC1-AC5 | Low |
| SCM-019 test set | Direct | All 15 test cases explicitly map to AC IDs and story ID SCM-019 in both plan and log | SCM-019 | AC1-AC5 | Low |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total test cases | 150 |
| Total test logs | 150 |
| Missing test cases | 0 |
| Missing test logs | 0 |
| Consistency status | Consistent |

## Defect Details
| Defect ID | Test Case ID | User Story ID | Defect Title / Description |
|---|---|---|---|
| DEF-SCM1-001 | UT_SCM1_005 | SCM-001 | Notification template rendering issue |
| DEF-SCM1-002 | UT_SCM1_009 | SCM-001 | Refund workflow synchronization error |
| DEF-SCM10-001 | UT_SCM10_005 | SCM-010 | Alert content template renders incorrect quantity field |
| DEF-SCM10-002 | UT_SCM10_009 | SCM-010 | Approval workflow fails to trigger for bulk adjustments processed in the same batch |
| DEF-SCM11-001 | UT_SCM11_005 | SCM-011 | Notification template does not populate requestor details field |
| DEF-SCM11-002 | UT_SCM11_009 | SCM-011 | Director approval routing fails when requestor and approver are in different cost centers |
| DEF-SCM12-001 | UT_SCM12_005 | SCM-012 | Notification content omits carrier name for multi-leg shipments |
| DEF-SCM12-002 | UT_SCM12_009 | SCM-012 | Escalation event not raised when delay spans a carrier handoff |
| DEF-SCM13-001 | UT_SCM13_005 | SCM-013 | Notification omits prior score for comparison in change summary |
| DEF-SCM13-002 | UT_SCM13_009 | SCM-013 | Corrective action plan workflow does not trigger for suppliers with missing cost metric |
| DEF-SCM14-001 | UT_SCM14_005 | SCM-014 | Notification fails to include picker ID for multi-picker orders |
| DEF-SCM14-002 | UT_SCM14_009 | SCM-014 | Recount workflow does not trigger when discrepancy spans multiple SKUs on the same order |
| DEF-SCM15-001 | UT_SCM15_005 | SCM-015 | Notification template renders incorrect item SKU for bundled returns |
| DEF-SCM15-002 | UT_SCM15_009 | SCM-015 | QC inspection workflow fails to trigger for multi-item returns totaling above $500 |
| DEF-SCM16-001 | UT_SCM16_005 | SCM-016 | Notification content shows stale forecast value from prior run |
| DEF-SCM16-002 | UT_SCM16_009 | SCM-016 | Planner review workflow does not trigger when variance calculation crosses a category re-mapping |
| DEF-SCM17-001 | UT_SCM17_005 | SCM-017 | Notification omits PO number when invoice references multiple line items |
| DEF-SCM17-002 | UT_SCM17_009 | SCM-017 | Manager review workflow fails to trigger when discrepancy results from a currency conversion rounding difference |
| DEF-SCM18-001 | UT_SCM18_005 | SCM-018 | Notification fails to send when SKU has an associated substitute item mapping |
| DEF-SCM18-002 | UT_SCM18_009 | SCM-018 | Escalation workflow does not trigger when backorder is partially fulfilled before day 14 |
| DEF-SCM19-001 | UT_SCM19_005 | SCM-019 | Notification fails to identify destination warehouse manager when transfer spans regions |
| DEF-SCM19-002 | UT_SCM19_009 | SCM-019 | Regional manager approval workflow not triggered when transfer is split across multiple shipments |

## Conclusion
Unit test design and traceability are complete and consistent across the analyzed document set, with 100.00% acceptance criteria coverage and no missing test logs or test cases. Remediation is required for the 22 execution defects concentrated in AC2 notification content/workflow behavior and AC5 approval/escalation workflow conditions before the affected user stories can be considered functionally stable.
