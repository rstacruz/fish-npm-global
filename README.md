# fish-npm-global

> Make user-installed global npm packages work with fish

Ever been frustrated that `npm install -g` just doesn't quite work? This fixes that. A fish plugin to make `yarn global add <pkg>` and `npm install -g <pkg>` work with your Fish shell.

## Install

Using [Fisherman](https://github.com/fisherman/fisherman):

```sh
fisher rstacruz/fish-npm-global
```

## Usage

__With npm:__ You can add global packages via npm using `npm install -g <package>`:

```sh
npm install -g benny-hill
```

__With yarn:__ You can add global packages via Yarn using `yarn global add <packagename>`:

```sh
yarn global add benny-hill
```

You'll now be able to run commands installed by yarn or npm!

```sh
# before: wtf is going on?
$ benny-hill --help
  bash: benny-hill: command not found

# after: hooray!
$ benny-hill --help
```

## Does it only work with fish?

To make your bins work outside of fish, put this into your `~/.profile`:

```sh
export PATH="$HOME/.node_modules/bin:$PATH"
export npm_config_prefix="~/.node_modules"
```

## How it works

See [conf.d/npm-global.fish](conf.d/npm-global.fish).

## Thanks

**fish-npm-global** © 2018, Rico Sta. Cruz. Released under the [MIT] License.<br>
Authored and maintained by Rico Sta. Cruz with help from contributors ([list][contributors]).

> [ricostacruz.com](http://ricostacruz.com) &nbsp;&middot;&nbsp;
> GitHub [@rstacruz](https://github.com/rstacruz) &nbsp;&middot;&nbsp;
> Twitter [@rstacruz](https://twitter.com/rstacruz)

[![](https://img.shields.io/github/followers/rstacruz.svg?style=social&label=@rstacruz)](https://github.com/rstacruz) &nbsp;
[![](https://img.shields.io/twitter/follow/rstacruz.svg?style=social&label=@rstacruz)](https://twitter.com/rstacruz)

[MIT]: http://mit-license.org/
[contributors]: http://github.com/rstacruz/fish-npm-install-g/contributors
