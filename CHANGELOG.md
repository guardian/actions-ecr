# actions-ecr

## 1.0.1

### Patch Changes

- 3e8ab3f: Correctly observe `githubRepository` input.

## 1.0.0

### Major Changes

- 2b4b0f0: Rename `appName` input to `app`.
- 7a64ea5: Make `appName` a required input.
  
  Previously, `appName` was optional and defaulted to the GitHub repository name.
  Setting `appName` as required makes it explicit which image is being pushed/pulled.
- 51a3cfc: Rename `guardian/actions-ecr` to `guardian/actions-ecr/push`.
  
  Please update your GitHub workflows:
  
  ```yaml
  # Before
  - uses: guardian/actions-publish-image@v0.0.13
    with:
      roleArn: ${{ secrets.GU_ARTIFACTS_ROLE_ARN }}
      githubToken: ${{ secrets.GITHUB_TOKEN }}
  
  # Now
  - uses: guardian/actions-ecr/push@v1.0.0
    with:
      roleArn: ${{ secrets.GU_ARTIFACTS_ROLE_ARN }}
      githubToken: ${{ secrets.GITHUB_TOKEN }}
  ```

### Minor Changes

- 974780d: Add Action to pull image from AWS ECR.

## 0.0.13

### Patch Changes

- 43eb054: Another test release following major version bump of changesets dependencies.

## 0.0.12

### Patch Changes

- 5b1e4fa: Test release following major version bump of changesets dependencies.

## 0.0.11

### Patch Changes

- cb32ffa: Test release following major version bump of changesets dependencies.

## 0.0.10

### Patch Changes

- 7d126ce: Initial release with changesets.
