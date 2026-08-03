<div align="center">

# **UNIT TEST QUALITY & COVERAGE REPORT**

</div>

# Scope

This report covers 10 user stories (SCM-010 through SCM-019), 50 acceptance criteria, 150 planned unit test cases, and 150 executed test log entries derived directly from the uploaded user story, test plan, and test log documents. Document completeness and integrity are acceptable for the provided scope: each user story contains an identifiable ID, title, and acceptance criteria; each test plan contains test case IDs with explicit acceptance-criteria mappings; each test log contains execution status per test case; no separate defect log documents were provided, so defect details were derived from the defect references embedded in the test log files.

Coverage assessment based on the available documents indicates 40 acceptance criteria are Fully Covered, 10 are Partially Covered, and 0 are Not Covered. Mapping consistency is structurally consistent across the uploaded artifacts, with 0 missing test cases and 0 missing test logs; however, several acceptance criteria remain only partially covered due to uncovered obligation elements within the AC text despite existing mapped test cases.

# Test Coverage Summary

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---|---|---|---|
| SCM-010 | AC2 | No testcase explicitly validates reminder is sent at least 7 days prior to renewal date. | Partially Covered |
| SCM-010 | AC4 | No testcase mapped for payment method used capture; no testcase mapped for renewal amount capture; no testcase mapped for timestamp capture. | Partially Covered |
| SCM-011 | AC1 | No testcase explicitly validates customer-initiated cancellation path. | Partially Covered |
| SCM-011 | AC3 | No testcase explicitly validates effective end date display in portal. | Partially Covered |
| SCM-011 | AC5 | No testcase explicitly validates finance team review gating before refund issuance. | Partially Covered |
| SCM-012 | AC4 | No testcase mapped for prorated amount capture in audit log; no testcase mapped for effective date capture in audit log. | Partially Covered |
| SCM-013 | AC3 | No testcase explicitly validates license expiration display in portal. | Partially Covered |
| SCM-014 | AC4 | No testcase explicitly validates approver capture in audit log when applicable. | Partially Covered |
| SCM-015 | AC2 | No testcase explicitly validates reminder timing against specified number of days before expiration. | Partially Covered |
| SCM-016 | AC3 | No testcase explicitly validates total subscription cost display in portal. | Partially Covered |
| SCM-017 | AC4 | No testcase explicitly validates old payment method reference capture in audit log. | Partially Covered |
| SCM-017 | AC5 | No testcase explicitly validates immediate retry execution using the new payment method after update. | Partially Covered |
| SCM-018 | AC3 | No testcase explicitly validates outstanding balance display in portal. | Partially Covered |
| SCM-018 | AC5 | No testcase explicitly validates restoration of full access within the defined SLA. | Partially Covered |
| SCM-019 | AC4 | No testcase explicitly validates old price capture in audit log; no testcase explicitly validates new price capture in audit log. | Partially Covered |

# Consistency Analysis

| Testcase ID | Consistency Type | Description | Mapped User Story ID | Mapped Acceptance Criteria ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All reviewed test cases in the uploaded test plans and test logs contain explicit User Story ID and Acceptance Criteria ID mappings, and execution records align to planned test case IDs. No ambiguous, missing, or duplicate testcase-to-AC mappings were identified from the provided artifacts. | NULL | NULL | Low |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---|---|---|---|---|---|
| NULL | Direct | All reviewed test cases in the uploaded test plans and test logs contain explicit User Story ID and Acceptance Criteria ID mappings, and execution records align to planned test case IDs. No ambiguous, missing, or duplicate testcase-to-AC mappings were identified from the provided artifacts. | NULL | NULL | Low |

## Consistency Metrics Summary

| Metric | Count |
|---|---|
| Total Test Cases | 150 |
| Total Test Logs | 150 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | Consistent |

# Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Title | Defect Description |
|---|---|---|---|---|
| DEF-SCM10-101 | TP_SCM10_005 | SCM-010 | NULL | Reminder notification omits current plan price for annual-billed subscriptions |
| DEF-SCM10-102 | TP_SCM10_012 | SCM-010 | NULL | Subscription remains active state after 3rd failed retry instead of moving to suspended |
| DEF-SCM11-101 | TP_SCM11_013 | SCM-011 | NULL | Prorated refund calculation returns small negative value for last-day-of-cycle cancellations |
| DEF-SCM11-102 | TP_SCM11_014 | SCM-011 | NULL | Duplicate cancellation request accepted when subscription already pending cancellation |
| DEF-SCM12-101 | TP_SCM12_014 | SCM-012 | NULL | Feature access delayed by several minutes for upgrades processed at midnight billing boundary |
| DEF-SCM12-102 | TP_SCM12_015 | SCM-012 | NULL | Prorated charge incorrectly applied at full price when upgrade occurs on last day of billing cycle |
| DEF-SCM13-101 | TP_SCM13_005 | SCM-013 | NULL | Revoking license from team member with no assignment returns generic server error instead of handled message |
| DEF-SCM13-102 | TP_SCM13_012 | SCM-013 | NULL | License pool count briefly shows incorrect total when revoke and reassign occur within same second |
| DEF-SCM14-101 | TP_SCM14_009 | SCM-014 | NULL | Refund reason field truncated to 50 characters in audit log for long free-text reasons |
| DEF-SCM14-102 | TP_SCM14_013 | SCM-014 | NULL | Refund request above threshold processed automatically before finance manager approval recorded |
| DEF-SCM15-101 | TP_SCM15_013 | SCM-015 | NULL | Conversion attempted using expired payment method instead of failing over to downgrade path |
| DEF-SCM15-102 | TP_SCM15_014 | SCM-015 | NULL | Downgrade notification not sent when conversion fails due to invalid (vs missing) payment method |
| DEF-SCM16-101 | TP_SCM16_013 | SCM-016 | NULL | Prorated charge for add-on added on last day of billing cycle rounds up to full month charge |
| DEF-SCM16-102 | TP_SCM16_015 | SCM-016 | NULL | Audit log merges two rapid add-on actions into a single entry, losing the first action |
| DEF-SCM17-101 | TP_SCM17_012 | SCM-017 | NULL | International card format with alphanumeric routing details rejected as invalid |
| DEF-SCM17-102 | TP_SCM17_015 | SCM-017 | NULL | No audit log entry created when payment method update fails midway through processing |
| DEF-SCM18-101 | TP_SCM18_011 | SCM-018 | NULL | Consecutive failure counter does not reset after an intervening successful payment |
| DEF-SCM18-102 | TP_SCM18_014 | SCM-018 | NULL | Suspension audit log omits failed attempts that occurred in a prior billing cycle |
| DEF-SCM19-101 | TP_SCM19_012 | SCM-019 | NULL | Only one of several simultaneous tier price changes is detected and flagged for notification |
| DEF-SCM19-102 | TP_SCM19_015 | SCM-019 | NULL | Downgrade request submitted on effective date boundary is charged a penalty fee in error |

# Conclusion

Unit test execution demonstrates broad structural coverage and consistent testcase-to-log traceability, but quality is not yet fully acceptable because 10 acceptance criteria are only partially covered and 20 defects were identified across the reviewed user stories. Remediation should prioritize closing uncovered obligation gaps in timing, audit-field completeness, portal display completeness, and retry/reinstatement behaviors, followed by defect resolution and targeted regression for the affected ACs.