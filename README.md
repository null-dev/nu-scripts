# null-dev/nu-scripts

My personal nushell scripts.

## Scripts

### `repo-cp`

Copy a directory recursively, skipping all gitignored files.

Uses `git ls-files` to enumerate files that are either tracked or untracked
but not ignored. Falls back to a plain recursive copy if the source directory
is not inside a git repository.

```
Usage:
  > repo-cp {flags} <src> <dst>

Flags:
  -h, --help: Display the help message for this command
  -n, --dry-run: Print files that would be copied without actually copying

Parameters:
  src <path>: Source directory to copy from
  dst <path>: Destination directory to copy to
```

Examples:
```sh
repo-cp ./my-project ~/backup/my-project
repo-cp --dry-run ./my-project ~/backup/my-project
```