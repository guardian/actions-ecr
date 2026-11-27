---
"actions-ecr": major
---

### What the change is:
Updates the push action to tag images with `latest`, or `latest-PR-<PR_NUMBER>` for pull requests, and removes the `branch-<BRANCH_NAME>` and `lifecycle-<BRANCH_NAME>-<BUILD_NUMBER>` tags. The PR comment now references latest instead of branch name. Also fixes a type in the dryRun input parameter.

### Why the change was made:
This change was made to avoid tagging images with `branch-main` when a PR is raised from the `main` branch into a feature branch currently behind `main`. It also simplifies the tagging by removing no longer needed tags such as `lifecycle-...`.

### How a consumer should update their code
They should remove any reference to tags that will no longer be supported and instead use the `latest` tag if they want to pull the most recently created image for the `main` branch (or any other default branch). They will also need to change the `dryRyn` parameter to `dryRun`.