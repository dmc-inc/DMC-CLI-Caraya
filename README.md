# DMC CLI Caraya

This package provides an improved command-line interface for Caraya, built on the g-CLI framework. It streamlines unit test execution and enhances developer feedback during automated testing workflows.
Key Features

Improved CLI Feedback: Utilizes g-CLI to deliver clearer, more structured output directly in the command line.
Efficient Test Discovery: Accelerates the search for unit tests, with optional support for bookmarks to include or exclude specific tests dynamically.

This toolkit is ideal for teams seeking faster, more flexible unit testing in LabVIEW environments, especially when integrating with automated workflows.

This uses a g-cli call in the form:

g-cli --arch 64 (optional)--lv-ver [LV_Year] (optional)--timeout [ms Timeout] "DMC CLI Caraya" -- [arguments]

This must be called from the working directory you want to analyze.

## Optional Arguments
- **-source** | relative to working directory paths, comma delimited. 
  - ***Default***: Defaults to working directory (Can be .vi, folders, .lvproj)
- **-reportdir** | absolute or relative to working directory relative path to report output directory. 
  - ***Default***: Defaults to *WorkingDir*/Reports
- **-reportname** | string name of xml report. 
  - ***Default***: "Caraya Test Results.xml"
- **-include** | comma seperated string of all Bookmarks Unit Tests must have to be included.
  - ***Default***: Defaults to include all
- **-exclude** | comma seperated string of all Bookmarks Unit Tests cannot have, or will be excluded.
  - ***Default***: Defaults to none
- **-verbose** | Flag to set report verbose
- **-help** | Returns this help information

## Example Use Cases

### Default Report Run
Will run a standard Caraya run on all files under the Working Directory A XML report will be generated in Working Directory / Reports
```
cd <Root Code Directory>
g-cli "DMC CLI Caraya" -- -verbose
```
#### Example Output
```
Running Caraya
Searching for Caraya Unit Tests
Found 23 Caraya Unit Tests in 00:00:00
23 remain after Bookmark Filtering
Total Discovery Time 00:00:00 
Running 1 of 23: Test Assert Almost Equal (Float)
Running 2 of 23: Test Assert Equal (Float Units)
Running 3 of 23: Test Assert Equal - deprecated
Running 4 of 23: Test Assert Equal Type
Running 5 of 23: Test Assert Equal Value (Arrays)
Running 6 of 23: Test Assert Equal Value (Typedef)
Running 7 of 23: Test Assert Equal Value and Type
Running 8 of 23: Test Assert Equal Value
Running 9 of 23: Test Assert Error
Running 10 of 23: Test Assert False
Running 11 of 23: Test Assert Greater Or Equal
Running 12 of 23: Test Assert Greater
Running 13 of 23: Test Assert In Assert Wrapper
Running 14 of 23: Test Assert In SubVI
Running 15 of 23: Test Assert Less Or Equal
Running 16 of 23: Test Assert Less
Running 17 of 23: Test Assert Not Equal - deprecated
Running 18 of 23: Test Assert Not Equal Type
Running 19 of 23: Test Assert Not Equal Value (Typedef)
Running 20 of 23: Test Assert Not Equal Value and Type
Running 21 of 23: Test Assert Not Equal Value
Running 22 of 23: Test Assert Not Error
Running 23 of 23: Test Assert True
Caraya Unit Testing Completed
23 total tests, 121 total assertions.
0 tests failed, 0 assertions failed.
Please find the full report at "*WorkingDir*\Reports\Caraya Test Results.xml".
Exiting Caraya
```

# [Wiki Homepage](../../wikis/Home)

# Author(s), Contributors
* Jonathan Jay


# License
All software in this repository is licensed under the license found in [..\Build\License\](../master/Build/License/). 
