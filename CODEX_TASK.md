# Codex handoff

Work in repository `ooonea/spoti.pw` on branch `docs/release-tag-source-note`.

## Goal

Finish and upstream the documentation fix that explains Chroma/spoti.pw v0.50+ release tag semantics.

## Context

Upstream repository: `skopevoj/spoti.pw`.

Relevant upstream work:
- PR #204: `feat: build from patcher`
- Release `v0.50.0` is a real distribution release published on 2026-10-05.
- Starting with v0.50, current Chroma development happens in a private repository.
- The public repository retains the older public source snapshot (0.22.0 / 0.23.0-beta).
- Therefore a public v0.50+ tag identifies the published distribution artifacts and is not a source snapshot of the private v0.50+ code.
- Git comparisons can therefore make v0.50.0 appear older than the public 0.23.0-beta branch even though the release kit itself is newer.
- Supported Spotify base remains 9.1.78 unless upstream explicitly changes it.

## Prepared work

The branch already contains commit:

`bb800c5358f6df4da2abab32e84fef441367b930`

It adds a README note explaining the above.

## Tasks

1. Review the prepared README wording for technical accuracy.
2. Check current upstream PR #204 and whether its head branch moved.
3. Rebase/update this branch if necessary.
4. Keep the patch minimal. Do not alter version numbers and do not move/recreate tags.
5. Confirm README still states Spotify 9.1.78 as the supported base.
6. Delete this `CODEX_TASK.md` file before opening the upstream PR.
7. Open a PR to `skopevoj/spoti.pw`:
   - Prefer base `feat/build-from-patcher` while upstream PR #204 is open.
   - If #204 has merged, target the branch that absorbed it or `main`, as appropriate.
   - Title: `docs: clarify v0.50+ release tag semantics`
   - Include the upstream CLA checkbox.

Do not attempt to "fix" v0.50.0 by retagging it: the private-source/public-distribution split is intentional.
