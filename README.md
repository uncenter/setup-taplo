# setup-taplo

Setup [Taplo](https://taplo.tamasfe.dev/) in GitHub Actions.

## Usage

```yaml
- uses: uncenter/setup-taplo@v2
  with:
    version: "0.10.0"
```

## Examples

```yaml
name: Check formatting

on:
  push:

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: uncenter/setup-taplo@v2
        with:
          version: "0.10.0"

      - run: taplo fmt foo.toml --check
```

## Changelog

### v2

**Compatability**: Taplo >= v0.10.0

With v2, this action is updated to supporting installing Taplo v0.10.0. Use `@v1` to install versions prior to this.

### v1

**Compatability**: Taplo < v0.10.0 (Taplo <= v0.9.3)

## License

[MIT](LICENSE)
