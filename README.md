# i18n<a name="EN-US_TOPIC_0000001101364976"></a>

-   [Introduction](#section11660541593)
-   [Directory Structure](#section1464106163817)
-   [Constraints](#section1718733212019)
-   [Usage](#section894511013511)
-   [Repositories Involved](#section15583142420413)

## Introduction<a name="section11660541593"></a>

The timezone module provides a tool set for timezone data management which includes timezone data update, parse, compile, deploy.

## Directory Structure<a name="section1464106163817"></a>

The directory structure for the timezone module is as follows:

```
/base/global/
├── timezone           # repository for the timezone data management
│   ├── data          # Directory of compiled timezone data
│   ├── tool          # TimeZone data management tool set
│   │   ├── compile_tool              # TimeZone data compile tool
│   │   └── update_tool          # TimeZone data update tool
```

## Constraints<a name="section1718733212019"></a>

## Usage<a name="section894511013511"></a>

Provide time zone data management functions, including time zone data update, parse, compile and deploy functions. Take the time zone data update tool as an example. This tool will search the latest version of the current time zone data from the IANA time zone data official website. If there is a new version, download the latest version to update the data; Otherwise, the data update operation is not performed. 

```
cd tool/update_tool  // change directory to update tool directory.
python3 download_iana.py  // run data update script.
```

## Repositories Involved<a name="section15583142420413"></a>

Globalization subsystem

**global\_timezone**

global\_i18n\_standard

global\_resmgr\_standard

