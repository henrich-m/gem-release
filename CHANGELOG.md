# Changelog

## v2.0.0

This is a major rewrite, 7 years after the initial implementation.

### Major changes

* Consistent config format, using config files, environment variables, and command line options
* Custom template groups for `gem bootstrap`
* Complete help output in `gem [command] --help`
* Consistent behaviour in multi-gem scenarios (see the [README](https://github.com/svenfuchs/gem-release/blob/master/README.md#scenarios))
* Consistent command line option defaults across commands when invoked with a
  shortcut, e.g. `gem bump --release --tag` vs `gem release --tag`
* Colorized, more consistently formatted output
* Parse friendly output on all commands when not on a tty (e.g. `gem bump --pretend --no-commit | awk '{ print $4 }')

### Other changes

* Fix misleading success message when `gem push` fails
* Release and tag now fail if there are uncommitted changes
* Add `--message` and `--skip-ci` to `gem bump` in order to customize the commit message
* Add `--branch` to `gem bump` in order to switch to a new branch
* Add `--sign` to `gem bump` and `gem tag` in order to GPG sign commits and tags
* Add `--no-color` to all commands
* Support version files of gems with an `\*\_rb` suffix
* Add `--bin` to `gem gemspec`, add executables to gemspec
* Add `--bin` to `gem bootstrap`, create executables
