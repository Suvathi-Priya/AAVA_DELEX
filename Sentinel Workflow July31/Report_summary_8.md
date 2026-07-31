<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 unit test cases, and 150 corresponding unit test execution log entries derived directly from the uploaded user story, test plan, and test log documents. Document completeness and integrity are acceptable for the provided scope: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs mapped to acceptance criteria and story IDs; each test log contains execution results per test case; no separate defect log documents were provided, so defect details were derived from the defect fields embedded in the test execution logs.

User story scope includes inventory stock monitoring, purchase order approvals, shipment tracking, supplier scorecards, pick-pack-ship automation, RMA processing, demand forecasting, vendor invoice reconciliation, backorder management, and multi-warehouse inventory transfer. Across the uploaded test assets, all 50 acceptance criteria are covered by mapped test cases, with no unreadable files identified and no missing test plan or test log among the listed documents.

# Test Coverage Summary

## Coverage Gap Details

Coverage assessment result: 50 of 50 acceptance criteria are Fully Covered (100.00%), 0 are Partially Covered (0.00%), and 0 are Not Covered (0.00%). No structural coverage gaps were identified from the uploaded test plans and logs; however, execution failures exist within covered acceptance criteria and are detailed in the Defect Details section.

# Consistency Analysis

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| ALL TEST CASES (UT_SCM10_001 to UT_SCM19_015) | Direct | All test cases in the uploaded test plans explicitly map to a single acceptance criteria ID and a single story ID, and each execution log entry aligns to the same mapped test case and story. No ambiguous, missing, or duplicate AC/user story mappings were identified. | SCM-010 to SCM-019 | AC1 to AC5 | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| ALL TEST CASES (UT_SCM10_001 to UT_SCM19_015) | Direct | All test cases in the uploaded test plans explicitly map to a single acceptance criteria ID and a single story ID, and each execution log entry aligns to the same mapped test case and story. No ambiguous, missing, or duplicate AC/user story mappings were identified. | SCM-010 to SCM-019 | AC1 to AC5 | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| total test cases | 150 |
| total test logs | 150 |
| missing test cases | 0 |
| missing test logs | 0 |
| consistency status | Consistent |

# Defect Details

| User Story ID | AC ID | Defect ID | Test Case ID | Defect Title / Description |
|---|---|---|---|---|
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

## Defect Details

Defect summary: 20 defects were reported across 10 user stories, with 2 defects per user story. All defects were derived from failed test execution entries in the uploaded test logs; no standalone defect log document was provided.

# Conclusion

Unit test design and traceability are complete and consistent, with 100.00% acceptance criteria coverage and full testcase-to-log reconciliation across the uploaded scope. Remediation is required for the 20 execution defects concentrated in notification content and approval/escalation workflow logic before the impacted acceptance criteria can be considered execution-stable.
