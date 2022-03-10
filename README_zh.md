# 时区数据管理组件<a name="ZH-CN_TOPIC_0000001101364976"></a>

-   [简介](#section11660541593)
-   [目录](#section1464106163817)
-   [约束](#section1718733212019)
-   [说明](#section894511013511)
-   [相关仓](#section15583142420413)

## 简介<a name="section11660541593"></a>

**时区数据管理组件**提供时区数据的更新、解析、编译、部署功能。

## 目录<a name="section1464106163817"></a>

时区数据管理组件目录结构如下所示：

```
/base/global/
├── timezone           # 时区数据管理组件代码仓
│   ├── data          # 时区编译数据目录
│   ├── tool          # 时区数据管理工具
│   │   ├── compile_tool              # 时区数据编译工具
│   │   └── update_tool          # 时区数据更新工具
```

## 说明<a name="section894511013511"></a>

以时区数据更新为例，时区数据管理组件会从IANA时区数据官网搜索当前时区数据的最新版本。若存在新的版本，则下载最新版本进行数据更新，否则不执行数据更新操作。示例如下：

```
cd tool/update_tool  // 切换到更新工具所在目录
python3 download_iana.py  // 执行数据更新脚本
```

## 相关仓<a name="section15583142420413"></a>

全球化子系统

**global\_timezone**

global\_i18n\_standard

global\_resmgr\_standard

