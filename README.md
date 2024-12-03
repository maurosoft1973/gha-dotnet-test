# .NET Test

Uses the .NET CLI `dotnet test` [command](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-test) that utilizes the test runner in the .NET SDK.

## Usage

To use this action in your GitHub repository, you can follow these steps:

```yaml
uses: maurosoft1973/dotnet-test@v2
```

### Inputs

```yaml
with:
  # Provides a way to fully customize the build. See https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-command-line-reference?view=vs-2022#switches for more information.
  buildSwitches: ''
  # Defines the build configuration.
  configuration: 'Release'
  # The name of the folder where the coverage report will be written.
  coverageReportFolderName: 'Coverage'
  # Sets the verbosity level of the command.Allowed values are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic]. The default is quiet.
  level: 'quiet'
  # Optional path to the project(s) file to test. Pass empty to test whole solution. Supports globbing.
  projects: 'test/**/*.csproj'
  # When set, current workspace will be overwritten with the content of the restore cache and NuGet packages will be restored.
  restoreCacheKey: ''
  # The name of the folder where the test results will be written.
  testResultsFolderName: 'TestResults'
```

### Outputs

This action has no outputs.

## Examples

### Test all projects in the test folder

```yaml
- name: Test with Release build
  uses: maurosoft1973/dotnet-test@v2
```

## Contributing to .NET Test

Contributions are welcome! 
Feel free to submit issues, feature requests, or pull requests to help improve this action.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
