## Documentation

- Add/update the doc comments in any scripts or commands you create/update
- When creating/updating a script, run the script with `--help` and add/update the script's help text to the repo's README.md. If the script's help text incorrectly references the script's name as `main`, change it to the script's name.

## About Nushell

- To test nushell commands/scripts, use `dev-sandbox-nu.sh` when possible. E.g. `dev-sandbox-nu.sh ls`
  - The command runs nushell in a docker container with the working directory mounted at `/workdir`
- To find how to use a command, run: `dev-sandbox-nu.sh -c 'help <command>'` E.g. `dev-sandbox-nu.sh -c 'help str join'`

## VCS Operations
As soon as the user asks you to make a change, you should succintly summarize the change you are about to make. Then, before you start writing the code, you MUST create a new change in `jj` using `jj new -m "<summary of the change>"`.

However, you should inspect the repo state before doing this with `jj status`. If the current change (`@`) is both empty AND has no description, you should create the change on the parent instead (e.g. `jj new -m "..." @-`).

ALWAYS DO THIS, even when the user asks you to tweak/refine a change you just made. This allows easy rollback of design/code tweaks.
