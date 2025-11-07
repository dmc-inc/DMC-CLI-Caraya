# DMC CLI Caraya

This repository contains the code to use a better CLI Caraya. It is g-cli based and thus returns better feedback in the command line as well as allows for quicker Unit Test search that optionally uses bookmarks to include or exclude specific tests.

This uses a g-cli call in the form:

g-cli (optional)--lv-ver [LV_Year] (optional)--timeout [ms Timeout] "DMC CLI Caraya" -- [arguments]

This must be called from the working directory you want to analyze.

-------optional arguments-------
-source <relative to working directory paths, comma delimited. Defaults to working directory> (Can be .vi, folders, .lvproj)
-reportdir <absolute or relative to working directory relative path to report output directory. Defaults to workingdir/Reports>
-reportname <string name of xml report. Defaults to Caraya Test Results.xml>
-include <comma seperated string of all Bookmarks Unit Tests must have to be included. Defaults to include all>
-exclude <comma seperated string of all Bookmarks Unit Tests cannot have, or will be excluded. Defaults to none>
-verbose <Flag to set report verbose>
-help <Returns this help information>

# [Wiki Homepage](../../wikis/Home)

# Author(s), Contributors
* Contributor 1
* Contributor 2


# License
All software in this repository is licensed under the license found in [..\Build\License\](../master/Build/License/). 


---

This project was created 2023-10-24 12:44:06.304161 by copying https://git.dmcinfo.com/DMC/labview/dmc-templates/gitlab-template.

---

This project was created 2025-09-11 13:58:51.223686 by copying https://git.dmcinfo.com/DMC/labview/dmc-templates/DMC-Lib-Project-Template.