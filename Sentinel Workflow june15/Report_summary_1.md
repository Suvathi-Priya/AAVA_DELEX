# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 6 user stories. The scope is restricted to test plans and execution records mapped to these user stories.

Analysis excludes non-unit test activities and unrelated defect categories. The user stories form the baseline for evaluation, and the scope is limited to unit test coverage and execution records mapped to these user stories.

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|---------------------|-----------------|
| SCM-001 | AC5 | No testcase explicitly validates fraud review requirement for high-value refunds above $1000. | Partially Covered |
| SCM-002 | AC2 | No testcase explicitly validates that resume date is included in pause confirmation notification. | Partially Covered |
| SCM-002 | AC3 | No testcase explicitly validates that scheduled resume date is viewable in the customer portal. | Partially Covered |
| SCM-002 | AC4 | No testcase explicitly validates that pause start date is captured in audit logs. | Partially Covered |
| SCM-003 | AC3 | No testcase explicitly validates that next billing cycle changes are viewable in the customer portal. | Partially Covered |
| SCM-005 | AC1 | No testcase explicitly validates automatic triggering of renewal reminder notifications.; No testcase explicitly validates renewal reminder trigger at 30 days before expiry.; No testcase explicitly validates renewal reminder trigger at 15 days before expiry.; No testcase explicitly validates renewal reminder trigger at 7 days before expiry. | Not Covered |
| SCM-005 | AC2 | No testcase explicitly validates that subscription name is included in renewal reminder notification.; No testcase explicitly validates that expiry date is included in renewal reminder notification.; No testcase explicitly validates that renewal amount is included in renewal reminder notification.; No testcase explicitly validates that direct renewal link is included in renewal reminder notification. | Not Covered |
| SCM-005 | AC3 | No testcase explicitly validates that upcoming renewal schedules are viewable in the customer portal.; No testcase explicitly validates that reminder history is viewable in the customer portal.; No testcase explicitly validates that renewal preferences are viewable in the customer portal. | Not Covered |
| SCM-005 | AC4 | No testcase explicitly validates that customer ID is captured in renewal reminder logs.; No testcase explicitly validates that subscription ID is captured in renewal reminder logs.; No testcase explicitly validates that reminder date is captured in renewal reminder logs.; No testcase explicitly validates that channel used is captured in renewal reminder logs. | Partially Covered |
| SCM-005 | AC5 | No testcase explicitly validates identification of subscriptions with annual value greater than $10,000.; No testcase explicitly validates that reminders are sent to customer for high-value subscriptions.; No testcase explicitly validates that reminders are sent to assigned account manager for high-value subscriptions. | Not Covered |
| SCM-006 | AC2 | No testcase explicitly validates that adjusted billing amount is detailed in downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates that previous plan is captured in downgrade audit logs.; No testcase explicitly validates that downgraded plan is captured in downgrade audit logs.; No testcase explicitly validates that effective date is captured in downgrade audit logs.; No testcase explicitly validates that timestamp is captured in downgrade audit logs. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates that customer retention review is required before processing enterprise-tier downgrade requests. | Partially Covered |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---------------|------------------|-------------|----------------|-------|---------------|
| UT_SCM1_001 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_001 | SCM-001 | NULL | Medium |
| UT_SCM1_002 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_002 | SCM-001 | NULL | Medium |
| UT_SCM1_003 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_003 | SCM-001 | NULL | Medium |
| UT_SCM1_004 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_004 | SCM-001 | NULL | Medium |
| UT_SCM1_005 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_005 | SCM-001 | NULL | Medium |
| UT_SCM1_006 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_006 | SCM-001 | NULL | Medium |
| UT_SCM1_007 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_007 | SCM-001 | NULL | Medium |
| UT_SCM1_008 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_008 | SCM-001 | NULL | Medium |
| UT_SCM1_009 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_009 | SCM-001 | NULL | Medium |
| UT_SCM1_010 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_010 | SCM-001 | NULL | Medium |
| UT_SCM1_011 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_011 | SCM-001 | NULL | Medium |
| UT_SCM1_012 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_012 | SCM-001 | NULL | Medium |
| UT_SCM1_013 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_013 | SCM-001 | NULL | Medium |
| UT_SCM1_014 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_014 | SCM-001 | NULL | Medium |
| UT_SCM1_015 | missing_testlog | Execution log is missing for testcase ID: UT_SCM1_015 | SCM-001 | NULL | Medium |
| TP_SCM_001 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_001 | SCM-002 | NULL | Medium |
| TP_SCM_002 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_002 | SCM-002 | NULL | Medium |
| TP_SCM_003 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_003 | SCM-002 | NULL | Medium |
| TP_SCM_004 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_004 | SCM-002 | NULL | Medium |
| TP_SCM_005 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_005 | SCM-002 | NULL | Medium |
| TP_SCM_006 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_006 | SCM-002 | NULL | Medium |
| TP_SCM_007 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_007 | SCM-002 | NULL | Medium |
| TP_SCM_008 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_008 | SCM-002 | NULL | Medium |
| TP_SCM_009 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_009 | SCM-002 | NULL | Medium |
| TP_SCM_010 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_010 | SCM-002 | NULL | Medium |
| TP_SCM_011 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_011 | SCM-002 | NULL | Medium |
| TP_SCM_012 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_012 | SCM-002 | NULL | Medium |
| TP_SCM_013 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_013 | SCM-002 | NULL | Medium |
| TP_SCM_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_014 | SCM-002 | NULL | Medium |
| TP_SCM_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM_015 | SCM-002 | NULL | Medium |
| TP_SCM3_001 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_001 | SCM-003 | NULL | Medium |
| TP_SCM3_002 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_002 | SCM-003 | NULL | Medium |
| TP_SCM3_003 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_003 | SCM-003 | NULL | Medium |
| TP_SCM3_004 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_004 | SCM-003 | NULL | Medium |
| TP_SCM3_005 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_005 | SCM-003 | NULL | Medium |
| TP_SCM3_006 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_006 | SCM-003 | NULL | Medium |
| TP_SCM3_007 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_007 | SCM-003 | NULL | Medium |
| TP_SCM3_008 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_008 | SCM-003 | NULL | Medium |
| TP_SCM3_009 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_009 | SCM-003 | NULL | Medium |
| TP_SCM3_010 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_010 | SCM-003 | NULL | Medium |
| TP_SCM3_011 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_011 | SCM-003 | NULL | Medium |
| TP_SCM3_012 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_012 | SCM-003 | NULL | Medium |
| TP_SCM3_013 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_013 | SCM-003 | NULL | Medium |
| TP_SCM3_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_014 | SCM-003 | NULL | Medium |
| TP_SCM3_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_015 | SCM-003 | NULL | Medium |
| TP_SCM4_001 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_001 | SCM-004 | NULL | Medium |
| TP_SCM4_002 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_002 | SCM-004 | NULL | Medium |
| TP_SCM4_003 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_003 | SCM-004 | NULL | Medium |
| TP_SCM4_004 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_004 | SCM-004 | NULL | Medium |
| TP_SCM4_005 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_005 | SCM-004 | NULL | Medium |
| TP_SCM4_006 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_006 | SCM-004 | NULL | Medium |
| TP_SCM4_007 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_007 | SCM-004 | NULL | Medium |
| TP_SCM4_008 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_008 | SCM-004 | NULL | Medium |
| TP_SCM4_009 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_009 | SCM-004 | NULL | Medium |
| TP_SCM4_010 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_010 | SCM-004 | NULL | Medium |
| TP_SCM4_011 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_011 | SCM-004 | NULL | Medium |
| TP_SCM4_012 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_012 | SCM-004 | NULL | Medium |
| TP_SCM4_013 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_013 | SCM-004 | NULL | Medium |
| TP_SCM4_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_014 | SCM-004 | NULL | Medium |
| TP_SCM4_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM4_015 | SCM-004 | NULL | Medium |
| TP_SCM5_012 | missing_testlog | Execution log is missing for testcase ID: TP_SCM5_012 | SCM-005 | NULL | Medium |
| TP_SCM5_013 | missing_testlog | Execution log is missing for testcase ID: TP_SCM5_013 | SCM-005 | NULL | Medium |
| TP_SCM5_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM5_014 | SCM-005 | NULL | Medium |
| TP_SCM5_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM5_015 | SCM-005 | NULL | Medium |
| TP_SCM6_001 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_001 | SCM-006 | NULL | Medium |
| TP_SCM6_002 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_002 | SCM-006 | NULL | Medium |
| TP_SCM6_003 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_003 | SCM-006 | NULL | Medium |
| TP_SCM6_004 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_004 | SCM-006 | NULL | Medium |
| TP_SCM6_005 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_005 | SCM-006 | NULL | Medium |
| TP_SCM6_006 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_006 | SCM-006 | NULL | Medium |
| TP_SCM6_007 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_007 | SCM-006 | NULL | Medium |
| TP_SCM6_008 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_008 | SCM-006 | NULL | Medium |
| TP_SCM6_009 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_009 | SCM-006 | NULL | Medium |
| TP_SCM6_010 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_010 | SCM-006 | NULL | Medium |
| TP_SCM6_011 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_011 | SCM-006 | NULL | Medium |
| TP_SCM6_012 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_012 | SCM-006 | NULL | Medium |
| TP_SCM6_013 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_013 | SCM-006 | NULL | Medium |
| TP_SCM6_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_014 | SCM-006 | NULL | Medium |
| TP_SCM6_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM6_015 | SCM-006 | NULL | Medium |

## Consistency Metrics Summary

| Metric | Count |
|---------|-------|
| Total Test Cases | 79 |
| Total Test Logs | 0 |
| Missing Test Cases | 0 |
| Missing Test Logs | 79 |
| Consistency Status | Mismatch Detected |

## Defect Details

No defects reported for this User Story.

## Conclusion

Remediation is required as multiple user stories have coverage gaps and all test execution logs are missing.
