# dotnet-version

[![Test .NET Version](https://github.com/VaclavElias/dotnet-version/actions/workflows/dotnet-version-test.yml/badge.svg)](https://github.com/VaclavElias/dotnet-version/actions/workflows/dotnet-version-test.yml)

Test dotnet version in GitHub Action.

## Purpose

This repository automatically tests the latest .NET version (currently targeting .NET 10.0.x) on Windows to ensure compatibility and availability of new .NET releases.

## GitHub Action Workflow

The workflow runs:
- **Manually** via workflow dispatch

### What it does:

1. **Sets up .NET 10.0.x** using `actions/setup-dotnet@v5`
2. **Verifies installation** with `dotnet --version`
3. **Displays comprehensive .NET info** including installed SDKs and runtimes
4. **Creates and runs a test console application** to validate functionality

## Monitoring

Check the [Actions tab](https://github.com/VaclavElias/dotnet-version/actions) to see the latest test results and .NET version information.
