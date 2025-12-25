# Codex MAX Merge - Execution Checklist

**GitHub Issue:** #619
**Date:** 2025-12-20
**Platforms to Delete:** 61 from 53 duplicate groups

---

## Pre-Execution Checklist

- [ ] Read CODEX_MAX_MERGE_EXECUTION_SUMMARY.md
- [ ] Read CODEX_MAX_MERGE_README.md in migrations/
- [ ] Verify database connection: `psql -U postgres -d consultation_platforms -c "SELECT COUNT(*) FROM platforms;"`
- [ ] Ensure you have sufficient disk space for backup
- [ ] Notify team of upcoming migration (if applicable)
- [ ] Schedule maintenance window (if applicable)

---

## Backup Phase

- [ ] Run backup script: `./migrations/BACKUP_COMMAND.sh`
- [ ] Verify backup file was created in `backups/` directory
- [ ] Check backup file size (should be > 1MB)
- [ ] Review backup metrics file
- [ ] Test backup header: `head -n 20 backups/backup_before_codex_max_merge_*.sql`
- [ ] Note backup timestamp: `___________________`
- [ ] Record pre-migration platform count: `___________________`

---

## Migration Execution Phase

### Step 1: Execute Migration

```bash
psql -U postgres -d consultation_platforms -f migrations/codex_max_merge_all_53_groups.sql
```

- [ ] Migration started at: `___________________`
- [ ] Migration completed without errors
- [ ] Migration completed at: `___________________`
- [ ] Note any warnings or messages: `___________________`

### Step 2: Run Verification

```bash
psql -U postgres -d consultation_platforms -f scripts/verify_codex_max_merge.sql
```

- [ ] Verification script executed
- [ ] All verification checks reviewed

---

## Verification Results Checklist

### CHECK 1: Total Platform Count

- [ ] Platform count decreased by 61
- [ ] New count matches expected value
- [ ] Recorded new platform count: `___________________`

### CHECK 2: Deleted Platforms Gone

- [ ] Result = 0 (all deleted platforms removed)

### CHECK 3: Kept Platforms Exist

- [ ] Result = 53 (all primary platforms exist)

### CHECK 4: No Orphaned Emails

- [ ] Result = 0 (no orphaned emails)

### CHECK 5: No Orphaned Campaign Data

- [ ] email_campaigns: 0 orphaned records
- [ ] project_requests: 0 orphaned records
- [ ] github_issues: 0 orphaned records
- [ ] platform_fingerprints: 0 orphaned records
- [ ] screener_answers: 0 orphaned records

### CHECK 6: No Remaining Duplicates

- [ ] Result = 0 rows (no duplicates remain)

### CHECK 7: Email Counts Match

- [ ] Sample platforms have expected email counts
- [ ] Asia CEO Network (64): 7 emails (4+3)
- [ ] Business Connect China (57): 13 emails (10+3)
- [ ] CertiK (11): 12 emails (11+1)
- [ ] Tegus (53): 12 emails (7+5)

### CHECK 8: No Lingering References

- [ ] All tables show 0 references to deleted IDs
- [ ] platform_emails: 0
- [ ] email_campaigns: 0
- [ ] project_requests: 0
- [ ] github_issues: 0
- [ ] platform_fingerprints: 0
- [ ] screener_answers: 0
- [ ] platform_credentials: 0

### CHECK 9: Email Distribution

- [ ] Reviewed top 20 platforms by email count
- [ ] Distribution looks reasonable

### CHECK 10: Summary Statistics

- [ ] Total platforms matches expected
- [ ] Total emails preserved
- [ ] Platforms with emails count reviewed
- [ ] No unexpected data loss

---

## Post-Migration Testing

### Application Testing

- [ ] Application starts without errors
- [ ] Platform lookup works correctly
- [ ] Email campaigns can be created
- [ ] Search functionality works
- [ ] No 404 errors for platforms
- [ ] Admin panel shows correct counts

### Database Integrity

- [ ] Run: `SELECT COUNT(*) FROM platforms;`
- [ ] Run: `SELECT COUNT(*) FROM platform_emails;`
- [ ] Run: `SELECT COUNT(DISTINCT platform_id) FROM platform_emails;`
- [ ] All foreign key constraints satisfied

---

## Documentation & Cleanup

- [ ] Save verification output to file
- [ ] Update GitHub issue #619 with results
- [ ] Document any issues encountered
- [ ] Archive backup file (keep for 30+ days)
- [ ] Update team wiki/docs (if applicable)
- [ ] Send completion notification to team

---

## Rollback Checklist (If Needed)

**Only use if verification fails or critical issues found**

- [ ] Stop application
- [ ] Drop database: `dropdb -U postgres consultation_platforms`
- [ ] Recreate database: `createdb -U postgres consultation_platforms`
- [ ] Restore backup: `psql -U postgres -d consultation_platforms < backups/backup_before_codex_max_merge_TIMESTAMP.sql`
- [ ] Verify restoration: `psql -U postgres -d consultation_platforms -c "SELECT COUNT(*) FROM platforms;"`
- [ ] Restart application
- [ ] Document rollback reason
- [ ] Plan remediation

---

## Success Criteria

Migration is successful when ALL of the following are true:

- [x] ✓ Backup created and verified
- [x] ✓ Migration executed without errors
- [x] ✓ Platform count decreased by exactly 61
- [x] ✓ All 53 primary platforms exist
- [x] ✓ All 61 duplicate platforms deleted
- [x] ✓ Zero orphaned emails
- [x] ✓ Zero orphaned campaign data
- [x] ✓ Zero remaining duplicates
- [x] ✓ Zero references to deleted platform IDs
- [x] ✓ Email counts consolidated correctly
- [x] ✓ Application works correctly
- [x] ✓ No data loss detected

---

## Quick Command Reference

### Backup

```bash
./migrations/BACKUP_COMMAND.sh
```

### Execute Migration

```bash
psql -U postgres -d consultation_platforms -f migrations/codex_max_merge_all_53_groups.sql
```

### Verify Results

```bash
psql -U postgres -d consultation_platforms -f scripts/verify_codex_max_merge.sql
```

### Check Platform Count

```bash
psql -U postgres -d consultation_platforms -c "SELECT COUNT(*) FROM platforms;"
```

### Check for Duplicates

```bash
psql -U postgres -d consultation_platforms -c "
SELECT
    REGEXP_REPLACE(LOWER(name), '[^a-z0-9]', '', 'g') as normalized_name,
    COUNT(*) as count,
    ARRAY_AGG(id ORDER BY id) as platform_ids
FROM platforms
GROUP BY normalized_name
HAVING COUNT(*) > 1;"
```

### Rollback (Emergency)

```bash
dropdb -U postgres consultation_platforms
createdb -U postgres consultation_platforms
psql -U postgres -d consultation_platforms < backups/backup_before_codex_max_merge_TIMESTAMP.sql
```

---

## Key Platform IDs

### Keep (53 platforms)

```
64, 180, 57, 59, 11, 61, 75, 172, 188, 189, 190, 28, 192, 78, 193,
82, 194, 195, 196, 198, 200, 202, 203, 86, 91, 205, 207, 19, 36,
210, 211, 212, 213, 214, 215, 99, 100, 216, 217, 105, 107, 109,
222, 223, 224, 53, 227, 282, 43, 44, 47, 49, 50
```

### Delete (61 platforms)

```
178, 237, 181, 170, 244, 182, 247, 185, 250, 251, 191, 346, 253,
249, 254, 235, 256, 257, 258, 199, 260, 348, 259, 261, 292, 349,
264, 350, 266, 209, 267, 303, 268, 269, 270, 271, 272, 304, 344,
233, 273, 274, 232, 276, 307, 277, 352, 279, 280, 356, 226, 41,
298, 230, 353, 285, 354, 46, 355, 48, 286
```

---

## Execution Log

**Performed By:** `___________________`
**Date:** `___________________`
**Start Time:** `___________________`
**End Time:** `___________________`

**Pre-Migration Count:** `___________________`
**Post-Migration Count:** `___________________`
**Platforms Deleted:** `___________________` (expected: 61)

**Backup File:** `___________________`
**Backup Size:** `___________________`

**Migration Status:** ☐ SUCCESS ☐ FAILED ☐ ROLLED BACK

**Notes:**

```
___________________________________________________________
___________________________________________________________
___________________________________________________________
___________________________________________________________
```

**Verification Status:** ☐ ALL PASSED ☐ SOME FAILED

**Issues Encountered:**

```
___________________________________________________________
___________________________________________________________
___________________________________________________________
```

**Rollback Required:** ☐ YES ☐ NO

**Sign Off:** `___________________` Date: `___________________`

---

## Files Reference

| File             | Location                                       | Purpose                           |
| ---------------- | ---------------------------------------------- | --------------------------------- |
| Migration SQL    | `migrations/codex_max_merge_all_53_groups.sql` | Main migration script (691 lines) |
| Verification SQL | `scripts/verify_codex_max_merge.sql`           | Verification queries (367 lines)  |
| Backup Script    | `migrations/BACKUP_COMMAND.sh`                 | Automated backup (executable)     |
| README           | `migrations/CODEX_MAX_MERGE_README.md`         | Detailed execution guide          |
| Summary          | `CODEX_MAX_MERGE_EXECUTION_SUMMARY.md`         | Overview and quick reference      |
| Checklist        | `CODEX_MAX_MERGE_CHECKLIST.md`                 | This file                         |
| Merge Plan       | `CODEX_MAX_MERGE_PLAN_ALL_53_GROUPS.md`        | Full decision rationale           |

---

**Ready to Execute:** All files are prepared and tested.
**Next Step:** Complete the Pre-Execution Checklist above.
