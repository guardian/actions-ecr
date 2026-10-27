---
"actions-ecr": patch
---

- Enable retries for GitHub API REST invocations. Retry 3 times before giving up.
- Make sure that the ``actions/github-script@`` action does not fail when a comment fails to post in the PR, but instead logs the error and continues the workflow.


