# pre-commit-version

A [pre-commit](https://pre-commit.com/) hook for enforcing that a specific file has been updated within the current branch.

By convention, many projects keep a version and/or changelog file.  I created
this hook so that I don't forget to update those files at least once within a
branch before creating pull requests.

This repo defines two hooks:

## check-version-change

Checks for a commit that changes a file named `VERSION` in the root of the repository.

## check-changelog-change

Checks for a commit that changes a file named `CHANGELOG.md` in the root of the repository.


Other files could be checked by overriding the args.  The `check_file_change`
script takes checked file as its first argument.


## Usage

```
- repo: https://github.com/speshak/pre-commit-versions.git
  rev: master
  hooks:
    - id: check-version-change
    - id: check-changelog-change
```
