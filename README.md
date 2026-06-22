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
- alter pyproject.toml
- use src layout

## Using as a dependency

I will not publish this package to PyPI because it is not
up to production standards.
To use as a pip dependency (e.g. pyproject.toml or requirements.txt),
use the git repo syntax:

```requirements.txt
marko_raidoc@git+https://github.com/tifuun/marko-raidoc
```

`git` must be installed for this to work.
To use additional features and pin at a specific commit (or tag name):

```requirements.txt
marko_raidoc[codehilite]@git+https://github.com/tifuun/marko-raidoc@4e4ebf7c3b813f02530a5af163777e9645a9c789
```

## License

marko-raidoc is released under [MIT License](LICENSE)

