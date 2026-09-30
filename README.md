# Fg小助手

#### 介绍

基于 Wails v2（Go + React）的一体化安全测试辅助桌面工具，同时内置 AI Coding Agent 工作台。集成信息收集、漏洞专区、工具专区、工具专区、情报专区、APP小程序、资产管理、webshell管理、C2管理、AK管理、应急日志分析等 50+ 实战模块，多数据源可视化聚合，自动化重复性安全测试工作。

- **开箱即用**：单安装包分发，无需配置运行环境，Windows 10/11 直接运行，目前仅支持windows。
- **本地优先**：扫描引擎、漏洞库、指纹库全部本地运行；API Key 通过 Windows DPAPI（当前用户域）加密存储于本机
- **AI 加持**：Coding Agent 支持 Diff 审批、经验库沉淀、MCP/Skills 扩展、沙盒预览与 normal/plan/yolo 三档运行模式

<img width="2559" height="1334" alt="image" src="https://github.com/user-attachments/assets/b6740971-a6dc-450d-b17c-f3cbaf150f59" />


**功能模块一览**

| 分类 | 模块 |
|------|------|
| 渗透测试 | 漏洞验证、PoC 库与生成器、漏洞扫描、未授权验证、漏洞库（VulnDB）、修复建议、渗透报告导出 |
| 信息收集 | Google 语法、FgFinder、目录枚举、域名/IP 查询、GitHub 泄露搜索、企业查询、Web 指纹、站点监控 |
| 资产测绘 | 五平台聚合（Hunter/FOFA/ZoomEye/Quake/Shodan）、资产总览/采集/资产库、AK 管理 |
| 扫描与利用 | 端口扫描（fscan 内核）、内网扫描、Mapkey 利用 |
| 流量与取证 | WebShell 文件扫描（含压缩包递归）、WebShell 流量检测（自动解码 / PHP AST / 家族识别）、PCAP 深度分析、HTTP 数据重放 |
| 数据库 | 数据库连接助手（20+ 类型，覆盖 SQL/NoSQL/搜索引擎/国产数据库）、数据库检索、敏感数据风险报告 |
| 应急响应 | 主机采集器（Windows/Linux）、检测与关联引擎、一键取证报告（Linux/Windows 模板） |
| 情报舆情 | 漏洞情报、威胁情报、微信安全情报、暗网监测、舆情监控、公众号扫描 |
| AI 工作台 | Coding Agent（Diff 审批/经验库/MCP/Skills/沙盒预览）、知识库、AI 代码审查、IM 机器人 |
| 实用工具 | 编解码、加解密、网络拓扑设计、接码平台、网盘搜索、隐私检查 |

**功能视频展示**

<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/5f227f55-0515-46c3-8113-1a74f0863cda" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/5da3f268-a343-4903-86a8-1bfc82940d8a" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/f85ca0c0-1460-48a7-8f3f-37d681ae9718" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/b313b348-553d-49ac-9f24-10384ce9ee21" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/08bbdc9f-613a-4717-b419-b3a61c87cd93" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/39eab19a-10bb-4f1b-8542-749b6c784ff0" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/46e99f79-cd1c-4fbe-80d8-ccdceed12d79" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/36db94e5-284c-428b-9114-775dde411850" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/c57ec0a3-de78-4d9a-b586-a45a3f055d26" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/9f2b144c-8092-4cf1-8344-f8b742478e9e" />
<img width="2559" height="1368" alt="image" src="https://github.com/user-attachments/assets/2162fed3-9e37-4dea-a9cb-fe1df09b8ca8" />


#### 安装教程

1. 前置要求：Windows 10/11 x64 与 WebView2 Runtime（Win10/11 系统自带；如缺失，安装器会自动提示安装）
2. 从 Releases 下载最新安装包（NSIS 安装器），双击运行，按向导完成安装
3. 首次启动进入激活向导：将机器码发送给供应商获取许可证，粘贴许可证文本块完成激活（支持离线激活）
4. 在「设置 → 模型服务」配置 AI 提供商与 API Key；在「设置 → 数据源 / 资产管理设置」按需填写各数据源 API Key/Cookie，保存即生效

#### 需求联系
<img width="801" height="513" alt="image" src="https://github.com/user-attachments/assets/f841912d-1799-462f-88e3-45102127d57c" />


#### 使用说明

1. 启动后通过左侧模块导航切换功能域（渗透测试 / 信息收集 / 资产测绘 / 应急响应 / 情报舆情 / 工具箱等）
2. AI 工作台选择运行模式：`normal`（逐步审批，界面显示为 auto）/ `plan`（先规划、批准后执行）/ `yolo`（会话内自动执行，请谨慎使用）
3. 扫描类任务提交后可在进度面板实时查看结果，支持一键导出报告（docx/CSV）
4. IM 机器人在设置中绑定平台 Token/Webhook 后，即可远程接收任务推送与告警

#### 免责声明

本工具仅面向**已获授权**的安全测试、应急响应与安全研究场景。请遵守《网络安全法》及相关法律法规，未经授权对目标系统进行测试属违法行为，由此产生的一切后果由使用者自行承担。

