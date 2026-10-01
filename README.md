# `guardian/actions-ecr`

A set of ([composite](https://docs.github.com/en/actions/tutorials/create-actions/create-a-composite-action)) GitHub Actions to interact with AWS ECR. 
Functionality includes:
- [Pushing a container image](push/README.md)

## Releasing
Automatic releases are handled by Changesets. Please see [here](https://github.com/changesets/changesets) for more information.

### Release Automatically
Run `npm run release` to generate a changeset. 

You will be prompted to select the type of release (major, minor, patch) and provide a description of the changes. This in turn will create a new changeset file in the `.changeset` directory with the release type and the description.

Add this file to your PR and after it's merged it will create a new "Release" PR which can be merged by a maintainer to release your changes.

### Do not Release Automatically
If you don't want to create a new release, you can run `npm run release -- --empty` to create an empty changeset.
