# Branching strategy

The applied branching strategy is loosely based on `git-flow`.

## Description

### Branch names

We try to enfore meaningful branch names by following this simple pattern

- `master` Holds the most recent released and stable version
- `feature/*` Branches that belong to a certain feature
- `fix/*` Branches that belong to a certain fix
- `release/`
  - `stable/*` Branches with the latest version of a stable release
  - `next/*` Branches with the latest version of a pre-release
- `chore/*` Housekeeping
- `ci/*` Branches for fixing/improving CI

### Pull requests

The `master` and `release/*` branches are protected to prevent pushing there by accident. The preferred way to push to this branches is by using pull requests.

There are typically checks that are running for pull requests that want to push into this branches, which need to pass before they can be merged. This way, only checked code should be able to be pushed into this special branches.

### Automated releases

Our CI is configured to automatically build releases and publish to npm, when changes are pushed to one of this branches

- `master`
- `release/*`

By protecting the branches and running checks before a PR can be merged, we want to make sure that this automatic releases only contain tested code.

## Branching workflow

Let's say you have `master` on version `1.2.3`. Now you are working on this feature in branch `feature/awesome-feature`.

Once you have finished working on this feature, you want to release it. Therefor you create a PR with the target branch `master`.

Once the PR is approved and merged, you feature is automatically released and published to npm, bumping version of `master` to `1.3.0`.

### Fixes for stable releases

If you want to provide a fix for a stable release `release/stable/1.x`, you follow the steps described above, but instead of choosing `master` as the target branch, you choose `release/stable/1.x`.

### Publishing a pre-release

If you want to create a pre-release version with your features and fixes, create a new branch `release/next/<any-name>`. Update `version` by running e.g. `npm version premajor` before pushing the branch the first time, so that you have the desired version.

Pushing the tag with the pre-release version number `v*-*` will trigger creating a pre-release and publishing to npm.
