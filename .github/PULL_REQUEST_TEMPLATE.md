## What

<!-- One or two sentences. The commit subject is usually enough. -->

## Task

<!-- Closes American-Tractor-Company/terra-program#NN   (use Refs for cross-repo work) -->
Task: <A-06 | none — this is a bug/chore>

## Evidence

<!-- Required when the task's deliverable is an artifact. A URL that proves it:
     a gs:// path, a run ID, a dashboard link, a signed record. -->
Evidence:

## Checks

- [ ] Branch is `feat/<TASK-ID>-<slug>` (or `fix/<issue#>-<slug>`)
- [ ] Commit carries the `Task:` trailer; signed (`-S`) if this is a safety-critical repo
- [ ] Schema change? version bumped in `terra-schemas` and consumers named below
- [ ] Touches farm data, PII or consent? `data-rights` label applied
- [ ] Touches E-stop, geofence, watchdog or CAN/ISOBUS? `safety-review` label + claim link
- [ ] Docs/runbook updated if behaviour changed

## Risk

<!-- What breaks if this is wrong, and how we would notice. "Nothing, it is a doc change"
     is a fine answer. -->
