# rp-test

Release flow:

1. `development` → PR to `staging2`
2. Merge to `staging2` → release-please opens a release PR
3. Merge the release PR → tag + GitHub release → PR `staging2` → `staging` (approval, auto-merge)
4. `staging` → PR to `preprod` (approval) → `preprod` → PR to `prod` (approval)

Promotion PR descriptions list the release tags being promoted. Use conventional
commits (`feat:`, `fix:`, …) so release-please can version releases.

Merge promotion PRs with a merge commit (not squash) so release tags stay
reachable from every downstream branch. a
