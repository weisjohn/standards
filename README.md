# standards

A collection of configuration and documentation for writing code at Alchemy.

## General Guidelines

When working with any language all code should be:

 - readable - code is read more than written, strive for readability
 - commented - explaining the logical / business context helps all maintainers
 - professional - do not use profanity or make disparaging remarks about 3rd parties
 - [modular](http://substack.net/finding_modules) - code should be logically separated into discrete units of functionality

### Formatting

Please utilize the [`.editorconfig`](./.editorconfig) file. If using Atom, please utilize the [atom-editorconfig](https://github.com/sindresorhus/atom-editorconfig) plugin. If using VSCode, please utilize [`editorconfig-vscode`](https://github.com/editorconfig/editorconfig-vscode). Please see [editorconfig.org](http://editorconfig.org/) for more integrations.


## Source Control

All work must be done in a Git repository, with work should be done in [separate branches](http://nvie.com/posts/a-successful-git-branching-model/).

All commits made should be [atomic](https://seesparkbox.com/foundry/atomic_commits_with_git). Commit messages should be [intentional and useful](https://alistapart.com/article/the-art-of-the-commit) and should [reference the issue number](https://help.github.com/articles/closing-issues-using-keywords/) to which they correspond.

For example, suppose issue number `42` asks us to implement a feature to allow users to login to a website. When adding the code that handles that request, (even if other features are missing) and the commit does not close that issue:

```
git commit -m "routes: allow POST against /login; re: #42"
```

This allows anyone reviewing the code (including your future self) to understand the purpose for that code, as they have a link to a larger description of the problem that code solves. This is also especially helpful in understanding the context for a line of code in the past through `git annotate`.



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
