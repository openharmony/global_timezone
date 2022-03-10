# i18n

## Introduction

The timezone module provides a tool set for timezone data management which includes timezone data update, parse, compile, deploy.

## Directory Structure

The directory structure for the timezone module is as follows:

```
/base/global/
├── timezone           # repository for the timezone data management
│   ├── data          # Directory of compiled timezone data
│   ├── tool          # TimeZone data management tool set
│   │   ├── compile_tool              # TimeZone data compile tool
│   │   └── update_tool          # TimeZone data update tool
```

## Constraints

## Usage

Provide time zone data management functions, including time zone data update, parse, compile and deploy functions. Take the time zone data update tool as an example. This tool will search the latest version of the current time zone data from the IANA time zone data official website. If there is a new version, download the latest version to update the data; Otherwise, the data update operation is not performed. 

```
cd tool/update_tool  // change directory to update tool directory.
python3 download_iana.py  // run data update script.
```

## Repositories Involved

[Globalization subsystem](https://gitee.com/openharmony/docs/blob/master/en/readme/globalization.md)

**global\_timezone**

[global\_i18n\_standard](https://gitee.com/openharmony/global_i18n_standard/blob/master/README.md)

[global\_resmgr\_standard](https://gitee.com/openharmony/global_resmgr_standard/blob/master/README.md)

