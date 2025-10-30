# Node
`Node`, often called `Node.js`, is an open-source, cross-platform, `JavaScript` runtime environment built upon Google's V8 JavaScript engine.

+ [Setup](#setup)
+ [Node Version Manager](#node-version-manager)

## Setup
`Node` can be donwloaded from [https://nodejs.org/en](https://nodejs.org/en) or can also be setup using `NVM (Node Version Manager)`. To confirm `Node` and `NPM (Node Package Manager)` are installed:

```shell
$ node --version
$ npm --version
```

It is recommended to set the `Node` version in the `package.json` file using the `engines` property. This will declare what version the project expects. Package manages like `npm` or `yarn` can then warn (or refuse) to install packages if the `Node` version does not match. This version can also be enforced through the use of the `.nvmrc` file.

```json
"engines": {
  "node": ">=24.11.0"
},
```

## Node Version Manager
`Node Version Manager (NVM)` is a tool used to manage different `Node` versions across different projects. To confirm `NVM` is installed:

```shell
$ nvm --version
```

To install a version of `Node` using `NVM` and then to use the installed version:

```shell
# Replace xx.xx.x with the Node version required to be installed
$ nvm install xx.xx.x
# Use the Node version
$ nvm use
```

Within a project root, a config file named `.nvmrc` can be added which can also set the `Node` version. This helps to enforce the `Node` version being used. The `.nvmrc` file simply contains the `Node` version:

```
24.11.0
```

To apply the `Node` version using `NVM`:

```shell
$ nvm use
```

If the following line is added to the shell config (`.bashrc`, `.zshrc`, etc.), `NVM` will automatically switch Node versions when developers `cd` into a project:

```
[ -f .nvmrc ] && nvm use
```
