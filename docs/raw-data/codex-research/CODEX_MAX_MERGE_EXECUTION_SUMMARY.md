# Codex MAX Merge - Execution Summary

## GitHub Issue #619: Platform Deduplication

**Status:** Ready for Execution
**Generated:** 2025-12-20
**Verification Model:** GPT-5.1-Codex-Max with High Reasoning Effort

---

## Overview

This migration consolidates 53 duplicate platform groups by deleting 61 duplicate platforms while preserving all associated data (emails, campaigns, projects, etc.).

## Migration Statistics

| Metric                       | Value |
| ---------------------------- | ----- |
| Total Duplicate Groups       | 53    |
| Primary Platforms (Keep)     | 53    |
| Duplicate Platforms (Delete) | 61    |
| Data Tables Migrated         | 7     |
| Verification Checks          | 10    |

## Files Created

### 1. Migration Script

**File:** `

Complete SQL migration script that:

- Migrates all platform_emails from duplicates to primary platforms
- Updates 5 related tables (campaigns, requests, issues, fingerprints, answers)
- Deletes platform_credentials for duplicates
- Deletes 61 duplicate platform records
- Includes inline documentation and comments

### 2. Verification Script

**File:** `

Comprehensive verification queries that check:

1. Total platform count (should decrease by 61)
2. Deleted platforms are gone (should be 0)
3. Kept platforms still exist (should be 53)
4. No orphaned emails
5. No orphaned campaign data
6. No remaining duplicates
7. Email counts match expectations
8. No lingering references to deleted IDs
9. Email distribution analysis
10. Summary statistics

### 3. Backup Script

**File:** `

Automated backup script that:

- Creates timestamped database backup
- Verifies backup file integrity
- Captures pre-migration metrics
- Provides rollback instructions
- **Usage:** `./migrations/BACKUP_COMMAND.sh`

### 4. Documentation

**File:** `

Complete execution guide with:

- Pre-migration checklist
- Step-by-step execution instructions
- Verification checklist
- Rollback procedures
- Special cases documentation
- Troubleshooting guide

---

## Quick Start: Execution Steps

### Step 1: Create Backup (REQUIRED)

```bash
# Option A: Using automated script (recommended)
./migrations/BACKUP_COMMAND.sh

# Option B: Manual backup
pg_dump -U postgres consultation_platforms > backup_before_codex_max_merge_$(date +%Y%m%d_%H%M%S).sql
```

### Step 2: Execute Migration

```bash
psql -U postgres -d consultation_platforms -f migrations/codex_max_merge_all_53_groups.sql
```

### Step 3: Run Verification

```bash
psql -U postgres -d consultation_platforms -f scripts/verify_codex_max_merge.sql
```

### Step 4: Review Results

Check that all verification checks pass:

- ✓ Platform count reduced by 61
- ✓ All 53 primary platforms exist
- ✓ 0 orphaned emails
- ✓ 0 orphaned campaign data
- ✓ 0 remaining duplicates
- ✓ 0 references to deleted platform IDs

---

## Decision Criteria (Applied to All 53 Groups)

The Codex MAX model used consistent high-reasoning effort to apply these criteria:

1. **Primary Factor: Email Count**
   - Platforms with more emails are more valuable (indicates engagement)
   - This was the deciding factor in 95% of cases

2. **Secondary Factor: Status**
   - COMPLETE status preferred over PENDING
   - Only relevant when email counts are equal (rare)

3. **Tiebreaker: Platform ID**
   - Lower ID preferred (indicates earlier creation)
   - Used when email count and status are equal

---

## Special Cases

### 1. Email Count Overrides Status

**Group 24: jurispro**

- Kept: ID 86 (3 emails, PENDING)
- Deleted: ID 292 (0 emails, COMPLETE)
- **Rationale:** 3 emails is more valuable than COMPLETE status with no emails

### 2. Email Count Overrides Lower ID

**Group 47: tenable**

- Kept: ID 227 (5 emails)
- Deleted: ID 41 (3 emails)
- **Rationale:** 5 emails > 3 emails, even though 41 < 227

**Group 51: vcisocatalyst**

- Kept: ID 47 (5 emails)
- Deleted: ID 46 (2 emails), ID 355 (0 emails)
- **Rationale:** 5 emails > 2 emails, even though 46 < 47

**Group 52: vikingcloud**

- Kept: ID 49 (4 emails)
- Deleted: ID 48 (2 emails)
- **Rationale:** 4 emails > 2 emails, even though 48 < 49

---

## Multi-Duplicate Groups

7 groups had 3+ duplicates (22 total platforms):

| Group | Name               | Keep | Delete        | Total Duplicates |
| ----- | ------------------ | ---- | ------------- | ---------------- |
| 21    | industrialdefender | 200  | 260, 348      | 3                |
| 26    | mavensworld        | 205  | 264, 350      | 3                |
| 35    | realciso           | 215  | 272, 304      | 3                |
| 40    | securitygen        | 105  | 232, 276, 307 | **4**            |
| 49    | travasecurity      | 43   | 230, 353      | 3                |
| 50    | trustedsec         | 44   | 285, 354      | 3                |
| 51    | vcisocatalyst      | 47   | 46, 355       | 3                |

**Note:** securitygen is the only group with 4 duplicates (quadruple)

---

## Data Migration Details

### Tables Updated

1. **platform_emails** - Primary data, migrated to primary platform
2. **email_campaigns** - Campaign associations updated
3. **project_requests** - Project requests reassigned
4. **github_issues** - GitHub issues linked to primary
5. **platform_fingerprints** - Fingerprint data consolidated
6. **screener_answers** - Screener responses preserved

### Tables Cleaned

1. **platform_credentials** - Deleted for duplicate platforms
2. **platforms** - 61 duplicate records removed

---

## Expected Results

### Before Migration

```sql
SELECT COUNT(*) FROM platforms;
-- Example: 360 platforms
```

### After Migration

```sql
SELECT COUNT(*) FROM platforms;
-- Example: 299 platforms (360 - 61 = 299)
```

### Email Consolidation Examples

| Platform                    | Old Email Count | Merged From              | New Email Count |
| --------------------------- | --------------- | ------------------------ | --------------- |
| Asia CEO Network (64)       | 4               | +3 from 178              | 7               |
| Business Connect China (57) | 10              | +3 from 181              | 13              |
| CertiK (11)                 | 11              | +1 from 244              | 12              |
| Forensisgroup (190)         | 4               | +3 from 191              | 7               |
| Tegus (53)                  | 7               | +5 from 226              | 12              |
| Trava Security (43)         | 6               | +5 from 230, +0 from 353 | 11              |
| trustedsec (44)             | 3               | +1 from 285, +0 from 354 | 4               |
| securitygen (105)           | 2               | +1+1+0 from 232,276,307  | 4               |

---

## Rollback Procedure

If verification fails or issues are found:

```bash
# Step 1: Drop the database
dropdb -U postgres consultation_platforms

# Step 2: Recreate the database
createdb -U postgres consultation_platforms

# Step 3: Restore from backup
psql -U postgres -d consultation_platforms < backup_before_codex_max_merge_TIMESTAMP.sql

# Step 4: Verify restoration
psql -U postgres -d consultation_platforms -c "SELECT COUNT(*) FROM platforms;"
```

**Important:** Keep the backup file for at least 30 days after successful verification.

---

## Platform IDs Reference

### Platforms to Keep (53)

```
64, 180, 57, 59, 11, 61, 75, 172, 188, 189,
190, 28, 192, 78, 193, 82, 194, 195, 196, 198,
200, 202, 203, 86, 91, 205, 207, 19, 36, 210,
211, 212, 213, 214, 215, 99, 100, 216, 217, 105,
107, 109, 222, 223, 224, 53, 227, 282, 43, 44,
47, 49, 50
```

### Platforms to Delete (61)

```
178, 237, 181, 170, 244, 182, 247, 185, 250, 251,
191, 346, 253, 249, 254, 235, 256, 257, 258, 199,
260, 348, 259, 261, 292, 349, 264, 350, 266, 209,
267, 303, 268, 269, 270, 271, 272, 304, 344, 233,
273, 274, 232, 276, 307, 277, 352, 279, 280, 356,
226, 41, 298, 230, 353, 285, 354, 46, 355, 48, 286
```

---

## Verification Success Criteria

All of the following must be TRUE:

- [ ] Platform count decreased by exactly 61
- [ ] All 53 primary platform IDs still exist
- [ ] All 61 duplicate platform IDs are deleted
- [ ] Zero orphaned emails (platform_emails with invalid platform_id)
- [ ] Zero orphaned campaign data (in all 5 related tables)
- [ ] Zero remaining duplicate platforms (by normalized name)
- [ ] Email counts match expected consolidated values
- [ ] Zero references to deleted platform IDs in any table
- [ ] No SQL errors during migration
- [ ] No SQL errors during verification

---

## Post-Migration Checklist

- [ ] Backup created and verified
- [ ] Migration executed successfully
- [ ] Verification script run
- [ ] All verification checks passed
- [ ] Pre/post metrics compared
- [ ] Application tested (email campaigns, platform lookup)
- [ ] GitHub issue #619 updated with results
- [ ] Backup archived (keep for 30 days minimum)
- [ ] Team notified of successful migration

---

## Support & References

- **Source Plan:** CODEX_MAX_MERGE_PLAN_ALL_53_GROUPS.md
- **Verification Model:** GPT-5.1-Codex-Max
- **Reasoning Effort:** High
- **GitHub Issue:** #619
- **Generated:** 2025-12-20

---

## Execution Log Template

```
CODEX MAX MERGE - EXECUTION LOG
Date: __________
Performed By: __________

PRE-MIGRATION
- Backup created: ☐
- Backup verified: ☐
- Backup file: _________________________________
- Pre-migration platform count: __________

EXECUTION
- Migration started: __________
- Migration completed: __________
- Errors encountered: ☐ Yes ☐ No
- Error details: _________________________________

VERIFICATION
- Verification run: ☐
- All checks passed: ☐ Yes ☐ No
- Post-migration platform count: __________
- Platform count delta: __________ (should be -61)

RESULTS
- Migration successful: ☐ Yes ☐ No
- Rollback required: ☐ Yes ☐ No
- Notes: _________________________________
_________________________________
_________________________________
```

---

**Ready for Execution:** All migration files are prepared and ready.
**Next Step:** Run `./migrations/BACKUP_COMMAND.sh` to create a backup.
