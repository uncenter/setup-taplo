# setup-taplo

```yaml
on:
  push:

jobs:
  check:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: uncenter/setup-taplo@v1
        with:
          version: "0.8.1"

      - run: taplo fmt foo.toml --check
        shell: bash
```
