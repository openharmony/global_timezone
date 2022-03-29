# 时区数据管理组件

## 简介

时区数据管理组件提供时区数据的更新、编译等功能。

## 目录

时区数据管理组件目录结构如下所示：

```
/base/global/
├── timezone           # 时区数据管理组件代码仓
│   ├── data          # 时区编译数据目录
│   ├── tool          # 时区数据管理工具
│   │   ├── compile_tool              # 时区数据编译工具
│   │   └── update_tool          # 时区数据更新工具
```

## 说明

时区数据更新工具会从[IANA时区数据官网](https://data.iana.org/time-zones/releases/)搜索当前时区数据的最新版本。若官网存在新的时区数据版本，则时区数据更新工具会下载最新版本时区数据进行数据更新，否则不执行数据更新操作。更新的时区数据会被保存到./data/iana/目录下，示例如下：

```
cd tool/update_tool  // 切换到时区数据更新工具所在目录
python3 download_iana.py  // 执行数据更新脚本
```

时区数据编译工具会对时区源数据进行编译，并在./data/prebuild/posix目录下生成时区二进制数据。示例如下：

```
cd tool/compile_tool  // 切换到时区数据编译工具所在目录
chmod 755 compile.sh
./compile.sh  // 执行数据更新脚本
```

## 相关仓

[全球化子系统](https://gitee.com/openharmony/docs/blob/master/zh-cn/readme/全球化子系统.md)

**global\_timezone**

[global\_i18n\_standard](https://gitee.com/openharmony/global_i18n_standard/blob/master/README_zh.md)

[global\_resmgr\_standard](https://gitee.com/openharmony/global_resmgr_standard/blob/master/README_zh.md)

