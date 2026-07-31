<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 executed test log entries derived directly from the uploaded user story, test plan, and test log documents.

Document completeness is acceptable for the uploaded set: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs mapped to acceptance criteria and story IDs; each test log contains execution status per test case; no separate defect log documents were uploaded, so defect details were derived from the “Defect Details & Description” field in the execution logs. Overall derived scope shows full testcase-to-acceptance-criteria coverage across all user stories, with execution evidence present for all planned test cases and 20 logged defects/failures affecting AC2 and AC5 across the 10 stories.

# Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-010 | AC5 | Defect observed in approval workflow trigger during execution | Fully Covered |
| SCM-011 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-011 | AC5 | Defect observed in approval routing during execution | Fully Covered |
| SCM-012 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-012 | AC5 | Defect observed in escalation trigger during execution | Fully Covered |
| SCM-013 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-013 | AC5 | Defect observed in corrective action workflow trigger during execution | Fully Covered |
| SCM-014 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-014 | AC5 | Defect observed in recount workflow trigger during execution | Fully Covered |
| SCM-015 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-015 | AC5 | Defect observed in inspection workflow trigger during execution | Fully Covered |
| SCM-016 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-016 | AC5 | Defect observed in planner review workflow trigger during execution | Fully Covered |
| SCM-017 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-017 | AC5 | Defect observed in manager review workflow trigger during execution | Fully Covered |
| SCM-018 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-018 | AC5 | Defect observed in escalation workflow trigger during execution | Fully Covered |
| SCM-019 | AC2 | Defect observed in notification content generation during execution | Fully Covered |
| SCM-019 | AC5 | Defect observed in approval workflow trigger during execution | Fully Covered |

# Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped Acceptance Criteria ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All planned test cases include explicit mapped story ID and acceptance criteria ID in the test plans and corresponding test logs. No ambiguous, missing, or duplicate mappings were identified from the uploaded documents. | NULL | NULL | Low |

# Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All planned test cases include explicit mapped story ID and acceptance criteria ID in the test plans and corresponding test logs. No ambiguous, missing, or duplicate mappings were identified from the uploaded documents. | NULL | NULL | Low |

# Consistency Metrics Summary

| Metric | Count |
|---|---|
| total_testcases | 150 |
| total_testlogs | 150 |
| missing_testcases | 0 |
| missing_testlogs | 0 |
| consistency_status | Consistent |

# Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|---|---|---|---|
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

No separate defect log document was uploaded; the above defect register was derived from execution log defect fields and linked to the corresponding user stories and test cases.

# Conclusion

Unit test coverage is complete and mapping consistency is compliant, but execution quality is not fully acceptable because 20 defects were identified across AC2 and AC5 in all 10 user stories. Remediation should prioritize notification-content defects and approval/escalation workflow trigger defects, followed by defect fix validation and targeted re-execution of the failed unit tests.
