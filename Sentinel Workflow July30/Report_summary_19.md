# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 5 user stories identified from the uploaded source set: SCM-010, SCM-011, SCM-012, SCM-013, and SCM-014. Complete user story, test plan, and test log document sets were available for SCM-010 through SCM-013; for SCM-014, only the test log was available, and the user story and test plan documents were missing/unreadable in the provided directory.

Across the readable documents, 4 user stories were fully analyzable with 20 acceptance criteria and 60 planned unit test cases, all of which had corresponding execution log entries, resulting in 60 test logs reviewed. An additional 15 executed test log entries were present for SCM-014, but due to missing source user story and test plan documents, requirement extraction, acceptance criteria validation, and coverage derivation for SCM-014 could not be fully established. Overall derived consistency metrics are: total test cases = 60.00, total test logs = 75.00, missing test cases = 15.00, missing test logs = 0.00, consistency status = Partially Consistent.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC5 | Reason code validation missing; testcase exists for approval trigger and boundary behavior, but no testcase explicitly validates mandatory reason code capture | Partially Covered |
| SCM-011 | AC5 | Budget verification validation missing; testcase exists for approval workflow and threshold behavior, but no testcase explicitly validates budget verification | Partially Covered |
| SCM-012 | AC5 | Root-cause review validation missing; testcase exists for escalation trigger and timing boundary behavior, but no testcase explicitly validates mandatory root-cause review | Partially Covered |
| SCM-013 | AC5 | Quarterly business review validation missing; testcase exists for corrective action trigger and threshold behavior, but no testcase explicitly validates mandatory quarterly business review | Partially Covered |
| SCM-014 | NULL | User story document missing; test plan document missing; acceptance criteria and requirement mapping cannot be derived from uploaded source documents | Not Covered |

## Consistency Analysis
| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped Acceptance Criteria ID | Impact Level |
|---|---|---|---|---|---|
| UT_SCM10_001 to UT_SCM10_015 | Direct | Test cases explicitly map to SCM-010 acceptance criteria AC1-AC5 in test plan and execution log | SCM-010 | AC1-AC5 | Low |
| UT_SCM11_001 to UT_SCM11_015 | Direct | Test cases explicitly map to SCM-011 acceptance criteria AC1-AC5 in test plan and execution log | SCM-011 | AC1-AC5 | Low |
| UT_SCM12_001 to UT_SCM12_015 | Direct | Test cases explicitly map to SCM-012 acceptance criteria AC1-AC5 in test plan and execution log | SCM-012 | AC1-AC5 | Low |
| UT_SCM13_001 to UT_SCM13_015 | Direct | Test cases explicitly map to SCM-013 acceptance criteria AC1-AC5 in test plan and execution log | SCM-013 | AC1-AC5 | Low |
| UT_SCM14_001 to UT_SCM14_015 | Missing Upstream Source Mapping | Test log entries exist for SCM-014, but corresponding user story and test plan documents are not present; mapping to validated acceptance criteria cannot be confirmed from source documents | SCM-014 | NULL | High |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| UT_SCM10_001 to UT_SCM10_015 | Direct | Test cases explicitly map to SCM-010 acceptance criteria AC1-AC5 in test plan and execution log | SCM-010 | AC1-AC5 | Low |
| UT_SCM11_001 to UT_SCM11_015 | Direct | Test cases explicitly map to SCM-011 acceptance criteria AC1-AC5 in test plan and execution log | SCM-011 | AC1-AC5 | Low |
| UT_SCM12_001 to UT_SCM12_015 | Direct | Test cases explicitly map to SCM-012 acceptance criteria AC1-AC5 in test plan and execution log | SCM-012 | AC1-AC5 | Low |
| UT_SCM13_001 to UT_SCM13_015 | Direct | Test cases explicitly map to SCM-013 acceptance criteria AC1-AC5 in test plan and execution log | SCM-013 | AC1-AC5 | Low |
| UT_SCM14_001 to UT_SCM14_015 | Missing Upstream Source Mapping | Test log entries exist for SCM-014, but corresponding user story and test plan documents are not present; mapping to validated acceptance criteria cannot be confirmed from source documents | SCM-014 | NULL | High |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 60.00 |
| Total Test Logs | 75.00 |
| Missing Test Cases | 15.00 |
| Missing Test Logs | 0.00 |
| Consistency Status | Partially Consistent |

## Defect Details
| Defect ID | Test Case ID | User Story ID | Defect Title / Description |
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

No additional defect log documents were provided; defect details above were derived from execution log defect fields only.

## Conclusion
Unit test coverage is largely complete for SCM-010 through SCM-013, but each of those stories contains one partially covered acceptance criterion due to missing validation of an explicit business obligation, and open execution defects remain in AC2 and AC5 areas. SCM-014 is not auditable for requirement coverage until its user story and test plan documents are provided, and remediation should prioritize closing the eight logged defects and adding explicit test cases for the missing obligation checks.
