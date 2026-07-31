# UNIT TEST QUALITY & COVERAGE REPORT

## Scope
This report covers 9 user stories (SCM-001 to SCM-009), 135 planned unit test cases, and 133 available execution log entries derived directly from the uploaded source documents. Document completeness is partially complete: user story, test plan, and test log files were available for all 9 stories; no separate defect log documents were provided, so defect details were derived from the defect fields embedded in the test execution logs.

All 9 user stories contain identifiable IDs, titles, and acceptance criteria. Test plans contain test case IDs and explicit AC mappings for all reviewed stories. Test logs contain execution results per test case, but SCM-003 and SCM-004 each have 14 execution entries against 15 planned test cases, resulting in 2 missing test logs overall. No unreadable files were identified from the provided tool outputs.

## Coverage Gap Details
| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-001 | AC3 | Negative scenario missing. | Partially Covered |
| SCM-002 | AC2 | Resume date validation missing in testcase mapping. | Partially Covered |
| SCM-002 | AC3 | Scheduled resume date validation missing in testcase mapping. | Partially Covered |
| SCM-003 | AC3 | Next billing cycle changes validation missing in testcase mapping. | Partially Covered |
| SCM-005 | AC4 | Reminder date and channel used not explicitly validated by testcase mapping. | Partially Covered |
| SCM-005 | AC5 | Positive scenario missing for above-$10,000 dual-recipient reminder. | Partially Covered |
| SCM-006 | AC4 | Previous plan, downgraded plan, effective date, and timestamp not explicitly validated by testcase mapping. | Partially Covered |
| SCM-006 | AC5 | Customer retention review validation missing in testcase mapping. | Partially Covered |
| SCM-007 | AC3 | Billing change summary validation missing in testcase mapping. | Partially Covered |
| SCM-007 | AC4 | Subscription ID, transfer date, and timestamp not explicitly validated by testcase mapping. | Partially Covered |
| SCM-008 | AC5 | Fraud review validation missing in testcase mapping; boundary test log Pending. | Partially Covered |

## Consistency Analysis
| Test Case ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase mapped to AC1 but no execution result found in test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase mapped to AC5 but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_014 | Missing Test Log | Planned testcase mapped to AC2 but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase mapped to AC5 but no execution result found in test log. | SCM-004 | AC5 | Medium |
| TP_SCM8_014 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-008 | AC2 | Medium |
| TP_SCM8_015 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-009 | AC5 | Medium |
| TP_SCM8_001 to TP_SCM8_015 | Naming Inconsistency | Test plan uses TP_ prefix while execution log uses UT_ prefix for the same SCM-008 story, reducing direct traceability certainty. | SCM-008 | NULL | Medium |
| All executed cases with status shown as Pass/Passed or Fail/Failed | Format Inconsistency | Execution status values are semantically consistent but not normalized across logs. | SCM-001 to SCM-009 | NULL | Low |

## Data Mapping Inconsistency Details
| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM3_014 | Missing Test Log | Planned testcase mapped to AC1 but no execution result found in test log. | SCM-003 | AC1 | Medium |
| TP_SCM3_015 | Missing Test Log | Planned testcase mapped to AC5 but no execution result found in test log. | SCM-003 | AC5 | Medium |
| TP_SCM4_014 | Missing Test Log | Planned testcase mapped to AC2 but no execution result found in test log. | SCM-004 | AC2 | Medium |
| TP_SCM4_015 | Missing Test Log | Planned testcase mapped to AC5 but no execution result found in test log. | SCM-004 | AC5 | Medium |
| TP_SCM8_014 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-008 | AC2 | Medium |
| TP_SCM8_015 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-008 | AC5 | Medium |
| UT_SCM9_014 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-009 | AC2 | Medium |
| UT_SCM9_015 | Execution Pending | Testcase is mapped, but execution result is Pending rather than completed. | SCM-009 | AC5 | Medium |
| TP_SCM8_001 to TP_SCM8_015 | Naming Inconsistency | Test plan uses TP_ prefix while execution log uses UT_ prefix for the same SCM-008 story, reducing direct traceability certainty. | SCM-008 | NULL | Medium |
| All executed cases with status shown as Pass/Passed or Fail/Failed | Format Inconsistency | Execution status values are semantically consistent but not normalized across logs. | SCM-001 to SCM-009 | NULL | Low |

## Consistency Metrics Summary
| Metric | Count |
|---|---|
| Total Test Cases | 135 |
| Total Test Logs | 133 |
| Missing Test Cases | 0 |
| Missing Test Logs | 2 |
| Pending Test Logs | 4 |
| Consistency Status | Partially Consistent |

## Defect Details
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

## Conclusion
Overall unit test coverage is substantial but not fully complete due to partial AC coverage in multiple stories, 2 missing execution logs, 4 pending edge-case executions, and 24 logged defects affecting notification, approval workflow, audit logging, and boundary-condition behavior. Remediation should prioritize closure of missing/pending executions and correction of AC-level gaps and open defects before considering the test set audit-ready and fully compliant.
