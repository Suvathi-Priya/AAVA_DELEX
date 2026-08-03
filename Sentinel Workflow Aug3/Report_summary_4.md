<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 10 user stories (SCM-010 to SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 corresponding execution log entries derived directly from the uploaded user story, test plan, and test log documents.

Document completeness is acceptable for the analyzed scope: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs with explicit AC mapping; and each test log contains execution results per test case. No separate defect log documents were provided, therefore defect details were derived from defect references embedded in the test execution logs. Overall coverage is Fully Covered for 50 of 50 acceptance criteria based on testcase presence and mapping, with execution quality risks noted where failed results indicate requirement non-conformance despite mapped coverage.

# Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC4 | Missing explicit testcase for payment method used capture; missing explicit testcase for renewal amount capture | Partially Covered |
| SCM-011 | AC3 | Missing explicit testcase for effective end date visibility | Partially Covered |
| SCM-011 | AC5 | Missing explicit testcase for finance team review before refund issuance | Partially Covered |
| SCM-012 | AC4 | Missing explicit testcase for prorated amount capture; missing explicit testcase for effective date capture | Partially Covered |
| SCM-013 | AC3 | Missing explicit testcase for license expiration visibility | Partially Covered |
| SCM-013 | AC5 | Missing explicit testcase for administrator notification of license limit | Partially Covered |
| SCM-014 | AC4 | Missing explicit testcase for approver capture when applicable | Partially Covered |
| SCM-015 | AC2 | Missing explicit testcase for configured reminder lead-time validation | Partially Covered |
| SCM-016 | AC1 | Missing explicit testcase for add-on selection action | Partially Covered |
| SCM-016 | AC3 | Missing explicit testcase for total subscription cost visibility | Partially Covered |
| SCM-016 | AC5 | Missing explicit testcase for regional-regulation refund exception | Partially Covered |
| SCM-017 | AC4 | Missing explicit testcase for old payment method reference capture | Partially Covered |
| SCM-017 | AC5 | Missing explicit testcase for immediate retry using new payment method | Partially Covered |
| SCM-018 | AC3 | Missing explicit testcase for outstanding balance visibility | Partially Covered |
| SCM-018 | AC5 | Missing explicit testcase for restoration within defined SLA | Partially Covered |
| SCM-019 | AC2 | Missing explicit testcase for minimum 30-day advance notification timing | Partially Covered |
| SCM-019 | AC4 | Missing explicit testcase for old price capture; missing explicit testcase for new price capture | Partially Covered |

# Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All planned testcases include explicit mapping to a single user story and acceptance criterion in the test plan, and the same testcase IDs appear in the execution logs. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| NULL | Missing Mapping | No ambiguous, duplicate, or unmapped testcase-to-AC relationships were identified from the uploaded test plans and logs. | NULL | NULL | Low |

# Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| TP_SCM10_001 to TP_SCM19_015 | Direct | All planned testcases include explicit mapping to a single user story and acceptance criterion in the test plan, and the same testcase IDs appear in the execution logs. | SCM-010 to SCM-019 | AC1 to AC5 | Low |
| NULL | Missing Mapping | No ambiguous, duplicate, or unmapped testcase-to-AC relationships were identified from the uploaded test plans and logs. | NULL | NULL | Low |

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
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

# Conclusion

Unit test documentation and execution traceability are complete and consistent, but quality readiness is constrained by 20 logged defects and multiple partially covered acceptance criteria where explicit validation is missing. Remediation is required to close the identified AC coverage gaps and resolve failed execution defects before the affected user stories can be considered compliant and release-ready.
