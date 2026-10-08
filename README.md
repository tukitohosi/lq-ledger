# L.Q记账

简体中文 | [English](README.en.md)

**一个不用注册、日常使用不联网的个人消费账本。**

快速记录支出，按分类和月份看消费，设置预算，再把数据备份到自己的文件中。

当前 Windows 版本为 **1.3.2**，另提供 Android ARM64 预览包。[下载](https://github.com/tukitohosi/lq-ledger/releases/tag/v1.3.2) · [使用指南](项目介绍与使用指南.md)

## 主要功能

- 快速记账：最近分类、地点联想、复制上一笔、金额算式和常用模板。
- 查找记录：按月份、关键词、分类、日期和金额筛选。
- 消费统计：分类占比、上月对比、日均支出、最高消费日和六个月趋势。
- 分类与预算：自定义分类、合并分类、按一级或末级分类设置预算。
- 数据备份：完整 JSON 导出与恢复、CSV 报表和可选每日滚动备份。
- 浅色／深色主题、舒适／紧凑布局及键盘操作。

## 下载与安装

在 [v1.3.2 发布页](https://github.com/tukitohosi/lq-ledger/releases/tag/v1.3.2) 选择：

- **Windows x64**：LQ-Ledger-1.3.2-x64-Setup.exe。
- **Android 7.0+ ARM64 预览包**：LQ-Ledger-1.3.2-Android-arm64-debug.apk。

首次安装时若缺少 WebView2，安装程序可下载微软运行环境；应用日常使用不联网。

Android 包使用 Debug 签名，属于预览分发，其构建改动尚未包含在 v1.3.2 源码标签中。发布页列出了两个平台各自的校验值。

## 数据与限制

只记录人民币支出，面向单人使用。金额以整数“分”保存；账本保存在本机 SQLite 中。

完整 JSON 用于备份和跨电脑恢复，恢复前会自动备份当前账本。CSV 用于表格查看，不能恢复账本。Windows 正常卸载会保留应用数据；可在设置中选择自己的每日备份目录。

## 从源码运行

需要 Node.js、Rust 和 Windows 构建环境。

~~~powershell
npm install
npm run desktop:dev
~~~
