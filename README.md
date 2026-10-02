# 流浪猫窝计划 · stray-cat-pod

一个面向半户外场景的模块化流浪猫窝开源设计项目，从「流浪猫窝计划」的方案文档与概念图孵化而来。目标是做出可移动、可维护、可复制的猫屋，并公开设计源文件、打印网格与试制记录。

当前处于方案与概念参考阶段：已归档一份 v1.0 计划和三轮共 18 张概念图；本仓库尚无 SolidWorks 模型、打印网格或实际验证记录。进度以 [STATUS.md](STATUS.md) 为准。

## 设计方向

沿用原计划的 A++ 路线：硬件结构优先 PETG 分件打印，使用榫卯、滑槽、燕尾、楔块和卡扣等连接；胶接用于允许半永久固定的区域。屋顶、内胆盘、检修口和软装保持可拆，默认不依赖金属紧固件。防水、防风、保温和通风通过结构设计与试验逐步验证。

原计划的约 600 × 520 × 550 mm 外形、450 × 380 × 380 mm 内部净空间等数值都是待验证目标。设备与打印边界来自历史计划记录，实际建模前需重新核对。

## 从哪里开始

- [设计计划 v1.0](docs/design-plan-v1.md)：需求、分件设想、初始参数、成本估算和测试安排。
- [设计参考索引](references/README.md)：三轮外观与结构概念图、历史说明和来源记录。
- [STATUS.md](STATUS.md)：当前状态、下一步与更新记录。
- [CONTRIBUTING.md](CONTRIBUTING.md)：如何提交设计建议、模型或试制反馈。

概念图可直接在浏览器或图片查看器中打开，无需安装依赖。后续 CAD 组件按根目录独立文件夹组织；下载模型时保留零件与装配体的相对路径，修改源模型后同步导出 STL。

## 开发组件

目前为 0 个。待选定分件与接口后，按实际开发需要建立组件目录，保存 SolidWorks 零件、装配体（如适用）和导出的 STL；不预先创建空组件或占位 CAD 文件。

## 目录导览

```text
stray-cat-pod/
├── <component-name>/           # 后续实际开发的组件，尚未建立
├── docs/
│   ├── README.md               # 设计文档导览
│   └── design-plan-v1.md        # 继承的 v1.0 设计计划
├── references/
│   ├── README.md               # 参考索引与命名规则
│   ├── import-manifest.tsv     # 孵化资料映射与 SHA-256
│   ├── shelter-v01/            # 第一轮：公共设施与结构探索，10 张
│   ├── shelter-v02-cute/        # 第二轮：A++ 克制萌，4 张
│   └── shelter-v03-cat-elements/ # 第三轮：建筑化猫元素，4 张
├── README.md
├── STATUS.md
├── CONTRIBUTING.md
├── AGENTS.md
├── CLAUDE.md
├── LICENSE
├── .gitignore
├── .gitattributes
└── .editorconfig
```

## 开源许可

本项目沿用 lab-workspace-suite 的 [CC BY 4.0](LICENSE)。项目自有设计与文档按该协议提供；引用或收录的第三方资料遵循其原许可，AI 概念图的来源与许可确定程度见各方案说明。署名可注明「WenjayWu / stray-cat-pod」并链接实际取得资料的仓库地址。

本次完成本地 Git 初始化；远程地址与公开发布状态见 [STATUS.md](STATUS.md)。
