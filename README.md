# setup-kubectl-action

This GitHub Action installs the `kubectl` CLI tool.

## Usage

To use this action in your GitHub workflows, add a step in your workflow YAML file as shown below:

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Install yq
        uses: tsanghan/setup-kubectl-action@main
        with:
          version: '1.31.1'

      # Add more steps here that require kubectl