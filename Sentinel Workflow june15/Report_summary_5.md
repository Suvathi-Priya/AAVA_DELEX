# UNIT TEST QUALITY & COVERAGE REPORT

## Scope

This report evaluates unit test coverage and quality across 8 user stories. The scope is restricted to test plans and execution records mapped to these user stories. Analysis excludes non-unit test activities and unrelated defect categories.

**Coverage Boundary:**
- Total number of user stories included in the analysis: 8
- These user stories form the baseline for evaluation
- Scope is limited to unit test coverage and execution records mapped to these user stories

**Inclusions:**
- Unit test cases linked to the identified user stories
- Test execution results (executed, not executed, passed, failed)
- Defect data directly associated with these user stories

**Exclusions:**
- Integration tests, system tests, or performance tests
- User stories not mapped to test cases

## Coverage Gap Details

| User Story ID | AC ID | Coverage Gap Reason | Coverage Status |
|---------------|-------|-------------------|-----------------|
| SCM-003 | AC3 | No testcase explicitly validates viewing next billing cycle changes in the customer portal. | Partially Covered |
| SCM-005 | AC4 | No testcase explicitly validates reminder date capture in renewal reminder logs.; No testcase explicitly validates channel used capture in renewal reminder logs.; No testcase explicitly validates delivery status capture in renewal reminder logs. | Partially Covered |
| SCM-005 | AC5 | No testcase explicitly validates high-value subscription flagging for annual value greater than $10,000.; No testcase explicitly validates sending reminders to both customer and account manager for high-value subscriptions. | Not Covered |
| SCM-006 | AC2 | No testcase explicitly validates adjusted billing amount in downgrade confirmation notification. | Partially Covered |
| SCM-006 | AC4 | No testcase explicitly validates previous plan capture in downgrade audit logs.; No testcase explicitly validates downgraded plan capture in downgrade audit logs.; No testcase explicitly validates effective date capture in downgrade audit logs.; No testcase explicitly validates credit issued capture in downgrade audit logs.; No testcase explicitly validates timestamp capture in downgrade audit logs. | Partially Covered |
| SCM-006 | AC5 | No testcase explicitly validates customer retention review requirement for enterprise-tier plan downgrades. | Partially Covered |

## Consistency Analysis

### Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---------------|------------------|-------------|----------------|-------|---------------|
| UT_SCM1_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_001 | SCM-001 | NULL | High |
| UT_SCM1_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_002 | SCM-001 | NULL | High |
| UT_SCM1_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_003 | SCM-001 | NULL | High |
| UT_SCM1_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_004 | SCM-001 | NULL | High |
| UT_SCM1_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_005 | SCM-001 | NULL | High |
| UT_SCM1_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_006 | SCM-001 | NULL | High |
| UT_SCM1_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_007 | SCM-001 | NULL | High |
| UT_SCM1_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_008 | SCM-001 | NULL | High |
| UT_SCM1_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_009 | SCM-001 | NULL | High |
| UT_SCM1_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_010 | SCM-001 | NULL | High |
| UT_SCM1_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_011 | SCM-001 | NULL | High |
| UT_SCM1_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_012 | SCM-001 | NULL | High |
| UT_SCM1_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_013 | SCM-001 | NULL | High |
| UT_SCM1_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_014 | SCM-001 | NULL | High |
| UT_SCM1_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_015 | SCM-001 | NULL | High |
| TP_SCM_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_001 | SCM-002 | NULL | High |
| TP_SCM_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_002 | SCM-002 | NULL | High |
| TP_SCM_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_003 | SCM-002 | NULL | High |
| TP_SCM_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_004 | SCM-002 | NULL | High |
| TP_SCM_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_005 | SCM-002 | NULL | High |
| TP_SCM_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_006 | SCM-002 | NULL | High |
| TP_SCM_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_007 | SCM-002 | NULL | High |
| TP_SCM_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_008 | SCM-002 | NULL | High |
| TP_SCM_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_009 | SCM-002 | NULL | High |
| TP_SCM_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_010 | SCM-002 | NULL | High |
| TP_SCM_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_011 | SCM-002 | NULL | High |
| TP_SCM_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_012 | SCM-002 | NULL | High |
| TP_SCM_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_013 | SCM-002 | NULL | High |
| TP_SCM_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_014 | SCM-002 | NULL | High |
| TP_SCM_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_015 | SCM-002 | NULL | High |
| TP_SCM3_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_014 | SCM-003 | NULL | Medium |
| TP_SCM3_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_015 | SCM-003 | NULL | Medium |
| TP_SCM4_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_014 | SCM-004 | NULL | High |
| TP_SCM4_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_015 | SCM-004 | NULL | High |
| TP_SCM5_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM5_014 | SCM-005 | NULL | High |
| TP_SCM5_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM5_015 | SCM-005 | NULL | High |
| TP_SCM6_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_015 | SCM-006 | NULL | High |
| TP_SCM7_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_001 | SCM-007 | NULL | High |
| TP_SCM7_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_002 | SCM-007 | NULL | High |
| TP_SCM7_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_003 | SCM-007 | NULL | High |
| TP_SCM7_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_004 | SCM-007 | NULL | High |
| TP_SCM7_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_005 | SCM-007 | NULL | High |
| TP_SCM7_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_006 | SCM-007 | NULL | High |
| TP_SCM7_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_007 | SCM-007 | NULL | High |
| TP_SCM7_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_008 | SCM-007 | NULL | High |
| TP_SCM7_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_009 | SCM-007 | NULL | High |
| TP_SCM7_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_010 | SCM-007 | NULL | High |
| TP_SCM7_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_011 | SCM-007 | NULL | High |
| TP_SCM7_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_012 | SCM-007 | NULL | High |
| TP_SCM7_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_013 | SCM-007 | NULL | High |
| TP_SCM7_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_014 | SCM-007 | NULL | High |
| TP_SCM7_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_015 | SCM-007 | NULL | High |
| UT_SCM_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_001 | SCM-008 | NULL | High |
| UT_SCM_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_002 | SCM-008 | NULL | High |
| UT_SCM_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_003 | SCM-008 | NULL | High |
| UT_SCM_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_004 | SCM-008 | NULL | High |
| UT_SCM_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_005 | SCM-008 | NULL | High |
| UT_SCM_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_006 | SCM-008 | NULL | High |
| UT_SCM_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_007 | SCM-008 | NULL | High |
| UT_SCM_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_008 | SCM-008 | NULL | High |
| UT_SCM_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_009 | SCM-008 | NULL | High |
| UT_SCM_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_010 | SCM-008 | NULL | High |
| UT_SCM_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_011 | SCM-008 | NULL | High |
| UT_SCM_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_012 | SCM-008 | NULL | High |
| UT_SCM_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_013 | SCM-008 | NULL | High |
| UT_SCM_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_014 | SCM-008 | NULL | High |
| UT_SCM_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_015 | SCM-008 | NULL | High |

## Data Mapping Inconsistency Details

| Test Case ID | Consistency Type | Description | User Story ID | AC ID | Impact Level |
|---------------|------------------|-------------|----------------|-------|---------------|
| UT_SCM1_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_001 | SCM-001 | NULL | High |
| UT_SCM1_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_002 | SCM-001 | NULL | High |
| UT_SCM1_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_003 | SCM-001 | NULL | High |
| UT_SCM1_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_004 | SCM-001 | NULL | High |
| UT_SCM1_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_005 | SCM-001 | NULL | High |
| UT_SCM1_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_006 | SCM-001 | NULL | High |
| UT_SCM1_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_007 | SCM-001 | NULL | High |
| UT_SCM1_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_008 | SCM-001 | NULL | High |
| UT_SCM1_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_009 | SCM-001 | NULL | High |
| UT_SCM1_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_010 | SCM-001 | NULL | High |
| UT_SCM1_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_011 | SCM-001 | NULL | High |
| UT_SCM1_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_012 | SCM-001 | NULL | High |
| UT_SCM1_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_013 | SCM-001 | NULL | High |
| UT_SCM1_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_014 | SCM-001 | NULL | High |
| UT_SCM1_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM1_015 | SCM-001 | NULL | High |
| TP_SCM_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_001 | SCM-002 | NULL | High |
| TP_SCM_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_002 | SCM-002 | NULL | High |
| TP_SCM_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_003 | SCM-002 | NULL | High |
| TP_SCM_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_004 | SCM-002 | NULL | High |
| TP_SCM_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_005 | SCM-002 | NULL | High |
| TP_SCM_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_006 | SCM-002 | NULL | High |
| TP_SCM_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_007 | SCM-002 | NULL | High |
| TP_SCM_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_008 | SCM-002 | NULL | High |
| TP_SCM_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_009 | SCM-002 | NULL | High |
| TP_SCM_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_010 | SCM-002 | NULL | High |
| TP_SCM_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_011 | SCM-002 | NULL | High |
| TP_SCM_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_012 | SCM-002 | NULL | High |
| TP_SCM_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_013 | SCM-002 | NULL | High |
| TP_SCM_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_014 | SCM-002 | NULL | High |
| TP_SCM_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM_015 | SCM-002 | NULL | High |
| TP_SCM3_014 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_014 | SCM-003 | NULL | Medium |
| TP_SCM3_015 | missing_testlog | Execution log is missing for testcase ID: TP_SCM3_015 | SCM-003 | NULL | Medium |
| TP_SCM4_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_014 | SCM-004 | NULL | High |
| TP_SCM4_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM4_015 | SCM-004 | NULL | High |
| TP_SCM5_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM5_014 | SCM-005 | NULL | High |
| TP_SCM5_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM5_015 | SCM-005 | NULL | High |
| TP_SCM6_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM6_015 | SCM-006 | NULL | High |
| TP_SCM7_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_001 | SCM-007 | NULL | High |
| TP_SCM7_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_002 | SCM-007 | NULL | High |
| TP_SCM7_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_003 | SCM-007 | NULL | High |
| TP_SCM7_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_004 | SCM-007 | NULL | High |
| TP_SCM7_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_005 | SCM-007 | NULL | High |
| TP_SCM7_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_006 | SCM-007 | NULL | High |
| TP_SCM7_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_007 | SCM-007 | NULL | High |
| TP_SCM7_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_008 | SCM-007 | NULL | High |
| TP_SCM7_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_009 | SCM-007 | NULL | High |
| TP_SCM7_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_010 | SCM-007 | NULL | High |
| TP_SCM7_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_011 | SCM-007 | NULL | High |
| TP_SCM7_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_012 | SCM-007 | NULL | High |
| TP_SCM7_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_013 | SCM-007 | NULL | High |
| TP_SCM7_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_014 | SCM-007 | NULL | High |
| TP_SCM7_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: TP_SCM7_015 | SCM-007 | NULL | High |
| UT_SCM_001 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_001 | SCM-008 | NULL | High |
| UT_SCM_002 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_002 | SCM-008 | NULL | High |
| UT_SCM_003 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_003 | SCM-008 | NULL | High |
| UT_SCM_004 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_004 | SCM-008 | NULL | High |
| UT_SCM_005 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_005 | SCM-008 | NULL | High |
| UT_SCM_006 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_006 | SCM-008 | NULL | High |
| UT_SCM_007 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_007 | SCM-008 | NULL | High |
| UT_SCM_008 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_008 | SCM-008 | NULL | High |
| UT_SCM_009 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_009 | SCM-008 | NULL | High |
| UT_SCM_010 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_010 | SCM-008 | NULL | High |
| UT_SCM_011 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_011 | SCM-008 | NULL | High |
| UT_SCM_012 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_012 | SCM-008 | NULL | High |
| UT_SCM_013 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_013 | SCM-008 | NULL | High |
| UT_SCM_014 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_014 | SCM-008 | NULL | High |
| UT_SCM_015 | missing_testcase | Mapped testcase definition is missing for testcase ID: UT_SCM_015 | SCM-008 | NULL | High |

## Consistency Metrics Summary

| Metric | Count |
|---------|-------|
| Total Test Cases | 55 |
| Total Test Logs | 118 |
| Missing Test Cases | 65 |
| Missing Test Logs | 2 |
| Consistency Status | Mismatch Detected |

## Defect Details

| Defect ID | Test Case ID | User Story ID | Defect Description |
|-----------|--------------|---------------|-------------------|
| DEF-SCM3-101 | TP_SCM3_004 | SCM-003 | Revised billing amount not included in upgrade confirmation notification |
| DEF-SCM3-102 | TP_SCM3_009 | SCM-003 | Manager approval workflow not initiated when price increase equals exactly 50% |
| DEF-SCM4-101 | TP_SCM4_004 | SCM-004 | Applicable refund details not included in cancellation confirmation notification |
| DEF-SCM4-102 | TP_SCM4_009 | SCM-004 | Finance team approval workflow fails for mixed currency outstanding balances |
| DEF-SCM5-103 | TP_SCM5_011 | SCM-005 | System sends reminder even when subscription expiry date is null |
| DEF-SCM5-101 | TP_SCM5_005 | SCM-005 | Renewal amount not populated in 30-day reminder notification for monthly billing plans |
| DEF-SCM5-104 | TP_SCM5_013 | SCM-005 | Boundary condition error: $10,000 subscription flagged as high-value instead of requiring value >$10,000 |
| DEF-SCM5-105 | TP_SCM5_015 | SCM-005 | Reminder log delivery status remains blank when notification channel fails |
| DEF-SCM6-101 | TP_SCM6_005 | SCM-006 | Adjusted billing amount not included in downgrade confirmation notification to customer |
| DEF-SCM6-102 | TP_SCM6_012 | SCM-006 | Audit log not created when downgrade results in zero credit amount |
| DEF-SCM6-103 | TP_SCM6_015 | SCM-006 | Enterprise downgrade not held pending state; processed immediately bypassing approval workflow |

## Conclusion

Remediation is required as multiple defects exist and coverage gaps are present across several user stories.