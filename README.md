# Shared governance demo 🌱

**Version 1** · Example policy, not real organisational governance.

One shared Git repository, reused by applications as a **pinned submodule**.
The app chooses a particular commit; edits here do not silently change its policy.

## Example rules

1. Keep secrets out of source control.
2. Explain changes in a pull request.
3. Run the project checks before merging.

## Change process

Change this repo → review and commit → publish/tag the version → propose an
update to each consuming app's submodule pointer → review and commit there.

A Git tag is a convenient human label. The app ultimately records a commit ID,
not a tag name or a moving branch. Do not move released tags.

## Demo tags

- `policy-v1`: the original rules; the app starts pinned here.
- `policy-v2`: adds a short review checklist; available but not automatically adopted.

In a real organisation, protect this repository's main branch and require owners
to review policy changes. Keep enforcement in CI as well as readable policy docs.
