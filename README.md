# agent-ci-dryrun
Disposable end-to-end dry-run of the release automation change pipeline (workflow wiring, branch + PR, review, Actions check)

## Dry-run checklist

- Verify the repository wiring: the 'Dry Run' workflow is registered on the default branch at `.github/workflows/dryrun.yml` and can only be triggered manually.
- Verify the pull request: the README change arrives via the `readme-dryrun-steps` branch as a pull request into the default branch, and it is the only change in that pull request.
- Verify the review and the Actions check: a comment review with one inline note is anchored to a changed README line, and the workflow behaves as expected from the Actions tab.
