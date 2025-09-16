# dotnet-version

[![Test .NET Version](https://github.com/VaclavElias/dotnet-version/actions/workflows/dotnet-version-test.yml/badge.svg)](https://github.com/VaclavElias/dotnet-version/actions/workflows/dotnet-version-test.yml)

Test dotnet version in GitHub Action

## Purpose

This repository automatically tests the latest .NET version (currently targeting .NET 10.0.x) on Windows to ensure compatibility and availability of new .NET releases.

## GitHub Action Workflow

The workflow runs:
- **Automatically** on pushes to main/master branches
- **Automatically** on pull requests to main/master branches  
- **Daily at 6:00 AM UTC** to check for new .NET versions
- **Manually** via workflow dispatch

### What it does:

1. **Sets up .NET 10.0.x** using `actions/setup-dotnet@v4`
2. **Verifies installation** with `dotnet --version`
3. **Displays comprehensive .NET info** including installed SDKs and runtimes
4. **Creates and runs a test console application** to validate functionality

### Example workflow step:

```yaml
- name: Set up .NET 10.0.x
  uses: actions/setup-dotnet@v4
  with:
    dotnet-version: 10.0.x

# Verify the installed .NET SDK version
- name: Verify .NET 10.0.x Installation
  run: dotnet --version
```

## Monitoring

Check the [Actions tab](https://github.com/VaclavElias/dotnet-version/actions) to see the latest test results and .NET version information.
