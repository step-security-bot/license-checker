<div style="display:flex; align-items:center; justify-content:center">
  <img alt="logo" src="./assets/banner-with-border.svg" width="100%" />
</div>

<br />

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-8-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

🕵️ Audit your NPM dependencies and reject any forbidden license.

Check our [wiki](https://github.com/guidesmiths/license-checker/wiki)!

## Description

This package allows you to do a quick audit on your NPM dependencies by adding it in your hooks.

You can optionally add options to exclude generating the report or avoid generating the error report in case a forbidden license is found (see more details [here](#options)).

## How to use it in your project

- Install the package

  ```
  npm install @guidesmiths/license-checker
  ```

- Add a script to run the package

```
npx @guidesmiths/license-checker --failOn license1 license2
```
- If you are using **yarn** you may want to run it from the node modules instead of using npx

```
node_modules/.bin/license-checker --failOn /licenseRegex/
```

- Use the script wherever you want (husky hook, in your CI/CD pipeline, ...)

## <a name="options"></a>Options

| Option                | Description                                                                                                                                                  | Type     | Default                         |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
| --start               | Path of the initial json to look for                                                                                                                         | string   | `process.cwd()`                 |
| --version             | Shows the version of the package                                                                                                                             | string   |                                 |
| --failOn              | Fail (exit with code 1) on the first occurrence of the licenses of the list. If the argument is enclosed in slashes, it will handled like a RegExp           | string[] |                                 |
| --generateOutputOn    | Generates an output file only if any the licenses of the comma-separated list exist (output generated by default)                                            | string   |                                 |
| --outputFileName      | Name of the output file generated                                                                                                                            | string   | `license-report-<timestamp>.md` |
| --errorReportFileName | Name of the file generated when a license in the failOn option is found                                                                                      | string   | `license-error-<timestamp>.md`  |
| --disableErrorReport  | Flag to disable the error report file generation                                                                                                             | boolean  | `false`                         |
| --disableReport       | Flag to disable the report file generation, whether there is an error or not                                                                                 | boolean  | `false`                         |
| --customHeader        | Name of a text file containing the custom header to add at the start of the generated report                                                                 | string   |                                 |
| --checkLicense        | License to be check against SPDX. It is intended to be used as a standalone option, i.e. if it is present, it will not trigger the package licenses scanning | string   |                                 |
| -h, --help            | Shows help                                                                                                                                                   | boolean  |                                 |

## <a name="examples"></a>Examples

### failOn
If the argument is enclosed in slashes, it will be handled like a regular expression where the pattern is the content enclosed.
In the following example, `license1` is the pattern to test:

```sh
npx @guidesmiths/license-checker --failOn /license1/
```

You may combine both string and regex-like arguments. In this example, `license1` will be handled as a RegExp whereas `license2` will be handled as a string:

```sh
npx @guidesmiths/license-checker --failOn /license1/ license2
```


## Useful links

- [Licensing a repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/licensing-a-repository)
- [Choose a license](https://choosealicense.com/appendix/)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/jmtorralvo"><img src="https://avatars.githubusercontent.com/u/6839860?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Jose Manuel Torralvo Moyano</b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/commits?author=jmtorralvo" title="Code">💻</a> <a href="https://github.com/guidesmiths/license-checker/commits?author=jmtorralvo" title="Documentation">📖</a> <a href="#ideas-jmtorralvo" title="Ideas, Planning, & Feedback">🤔</a> <a href="#maintenance-jmtorralvo" title="Maintenance">🚧</a> <a href="https://github.com/guidesmiths/license-checker/pulls?q=is%3Apr+reviewed-by%3Ajmtorralvo" title="Reviewed Pull Requests">👀</a></td>
    <td align="center"><a href="https://github.com/MarioQuiroga32"><img src="https://avatars.githubusercontent.com/u/43605474?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Mario Quiroga</b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/commits?author=MarioQuiroga32" title="Code">💻</a> <a href="https://github.com/guidesmiths/license-checker/commits?author=MarioQuiroga32" title="Documentation">📖</a> <a href="#ideas-MarioQuiroga32" title="Ideas, Planning, & Feedback">🤔</a> <a href="#maintenance-MarioQuiroga32" title="Maintenance">🚧</a> <a href="https://github.com/guidesmiths/license-checker/pulls?q=is%3Apr+reviewed-by%3AMarioQuiroga32" title="Reviewed Pull Requests">👀</a></td>
    <td align="center"><a href="https://github.com/inigomarquinez"><img src="https://avatars.githubusercontent.com/u/25435858?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Íñigo Marquínez</b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/commits?author=inigomarquinez" title="Code">💻</a> <a href="https://github.com/guidesmiths/license-checker/commits?author=inigomarquinez" title="Documentation">📖</a> <a href="#ideas-inigomarquinez" title="Ideas, Planning, & Feedback">🤔</a> <a href="#maintenance-inigomarquinez" title="Maintenance">🚧</a> <a href="https://github.com/guidesmiths/license-checker/pulls?q=is%3Apr+reviewed-by%3Ainigomarquinez" title="Reviewed Pull Requests">👀</a></td>
    <td align="center"><a href="https://github.com/LonelyPrincess"><img src="https://avatars.githubusercontent.com/u/17673317?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Sara Hernández</b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/commits?author=LonelyPrincess" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/dustytrinkets"><img src="https://avatars.githubusercontent.com/u/18383417?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Laura</b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/pulls?q=is%3Apr+reviewed-by%3Adustytrinkets" title="Reviewed Pull Requests">👀</a></td>
    <td align="center"><a href="https://github.com/ardguezsoc"><img src="https://avatars.githubusercontent.com/u/79102959?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Adri Rodríguez </b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/pulls?q=is%3Apr+reviewed-by%3Aardguezsoc" title="Reviewed Pull Requests">👀</a></td>
    <td align="center"><a href="https://github.com/neodmy"><img src="https://avatars.githubusercontent.com/u/36865163?v=4?s=100" width="100px;" alt=""/><br /><sub><b>David Miguel Yusta</b></sub></a><br /><a href="https://github.com/guidesmiths/license-checker/commits?author=neodmy" title="Code">💻</a> <a href="https://github.com/guidesmiths/license-checker/commits?author=neodmy" title="Documentation">📖</a> <a href="#ideas-neodmy" title="Ideas, Planning, & Feedback">🤔</a> <a href="#maintenance-neodmy" title="Maintenance">🚧</a> <a href="https://github.com/guidesmiths/license-checker/pulls?q=is%3Apr+reviewed-by%3Aneodmy" title="Reviewed Pull Requests">👀</a> <a href="https://github.com/guidesmiths/license-checker/commits?author=neodmy" title="Tests">⚠️</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/lcruz45"><img src="https://avatars.githubusercontent.com/u/91122266?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Lucía</b></sub></a><br /><a href="#design-lcruz45" title="Design">🎨</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
