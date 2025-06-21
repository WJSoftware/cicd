# Reusable Workflows And Actions for WJSoftware

This repository defines reusable actions and workflows for its repositories.  Feel free to copy any that you like, 
but note that these are not intended for general consumption use.

## Reusable Workflows

+ **npm-test**:  Runs the desired set of tests.
+ **npm-publish**:  Builds, tests and publishes an NPM package.

### npm-test

| Input | Type | Default Value | Description |
| - | - | - | - |
| `node-version` | `number` | `24` | Version of Node to install.[^1] |
| `pwsh` | `boolean` | `true` | Whether to install PowerShell or not. |
| `build-script` | `string` | `build` | The name of the script (as defined in package.json) to execute to have the project built. |
| `test-script` | `string` | `test` | The name of the script (as defined in package.json) to execute to have the project tested. |
| `build` | `boolean` | `true` | Whether to build the project or not. |

All inputs are optional.

### npm-publish

| Input | Type | Default Value | Description |
| - | - | - | - |
| `node-version` | `number` | `24` | Version of Node to install.[^1] |
| `pwsh` | `boolean` | `true` | Whether to install PowerShell or not. |
| `build-script` | `string` | `build` | The name of the script (as defined in package.json) to execute to have the project built. |
| `test-script` | `string` | `test` | The name of the script (as defined in package.json) to execute to have the project tested. |
| `npm-tag` | `string` | `'latest'` | NPM tag to publish the package (e.g., latest, beta, etc.) |
| `dry-run` | `boolean` | `false` | Perform a dry run (true/false) |

[^1]: See [PSModule/Install-PowerShell](https://github.com/PSModule/Install-PowerShell) for details.
