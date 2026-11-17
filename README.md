# AI 办公室 · 本地可运行包

双击 `启动.bat`，浏览器会自动打开。**不需要联网，不需要 pip 安装任何东西。**

## 环境要求
- Windows 10 / 11
- Python 3.9 及以上（安装时勾选 "Add Python to PATH"）

## 三个页面
| 地址 | 内容 |
|---|---|
| http://127.0.0.1:8790/ | 作品集首页（Bento 布局 + 真实产出样张） |
| http://127.0.0.1:8790/workbench | 工作台（52 个模块，卡片可点） |
| http://127.0.0.1:8790/terminal | 命令终端（可执行 PowerShell） |

## 开箱即用的四个演示
| 演示 | 做什么 |
|---|---|
| 系统信息 | 打印操作系统、Python 版本、架构 |
| 列出当前目录 | 等价 `dir` |
| 生成 Markdown 报告 | 输出 `artifacts/demo_report.md`（真实报价核查表） |
| 生成 SVG 图表 | 输出 `artifacts/demo_chart.svg`（流水线耗时柱状图） |

## 能做什么
- **终端**：执行任意 PowerShell 命令（`dir`、`git`、`python`、`npm`…）
- **工作台**：52 个模块卡片，点开看说明与命令
- **产物**：报告和图表生成在 `artifacts/` 目录

## 安全边界
- 危险命令直接拦截：`format` / `diskpart` / `reg delete HKLM` / `shutdown` / `vssadmin delete` / `cipher /w`
- 文件打开限制在包目录内
- 命令超时 180 秒

## 停止
关闭那个命令行窗口，或在窗口里按 Ctrl+C。

## 换端口
```
python serve.py 8800
```
或者 `启动.bat 8800`
