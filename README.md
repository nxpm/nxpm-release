oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g nxpm-release
$ nxpm-release COMMAND
running command...
$ nxpm-release (--version)
nxpm-release/0.0.0 darwin-x64 node-v16.13.0
$ nxpm-release --help [COMMAND]
USAGE
  $ nxpm-release COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`nxpm-release hello PERSON`](#nxpm-release-hello-person)
* [`nxpm-release hello world`](#nxpm-release-hello-world)
* [`nxpm-release help [COMMAND]`](#nxpm-release-help-command)
* [`nxpm-release plugins`](#nxpm-release-plugins)
* [`nxpm-release plugins:install PLUGIN...`](#nxpm-release-pluginsinstall-plugin)
* [`nxpm-release plugins:inspect PLUGIN...`](#nxpm-release-pluginsinspect-plugin)
* [`nxpm-release plugins:install PLUGIN...`](#nxpm-release-pluginsinstall-plugin-1)
* [`nxpm-release plugins:link PLUGIN`](#nxpm-release-pluginslink-plugin)
* [`nxpm-release plugins:uninstall PLUGIN...`](#nxpm-release-pluginsuninstall-plugin)
* [`nxpm-release plugins:uninstall PLUGIN...`](#nxpm-release-pluginsuninstall-plugin-1)
* [`nxpm-release plugins:uninstall PLUGIN...`](#nxpm-release-pluginsuninstall-plugin-2)
* [`nxpm-release plugins update`](#nxpm-release-plugins-update)

## `nxpm-release hello PERSON`

Say hello

```
USAGE
  $ nxpm-release hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/nxpm/nxpm-release/blob/v0.0.0/dist/commands/hello/index.ts)_

## `nxpm-release hello world`

Say hello world

```
USAGE
  $ nxpm-release hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `nxpm-release help [COMMAND]`

Display help for nxpm-release.

```
USAGE
  $ nxpm-release help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for nxpm-release.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `nxpm-release plugins`

List installed plugins.

```
USAGE
  $ nxpm-release plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ nxpm-release plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `nxpm-release plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ nxpm-release plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ nxpm-release plugins add

EXAMPLES
  $ nxpm-release plugins:install myplugin 

  $ nxpm-release plugins:install https://github.com/someuser/someplugin

  $ nxpm-release plugins:install someuser/someplugin
```

## `nxpm-release plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ nxpm-release plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ nxpm-release plugins:inspect myplugin
```

## `nxpm-release plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ nxpm-release plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ nxpm-release plugins add

EXAMPLES
  $ nxpm-release plugins:install myplugin 

  $ nxpm-release plugins:install https://github.com/someuser/someplugin

  $ nxpm-release plugins:install someuser/someplugin
```

## `nxpm-release plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ nxpm-release plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.

EXAMPLES
  $ nxpm-release plugins:link myplugin
```

## `nxpm-release plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ nxpm-release plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ nxpm-release plugins unlink
  $ nxpm-release plugins remove
```

## `nxpm-release plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ nxpm-release plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ nxpm-release plugins unlink
  $ nxpm-release plugins remove
```

## `nxpm-release plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ nxpm-release plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ nxpm-release plugins unlink
  $ nxpm-release plugins remove
```

## `nxpm-release plugins update`

Update installed plugins.

```
USAGE
  $ nxpm-release plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
