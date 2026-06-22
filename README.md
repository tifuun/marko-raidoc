# marko-raidoc

This is a fork frostming's
[Marko](https://github.com/frostming/marko)
markdown parser
with augmentations needed for [RAIDOC](https://github.com/tifuun/raidoc).

This is mostly a permanently temporary solution.
I will likely eventually re-write all of raidoc from scratch.

## Changes from upstream

- `Parser.parse` now gets a `monkeypatch_source` attribute
    when `Praser.parse()` is called that points to the `Source`
    object built from the input text

- parsed AST nodes now have a `monkeypatch_source` attribute
    that contains the input lines that created them as a string.

## non-code changes from upstream

- remove github metadata and workflows
- remove changelog
- remove lock/config files of tooling I do not use
- remove docs
- remove precommit hook
- alter README.md

## License

marko-raidoc is released under [MIT License](LICENSE)

