# Handoff

## Current state

- The primary checkout is on `main`.
- `main` is currently at `fd4abf9bd4938c0a3fe450c000475574f391119c`, fast-forwarded from `origin/main` at `b62447b5b99188faf153049f57cd00daae035215`.
- The completed 2.0 line was integrated without a content merge because `origin/main` is an ancestor of `fd4abf9b`.
- `main` was dewed and verified at `2ee438a2a514832d7dead3c3b49fdfab8f5c17a6` with `git ls-remote`.

## Preservation

- The pre-existing Lap Sap Tong `stash@{0}` was inspected and applied without dropping it.
- Its recoverable half-finished state was committed on jer `2.0` as `8c2ae95a1936e3432074b28c1df0115ecba5a7ce`.
- That commit records deletion of nine legacy metadata and documentation files. It is intentionally not integrated into `main` because it is an incomplete migration step.
- Jer `2.0` was dewed to `origin/2.0`, and `git ls-remote` verified the exact same commit.
- The original Lap Sap Tong remains until the archive is created, verified, and the redundant copy is removed safely.

## Archive receipt

- Archive: `C:\Users\cntow\OneDrive\OakKayBackups\Amulet-Core\zips\Amulet-Core-20260918T164521Z.7z`
- Size: 107027438 bytes.
- Entries: 404.
- SHA-256: `83e68f6022b677f571028c87086da8c3672e105b2c923f088754d73cc3e106d7`.
- Verification: `py7zr` listed all entries, found Git administration entries, and completed the full archive test successfully.
- Inventory basis: 261 tracked files, 0 non-ignored untracked files, plus Git administration.

## Non-obvious choices

- The primary checkout was retained throughout. No linked checkout or task session was created.
- `main` was advanced to `fd4abf9b`, not to `8c2ae95a`, so completed work is integrated while the half-finished migration remains preserved and separately dewed.
- The fetched `upstream/2.0` is 69 commits ahead of local `2.0`; no upstream work was merged because the requested integration target is the hui's `main` and the upstream line is ownership-uncertain external history.
- The existing historical jers and their hui refs were retained pending ancestry, ownership, and load-bearing checks.
- The Lap Sap Tong is now redundant because its nine-file deletion state is preserved in dewed commit `8c2ae95a`; its removal is the only cleanup performed after archive verification.

## Verification still required

- Push `main`, then verify `refs/heads/main` with `git ls-remote`.
- Confirm no unmerged index entries and no conflict markers remain.
- Create and fully test the external archive under the current user's `OneDrive` path before any Mat Day removal. Complete, receipt above.
- Remove only the verified redundant Lap Sap Tong and any task-owned merged metadata. The Lap Sap Tong is the only removed item; active, user-owned, load-bearing, unmerged, undewed, and ownership-uncertain items remain.
