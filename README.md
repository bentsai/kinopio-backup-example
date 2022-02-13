# Kinopio backup

Use this example to automate regular backups of your [Kinopio](https://kinopio.club) spaces.

1. Create a new repository using this repository as a template.
2. Obtain [your Kinopio API key](https://help.kinopio.club/api/).
3. Create a new repository secret (`settings/secrets/actions`) called `KINOPIO_API_KEY` with the value.
4. That *might* be it. The action is set to run every 30 minutes.

## What the action does

- Checks out this repository.
- Uses the Kinopio API to see what new spaces have been created or modified since the last time the action was run.
- Downloads each of these spaces as a JSON file.
- Updates the time in `.config.json` to indicate the action was just run.
- Commits these changes into the repository.

## Notes

- Set your repository to be private since it will contain all of your Kinopio spaces (private and public).
