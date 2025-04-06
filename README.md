# git-hooks

Git-hooks scripts

## Description

Divided into catalogs per git-hook (pre-commit, commit-msg, etc.). Each catalog contains a README with description of contents and additional info on hooks

## Git-hooks info

##### commit-msg

- General use: resolve additional info for commit message; (imo should not be used for checks that invalidate commit since the commit registers (?))
- Runs: after user closes file editor for commit message
- Args: ?
- Caveats: ?

##### pre-commit

- General use: commit validation (i.e. linters, build tests, conflicts, etc.)
- Runs: after `git commit` command and before user is prompted for commit message
- Args: you can get a list (one per line) of affected files in commit by reading input
- Caveats:
  - can be !SKIPPED! via `git commit --no-verify`
  - a list of files from input contains files relative to last change, i.e. if commiting a patch set only new changes relative to previous patch set are handed to pre-commit
  - `git rebase` results in 0 (zero) files handed to pre-commit
