# ts-init
This repository contains the boilerplate for a TypeScript project.
To set your project up with just one command, add the following script to your `.bashrc` file:
```sh
function tsinit() {
    # Clones the repo
    git clone --depth=1 https://github.com/oathompsonjones/ts-init.git .
    # Remove the git history
    rm -rf ./.git
    # Reinitialises git
    git init
    # Installs the dependencies
    pnpm i
    pnpm update --latest
    # Creates files which git ignores
    touch .env
    mkdir .vscode
    touch .vscode/settings.json
    echo -e "{\n\t\"vitest.commandLine\": \"pnpx vitest watch\"\n}" > .vscode/settings.json
    # Opens the index file in VSCode
    code ./src/index.ts
}
```
To use the function, simply run the command `tsinit` in an empty directory using a fresh bash terminal.