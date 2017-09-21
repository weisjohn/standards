# standards

A collection of configuration and documentation for writing code at Alchemy.

## General Guidelines

When working with any language all code and commit messages should be:

 - readable - code is read more than written, strive for readability
 - commented - explaining the logical / business context helps all maintainers
 - professional - do not use profanity or make disparaging remarks about 3rd parties
 - [atomic](https://seesparkbox.com/foundry/atomic_commits_with_git) - code should be added and located in a logically organized fashion

### Formatting

Please utilize the [`.editorconfig`](./.editorconfig) file. If using Atom, please utilize the [atom-editorconfig](https://github.com/sindresorhus/atom-editorconfig) plugin. If using VSCode, please utilize [`editorconfig-vscode`](https://github.com/editorconfig/editorconfig-vscode). Please see [editorconfig.org](http://editorconfig.org/) for more integrations.


## Languages

### JavaScript

#### Syntax and Formatting

All code should conform to our [`eslint`](https://eslint.org/) configuration found in [`.eslintrc`](./.eslintrc). Additionally, all code should be formatted with [`prettier`](https://prettier.io/).

To use these tools in your project, install them as devDependencies via:

```
npm i -D eslint babel-eslint
```

#### Editors

Modern editors such as [Atom](https://atom.io/) and [VSCode](https://code.visualstudio.com/) provide integrations for both syntax highlighting and linting and formatting errors.

If using Atom, please use [`prettier-atom`](https://atom.io/packages/prettier-atom) together with [`prettier-eslint`](https://github.com/prettier/prettier-eslint) integration. Once you have installed `prettier-atom`, please turn on checkboxes for `ESLint Integration` and `Format Files on Save`.

#### Technology Approach

All JavaScript code, including Node.js and React should be written against the most recent ES-next standards. Please refer to the [`javascript`](https://github.com/airbnb/javascript) style guide for guidance on code technique and style. (Where this differs with our `eslint` and `prettier` config, those should prevail.)

For shipping assets to the browser, tools such as [`webpack`](https://webpack.js.org/) and [`babel`](https://github.com/babel/babel-preset-env) ought to be used. Legacy tools, such as `grunt`, `gulp`, etc. are discouraged.
