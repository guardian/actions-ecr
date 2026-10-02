---
"actions-ecr": major
---

Rename `guardian/actions-ecr` to `guardian/actions-ecr/push`.

Please update your GitHub workflows:

```yaml
# Before
- uses: guardian/actions-ecr@v0.0.13
  with:
    roleArn: ${{ secrets.GU_ARTIFACTS_ROLE_ARN }}
    githubToken: ${{ secrets.GITHUB_TOKEN }}

# Now
- uses: guardian/actions-ecr/push@v1.0.0
  with:
    roleArn: ${{ secrets.GU_ARTIFACTS_ROLE_ARN }}
    githubToken: ${{ secrets.GITHUB_TOKEN }}
```