# setup-taplo

Setup [Taplo](https://taplo.tamasfe.dev/) in GitHub Actions.

## Usage

```yaml
- uses: uncenter/setup-taplo@v1.0.3
  with:
    version: "0.8.1"
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

      - uses: uncenter/setup-taplo@v1.0.3
        with:
          version: "0.8.1"

      - run: taplo fmt foo.toml --check
```

## License

[MIT](LICENSE)
