# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 6 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Coverage Boundary:** The total number of user stories included in the analysis is 6, forming the baseline for evaluation. The scope is limited to unit test coverage and execution records mapped to these user stories.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|---------------------|-----------------|
| 1850 | AC4 | No testcase explicitly validates reminder date capture in renewal reminder logs.; No testcase explicitly validates channel used capture in renewal reminder logs. | Partially Covered |
| 1850 | AC5 | No testcase explicitly validates that reminders are sent to customers for high-value subscriptions.; No testcase explicitly validates that reminders are sent to assigned account managers for high-value subscriptions. | Partially Covered |
| 1846 | AC3 | No testcase explicitly validates viewing next billing cycle changes in the customer portal. | Partially Covered |
| 1846 | AC5 | No testcase explicitly validates that upgrade is activated after manager approval for price increase greater than 50%. | Partially Covered |
| 1852 | AC2 | No testcase explicitly validates adjusted billing amount inclusion in downgrade confirmation notifications. | Partially Covered |
| 1852 | AC4 | No testcase explicitly validates previous plan capture in downgrade audit logs.; No testcase explicitly validates downgraded plan capture in downgrade audit logs.; No testcase explicitly validates effective date capture in downgrade audit logs.; No testcase explicitly validates timestamp capture in downgrade audit logs. | Partially Covered |
| 1852 | AC5 | No testcase explicitly validates customer retention review requirement for downgrade requests from enterprise-tier plans. | Partially Covered |
| 1848 | AC5 | No testcase explicitly validates that cancellation is processed after finance team approval for outstanding balances greater than $500. | Partially Covered |
| 1844 | AC2 | No testcase explicitly validates resume date inclusion in pause confirmation notifications. | Partially Covered |
| 1844 | AC3 | No testcase explicitly validates viewing scheduled resume date in the customer portal. | Partially Covered |
| 1844 | AC4 | No testcase explicitly validates pause start date capture in pause audit logs. | Partially Covered |
| 1844 | AC5 | No testcase explicitly validates that pause is activated after manager approval for pause requests exceeding 90 days. | Partially Covered |
| 1836 | AC5 | No testcase explicitly validates fraud review requirement for high-value refunds above $1000. | Partially Covered |

## Consistency Analysis

## Data Mapping Inconsistency Details

No data mapping inconsistencies detected.

## Consistency Metrics Summary

| Metric | Count |
|---------|-------|
| Total Test Cases | 0 |
| Total Test Logs | 0 |
| Missing Test Cases | 0 |
| Missing Test Logs | 0 |
| Consistency Status | NULL |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-SCM5-101 | TP_SCM5_005 | 1850 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-105 | TP_SCM5_015 | 1850 | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM5-104 | TP_SCM5_013 | 1850 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-103 | TP_SCM5_011 | 1850 | System sends reminder even when subscription expiry date is null |
| DEF-SCM3-101 | TP_SCM3_004 | 1846 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | 1846 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM6-101 | TP_SCM6_005 | 1852 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | 1852 | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | 1852 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |
| DEF-SCM4-101 | TP_SCM4_004 | 1848 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | 1848 | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM2-101 | TP_SCM2_008 | 1844 | Pause reason not captured consistently |
| DEF-SCM2-102 | TP_SCM2_009 | 1844 | Activation allowed without completed approval |
| DEF-SCM1-002 | TP_SCM1_009 | 1836 | Refund workflow synchronization error |
| DEF-SCM1-001 | TP_SCM1_005 | 1836 | Notification template rendering issue |

## Conclusion

Remediation is required as multiple test cases have failed and defects exist across all user stories. The report indicates outstanding coverage gaps and execution issues that must be addressed before progression.
