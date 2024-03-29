# Check IntelliTect.Coalesce

This GitHub Action ensures that the `coalesce` process has been run in your project.

## Description

The purpose of this action is to verify that the `coalesce` tool has been executed successfully. If any issues are detected, it will fail the workflow.

## Inputs

- `working-directory` (required): The working directory where the `coalesce` process should be run.

## Usage

```yaml
name: Check IntelliTect.Coalesce
description: Make sure coalesce has been run
on:
  push:
    branches:
      - main
jobs:
  check-coalesce:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Ensure Coalesce has been run
        uses: benjaminmichaelis/check-intellitect-coalesce-action@v1
        with:
          working-directory: ./
