# Backbone GitHub Action

## Introduction

This GitHub Action starts a Backbone Consumer API instance including its dependencies.

The inputs are:
- `consumerapi-version` (e.g. `v4.0.0`) must be specified. See [GitHub](https://github.com/nmshd/backbone/releases) for a list of available versions
- `consumerapi-port` (default `5000`)

## Usage

```yaml
name: Run tests

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4
        
      - name: Start Consumer API
        uses: nmshd/start-backbone:v1.0.0
        with:
          consumerapi-version: v4.1.3
```

## License

[MIT](LICENSE)
