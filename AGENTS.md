## Documentation

- Add/update the doc comments in any scripts or commands you create/update
- When creating/updating a script, run the script with `--help` and add/update the script's help text to the repo's README.md. If the script's help text incorrectly references the script's name as `main`, change it to the script's name.

## About Nushell

- To test nushell commands/scripts, use `dev-sandbox-nu.sh` when possible. E.g. `dev-sandbox-nu.sh ls`
  - The command runs nushell in a docker container with the working directory mounted at `/workdir`
- To find how to use a command, run: `dev-sandbox-nu.sh -c 'help <command>'` E.g. `dev-sandbox-nu.sh -c 'help str join'`
