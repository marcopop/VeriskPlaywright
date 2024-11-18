# Playwright with .NET

This project brifly sumerize basic setup for Playwright automation with .NET.

## Running tests

### Execute single test:

```bash
dotnet test --filter "PageDisplayedCorrectly"
```

### Execute all tests:

```bash
dotnet test
```

### Execute all tests using Playwright UI:

```bash
dotnet test --settings .\test.runSettings
```

### Execute and debug single test using Playwright UI:

```bash
dotnet test --filter "PageDisplayedCorrectly" --settings .\test.runSettings
```

test
1. HEADED = 1 to launch the Playwright UI in your tests.
2. set PWDEBUG = 1 to open Playwright Inspector automatically.
3. Use the Playwright Inspector to step through and debug tests interactively.

## Parallel Execution

Paralel Execution : 

[Parallelizable(ParallelScope.Fixtures)]: 

This tells NUnit to run all tests in the class in parallel at the fixture level. 

Examples:

- ParallelScope.Self runs the test in parallel with other tests in the same class. 
- ParallelScope.All runs all tests in parallel regardless of fixture.
- ParallelScope.Children allows child tests to run in parallel.
