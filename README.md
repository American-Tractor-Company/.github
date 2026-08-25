# `orgs/dot-github` → push this to `American-Tractor-Company/.github`

Everything in this directory is the *content of the org's `.github` repo*, which supplies:

- `profile/README.md` — the org landing page
- `.github/ISSUE_TEMPLATE/`, `.github/PULL_REQUEST_TEMPLATE.md` — defaults inherited by every
  repo that does not define its own
- `.github/workflows/wf-*.yml` — the **reusable workflows** every TERRA repo calls
- `workflow-templates/` — starter workflows offered in the Actions tab of new repos

Push it before any other repo's CI runs, or every `ci.yml` will fail to resolve its
reusable workflow:

```bash
gh repo clone American-Tractor-Company/.github /tmp/dot-github && rsync -a --delete --exclude .git orgs/dot-github/ /tmp/dot-github/ && cd /tmp/dot-github && git add -A && git commit -m "chore: TERRA shared workflows" && git push
```

Changes here affect all 14 repos: two approvals, and bump the pinned tag consumers use
(`uses: American-Tractor-Company/.github/.github/workflows/wf-python-ci.yml@v1`) rather than
moving `v1` under people's feet for anything breaking.
