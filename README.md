# IoT.js Modules

## Introduction

IoT.js Modules is a collection of packages which works with [IoT.js](https://github.com/Samsung/iotjs), its mother project. The purpose of this "central community repository" is to provide a place everyone can freely share and borrow the packages. It includes not only IoT.js compatible modules but also tools and demo projects which can get inspiration from.

## Ground rules
As of now, we set out to use git submodule to avoid raw duplication of each package. Tracking history and its integrity are guaranteed by git. The minimum requirements for the package are as follows:
- Basically, each package should be given as a standalone gitmodule and be added as a submodule of this repository.
- Each package should contain a descriptor, `package.json`, which includes `name`, `version` and `iotjs`.
- Each package should not use IoT.js core module names such as `fs`, `http`, `console`, and so on. It's encouraged to align with the conventions of `Node.JS` as much as possible.
- It's required to put a line at the end of your commit message which certifies who is the author. It aims to improve tracking of who did what, especially with patches. You should use your real name and email address in the format below:

```
IoT.js-Modules-DCO-1.0-Signed-off-by: Random Developer random@developer.example.org
```
- Other rules unmentioned follow [IoT.js Developer's Guide](https://github.com/Samsung/iotjs/wiki/Developer's-Guide) — e.g., One commit per one pull request, Commit message convention and so on.

## Examples
### Adding a custom property for IoT.js to `package.json`.
```js
// package.json
{
  "name": "", // all lowercase. one word, no spaces. dashes and underscores allowed.
  "version": "", // in the form of x.x.x.

  .....

  "iotjs": {
    "version": ">=1.0"
  }

  .....
}
```
For further information, please refer to [package.json](https://docs.npmjs.com/files/package.json).

### Adding a submodule
```
git submodule add https://github.com/{org}/{project}
git commit -sam 'Import {module} to iotjs modules'
```

## License
IoT.js Modules is Open Source software under the [Apache 2.0 license](LICENSE). Respectively imported modules are under compatible licenses, as long as they are allowing to be imported as git modules.
