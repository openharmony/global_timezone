# 时区数据管理组件

## 简介

时区数据管理组件 提供时区数据的更新、解析、编译、部署功能。

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

以时区数据更新为例，时区数据管理组件会从IANA时区数据官网搜索当前时区数据的最新版本。若存在新的版本，则下载最新版本进行数据更新，否则不执行数据更新操作。示例如下：

```
cd tool/update_tool  // 切换到更新工具所在目录
python3 download_iana.py  // 执行数据更新脚本
```

## 相关仓

[全球化子系统](https://gitee.com/openharmony/docs/blob/master/zh-cn/readme/全球化子系统.md)

**global\_timezone**

[global\_i18n\_standard](https://gitee.com/openharmony/global_i18n_standard/blob/master/README_zh.md)

[global\_resmgr\_standard](https://gitee.com/openharmony/global_resmgr_standard/blob/master/README_zh.md)

