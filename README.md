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
    # Installs the devDependencies
    pnpm add -D @oathompsonjones/eslint-config@latest @oathompsonjones/ts-config@latest @total-typescript/ts-reset@latest @types/jest@latest @types/node@latest eslint@latest jest@latest ts-jest@latest typescript@latest
    # Installs the dependencies
    pnpm add simple-node-utils@latest
    # Opens the index file in VSCode
    code ./src/index.ts
}
```
To use the function, simply run the command `tsinit` in an empty directory using a fresh bash terminal.

#### Packages Included
###### Dev Dependencies
[@oathompsonjones/eslint-config](https://npmjs.org/package/@oathompsonjones/eslint-config)
[@oathompsonjones/ts-config    ](https://npmjs.org/package/@oathompsonjones/ts-config    )
[@total-typescript/ts-reset    ](https://npmjs.org/package/@total-typescript/ts-reset    )
[@types/jest                   ](https://npmjs.org/package/@types/jest                   )
[@types/node                   ](https://npmjs.org/package/@types/node                   )
[eslint                        ](https://npmjs.org/package/eslint                        )
[jest                          ](https://npmjs.org/package/jest                          )
[ts-jest                       ](https://npmjs.org/package/ts-jest                       )
[typescript                    ](https://npmjs.org/package/typescript                    )
###### Dependencies
[simple-node-utils             ](https://npmjs.org/package/simple-node-utils             )

#### Files Generated
```
.
├── src
│   ├── index.ts
│   └── tests
│       └── index.test.ts
├── .eslintrc
├── .gitattributes
├── .gitignore
├── .npmignore
├── jest.config.js
├── LICENSE
├── package.json
├── pnpm-lock.yaml
├── README.md
└── tsconfig.json
```