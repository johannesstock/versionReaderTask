# VersionReaderTaskExtended
VSTS build task to read Version tag from project files

Reads the `<Version>` tag from new `csproj` and `vbproj` 2017 format files into environment variables

##Generated Variables

* Version = Whole Version Tag - Example: 4.3.2.1
* Version.Major = First Number of Version Tag  - Example: 4
* Version.Minor = Second Number of Version Tag  - Example: 3
* Version.Build = Third Number of Version Tag  - Example: 2
* Version.Revision = Fourth Number of Version Tag  - Example: 1

## Arguments

### Path to .cs/vbproj
".??proj is the default value. This should find the xxproj file in the build sources directory. However, when building a multiple project solution one would want to enter the exact path.

### Variables Prefix
The value entered here will be prefixed to each variable name generated. This can be useful when using this task multiple times during a build and pointing each task to different AssemblyInfo files.

## Credits
This work is basically a mashup of those two projects:
-[versionReaderTask](https://github.com/conficient/versionReaderTask) with thanks to [conficient](https://github.com/conficient)
-[AssemblyInfoReaderTask](https://github.com/kyleherzog/AssemblyInfoReaderTask) with thanks to [kyleherzog](https://github.com/kyleherzog)
