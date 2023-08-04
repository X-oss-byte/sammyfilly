repos:
  - repo: https://github.com/sourcery-ai/sourcery
    rev: v1.6.0
    hooks:
      - id: sourcery
        # The best way to use Sourcery in a pre-commit hook:
        # * review only changed lines:
        # * omit the summary
        args: [--diff=git diff HEAD, --no-summary]
To review all changes compared to the main branch:

args: [--diff=git diff main, --no-summary]
If you want Sourcery to automatically apply the suggested changes,add the --fix option:

args: [--diff=git diff HEAD, --fix, --no-summary]
By default, pre-commit executes its hooks in multiple processes in parallel. This can lead to multiple summaries displayed. For this reason, it's recommended to use the --no-summary option in pre-commit hooks.

The --diff option was introduced in version 0.12.11
The --no-summary option was introduced in version 0.13.0
If Sourcery is the first pre-commit hook that you've added to your project, you'll also need to run pre-commit install.

Notes
Initializing the environment for the Sourcery pre-commit hook might take some minutes.
When the Sourcery pre-commit hook runs for the first time, you might be prompted to log in to Sourcery. Run the sourcery login command as described in the CLI docs. For further runs of the Sourcery pre-commit hook, this login step isn't necessary .
