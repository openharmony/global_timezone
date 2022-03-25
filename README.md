# Time Zone

## Introduction

The time zone module provides the functions of updating, parsing, compiling, and deploying time zone data.

## Directory Structure

The directory structure of the time zone module is as follows:

```
/base/global/
├── timezone           # Code repository of the time zone module
│   ├── data          # Time zone compilation data
│   ├── tool          # Time zone management tools
│   │   ├── compile_tool              # Tool for compiling time zone data
│   │   └── update_tool          # Tool for updating time zone data
```

## Usage

Take time zone data update as an example. The time zone module searches for the latest version of the current time zone data from the Internet Assigned Numbers Authority (IANA) database. The module downloads the latest version to update the data only if a new version is available. Example:

```
cd tool/update_tool  // Switch to the directory where the update tool is located.
python3 download_iana.py  // Run the data update script.
```

## Repositories Involved

[Globalization Subsystem](https://gitee.com/openharmony/docs/blob/master/en/readme/globalization.md)

**global\_timezone**

[global\_i18n\_standard](https://gitee.com/openharmony/global_i18n_standard/blob/master/README.md)

[global\_resmgr\_standard](https://gitee.com/openharmony/global_resmgr_standard/blob/master/README.md)
