Why the fork. See https://github.com/travissalascox/fkill-cli/pull/1. Mostly just so that I can clone this down locally to whatever workstation I need and run `pnpm install .` and then `pnpm install -g .` on this without having to change the `package.json` file each time. Will definitely delete this if I am able to get a hold of the maintainer, or if they update the `package.json` before I am able to.

> Fabulously kill processes. Cross-platform.

Works on macOS, Linux, and Windows.

## Install

```sh
npm install --global fkill-cli
```

## Usage

```
$ fkill --help

	Usage
		$ fkill [<pid|name|:port> …]

	Options
		--force, -f                  Force kill
		--verbose, -v                Show process arguments
		--silent, -s                 Silently kill and always exit with code 0
		--force-timeout <N>, -t <N>  Force kill processes which didn't exit after N seconds
		--smart-case                 Case-insensitive unless pattern contains uppercase
		--case-sensitive             Force case-sensitive matching

	Examples
		$ fkill 1337
		$ fkill safari
		$ fkill :8080
		$ fkill 1337 safari :8080
		$ fkill

	To kill a port, prefix it with a colon. For example: :8080.

	Run without arguments to use the interactive interface.
	In interactive mode, 🚦n% indicates high CPU usage and 🐏n% indicates high memory usage.
	Supports fuzzy search in the interactive mode.

	The process name is case-insensitive by default.
```

## Interactive UI

Run `fkill` without arguments to launch the interactive UI.

![](screenshot.svg)

## Related

- [fkill](https://github.com/sindresorhus/fkill) - API for this package
- [alfred-fkill](https://github.com/SamVerschueren/alfred-fkill) - Alfred workflow for this package
