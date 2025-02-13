版本
====

版本号
------

GMT 版本号遵循“`语义化版本号规范 <https://semver.org/lang/zh-CN>`__”，其版本号格式为:

    *major.minor.patch*

其中，*major* 为主版本号，*minor* 为次版本号，*patch* 为补丁版本号，如 6.2.0。

根据“语义化版本号规范”的要求：

- 有大更新时（如重写底层代码），会增加主版本号 *major*。
  *major* 不同的两个版本的语法、功能以及 API 接口可能有差异
- 有较大更新时（如新增模块或者新增功能），会增加次版本号 *minor*
- 若只是修复代码 BUG 或改进文档，则增加补丁版本号 *patch*

因而，GMT 6.x.x 与 5.x.x 在底层存在很大差异，两个版本的语法不一定完全兼容；
GMT 6.2.x 相对于 6.1.x 增加了更多的功能；
GMT 6.1.1 相对于 6.1.0 则主要是修复了一些 BUG。

.. note::

    GMT 开发版的版本号略有不同，其格式为：

        *major.minor.patch*\_\ *hash*\_\ *yyyy.mm.dd*

    其中，*hash* 和 *yyyy.mm.dd* 是开发版中最新提交的 hash 值和日期。
    例如，6.1.0_267ce55_2020.01.21 表示更新于 2020 年 1 月 21 日、
    hash 值为 267ce55 的 6.1.0 开发版。

GMT 主流版本
------------

GMT 目前主流版本有 GMT6、GMT5 和 GMT4 三个主版本。这几个版本有什么区别呢？用户该如何选择呢？

GMT6 基本兼容 GMT4 和 GMT5 语法，且 GMT6 新增的现代模式语法更加简洁易用。
因而，建议所有 GMT 新用户学习并使用 GMT6 的现代模式。
GMT 老用户可以在 GMT6 下运行老脚本，但建议学习并使用 GMT6 现代模式写新脚本。

.. note::

    本文档中所有示例均使用 GMT6 的现代模式语法。

**GMT6**
    GMT6 是 GMT 目前的最新版本，也是开发者在持续维护和更新的版本。
    GMT6 特点在于：

    - 基本兼容 GMT4 和 GMT5 语法，因而老脚本无需修改或仅需少量修改即可在 GMT6 下使用，
      详情见\ :doc:`/migrating/index`\ 一节
    - 新增现代模式语法，其极大简化了绘图脚本，同时避免了 GMT 使用中的常见错误，
      详情见\ :doc:`/migrating/classic2modern`\ 一节
    - 新增模块

      - :doc:`/module/docs` 模块用于直接打开模块的网页文档
      - :doc:`/module/subplot` 模块用于绘制子图
      - :doc:`/module/inset` 模块用于绘制图中图
      - **movie** 模块用于制作动画

    - 相比于 GMT5 和 GMT4，GMT6 提供了更多新功能，并修复了很多 BUG

**GMT5**
    GMT5 的最终版本为 5.4.5，发布于 2019 年 1 月 4 日。GMT5 将不会再更新，所有 BUG 将不会得到修复。

    GMT5 相对于 GMT4 有诸多改进，其命令语法更统一，选项设计更合理，还增加了
    很多新功能。其中，常用的功能包括：

    - **-Bafg** 选项自动确定坐标轴的标注、刻度和网格间隔
    - **-X** 和 **-Y** 选项支持多种指定坐标原点的方式，画多子图的组合图时更加简单
    - **-p** 选项可以绘制任意 3D 视角图
    - 支持透明色和透明图层

**GMT4**
    GMT4 的最终版本为 4.5.18，发布于 2018 年 7 月。
    GMT4 将不会再更新，所有 BUG 将不会得到修复。
