# GitPlayground

repo for playing with git and github

## Test 1

Added new section for test 1.

adding additional text.

## GitVersion

[GitVersion](https://gitversion.net/docs/) is a tool that generates a Semantic Version number based on your Git history.

For a project, you must first setup a dotnet manifest file.

```shell
dotnet new tool-manifest
```

when you run that command it will create a folder in your project called `.config`. In that folder a file is created called dotnet-tools.json.

To install GitVersion for the project you must run:

```shell
dotnet tool install GitVersion.Tool --version 5.*
```

To run Gitversion.

```shell
 dotnet dotnet-gitversion
```

The output will look like the below:

```json
{
  "Major": 0,
  "Minor": 1,
  "Patch": 0,
  "PreReleaseTag": "feat-gitversion.1",
  "PreReleaseTagWithDash": "-feat-gitversion.1",
  "PreReleaseLabel": "feat-gitversion",
  "PreReleaseLabelWithDash": "-feat-gitversion",
  "PreReleaseNumber": 1,
  "WeightedPreReleaseNumber": 1,
  "BuildMetaData": 3,
  "BuildMetaDataPadded": "0003",
  "FullBuildMetaData": "3.Branch.feat-gitversion.Sha.16a45d49fd7a7c8d69e59cd34e73fedbfaa97865",
  "MajorMinorPatch": "0.1.0",
  "SemVer": "0.1.0-feat-gitversion.1",
  "LegacySemVer": "0.1.0-feat-gitversion1",
  "LegacySemVerPadded": "0.1.0-feat-gitversion0001",
  "AssemblySemVer": "0.1.0.0",
  "AssemblySemFileVer": "0.1.0.0",
  "FullSemVer": "0.1.0-feat-gitversion.1+3",
  "InformationalVersion": "0.1.0-feat-gitversion.1+3.Branch.feat-gitversion.Sha.16a45d49fd7a7c8d69e59cd34e73fedbfaa97865",
  "BranchName": "feat/gitversion",
  "EscapedBranchName": "feat-gitversion",
  "Sha": "16a45d49fd7a7c8d69e59cd34e73fedbfaa97865",
  "ShortSha": "16a45d4",
  "NuGetVersionV2": "0.1.0-feat-gitversion0001",
  "NuGetVersion": "0.1.0-feat-gitversion0001",
  "NuGetPreReleaseTagV2": "feat-gitversion0001",
  "NuGetPreReleaseTag": "feat-gitversion0001",
  "VersionSourceSha": "00154908779188a7172ab91f0f33ff0623b6a7c1",
  "CommitsSinceVersionSource": 3,
  "CommitsSinceVersionSourcePadded": "0003",
  "UncommittedChanges": 1,
  "CommitDate": "2023-06-15"
}
```

To configure GitVersion you must run the below

```shell
dotnet dotnet-gitversion init
```

Once complete, the init command will create a `GitVersion.yml` file in the working directory. It can be the root repository directory or any subdirectory in case you have a single repository for more than one project or are restricted to commit into a subdirectory.
