### Just a basic TypeScript project

Includes my default settings and linting for any TypeScript-based project.

##### For installing ESLint & Prettier:
- Authenticate with `npm login --registry=https://npm.pkg.github.com/` using your GitHub username and a personal access token (with the `read:packages` scope) instead of password.
- Standards provided by [@glen-84](https://github.com/glen-84)

##### Notes:
- The repo uses (commitlint)[https://commitlint.js.org/] to force minor consistency across commit messages. However, the settings are set for "applications", not "libraries" (meaning, it doesn't allow the header to include `type (scope):` prefix mentioned in the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)).
  - Pre-commit hook also checks for spelling errors.
- `cspell` stores all new words in a dedicated, custom, file named `custom.dic`. Each new word must be added to this file.
    - VSCode has a plugin to automate this.
    - JetBrains users have to manually add each word to the dictionary (see [IDEA-188338](https://youtrack.jetbrains.com/issue/IDEA-188338)).

##### Shortcuts:
- `npm run format-check` - checks for formatting issues
- `npm run format` - formats all code
- `npm run lint:scripts` - checks for lint errors
- `npm run spell-checks` - checks for spelling errors

##### To update all dependencies at once:
  - `npm install -g npm-check-updates`
  - `ncu -u`
  - `npm update`
  - `npm install`
