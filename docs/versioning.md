## Versioning

This repo follows the [semantic versioning](https://semver.org/) and utilizes the 
[semantic-release](https://github.com/semantic-release/semantic-release) package inside GitHub actions to generate 
versioned tags.

These tags are automatically created on commits to the main branch when commit messages contain trigger words defined in
the [semantic release documentation](https://github.com/semantic-release/semantic-release#how-does-it-work). The
[semantic-release](https://github.com/semantic-release/semantic-release) package follows the 
[angular commit message format](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format) for
conventions.

> **NOTE**: Not all commits to main will produce a semvar tag. Commits that do not meet the criteria outlined in the
> commit message conventions will not produce a new tag.

When a commit message contains a trigger word, the following actions are performed:
- A new tag is created
- A new GitHub release is created
- A deployment occurs tagging the container image with the new semver tag
