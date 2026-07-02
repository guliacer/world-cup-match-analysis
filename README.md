# 世界杯球赛分析项目

<p align="center">
  <strong>AI 驱动的世界杯比赛分析规则、网页模板与静态报告生成项目</strong>
</p>

<p align="center">
  <a href="#使用-codex-生成报告">Codex 使用方法</a> ·
  <a href="#使用豆包生成报告">豆包使用方法</a> ·
  <a href="#推荐查看方式">长截图查看</a> ·
  <a href="#仓库更新建议">仓库推送</a>
</p>

> [!IMPORTANT]
> 本项目是一个 AI 数据分析与页面生成学习项目。所有比赛预测内容仅供娱乐、技术研究及 AI 学习参考。
>
> 严禁将本项目内容用于任何形式的赌球、资金充值、投注决策、盘口推荐或收益承诺。项目中的概率、比分、盘口倾向和分析结论均不构成任何投注建议。
>
> 请理性看球，拒绝赌博。

## 项目展示

三张长截图展示了生成后的比赛分析页面效果。截图放在同一排，仓库页面较窄时可以左右滑动查看。

| 西班牙 vs 奥地利 | 葡萄牙 vs 克罗地亚 | 瑞士 vs 阿尔及利亚 |
| --- | --- | --- |
| <a href="docs/images/showcase-spain-austria.png"><img src="docs/images/showcase-spain-austria.png" alt="西班牙 vs 奥地利比赛预测分析长截图" width="360"></a> | <a href="docs/images/showcase-portugal-croatia.png"><img src="docs/images/showcase-portugal-croatia.png" alt="葡萄牙 vs 克罗地亚比赛预测分析长截图" width="360"></a> | <a href="docs/images/showcase-switzerland-algeria.png"><img src="docs/images/showcase-switzerland-algeria.png" alt="瑞士 vs 阿尔及利亚比赛预测分析长截图" width="360"></a> |

## 项目简介

本项目用于生成「世界杯比赛预测分析 HTML 页面」。仓库内包含分析规则、网页模板、示例生成脚本，以及由不同 AI 工具生成的静态 HTML 分析报告。

分析内容应基于真实数据、可靠来源与明确计算口径。无法核验的数据应明确标记，避免把推测写成事实。

## 项目速览

| 模块 | 说明 |
| --- | --- |
| `世界杯分析规则.md` | AI 生成比赛分析页面时遵循的结构、数据口径和风险提示规则 |
| `分析结果网页模版.html` | 静态 HTML 报告模板，包含页面结构、样式与占位符 |
| `GPT/` | Codex/GPT 方案相关脚本与生成报告 |
| `GPT/outputs/` | GPT 方案输出的 HTML 报告目录 |
| `豆包/` | 豆包方案相关脚本与生成报告 |
| `豆包/output/` | 豆包方案输出的 HTML 报告目录 |
| `docs/images/` | README 使用说明截图 |

## 目录结构

```text
.
├── README.md
├── 世界杯分析规则.md
├── 分析结果网页模版.html
├── docs/
│   └── images/
├── GPT/
│   ├── generate_england_drc_report.py
│   ├── outputs/
│   └── *.html
└── 豆包/
    ├── generate_england_drc_report.py
    ├── output/
    └── *.html
```

## 快速开始

本项目当前生成脚本仅依赖 Python 标准库。

```bash
python GPT/generate_england_drc_report.py
```

生成后的 HTML 报告会输出到对应目录：

```text
GPT/outputs/
豆包/output/
```

也可以直接双击已有的 `.html` 报告文件，在浏览器中查看静态页面。

## 使用 Codex 生成报告

Codex 适合直接读取本地项目中的规则文件和网页模板，再按指定比赛生成新的 HTML 报告。

| 步骤 | 操作 | 目标 |
| --- | --- | --- |
| 1 | 指定本地项目地址 | 让 Codex 能读取规则、模板和历史输出 |
| 2 | 输入比赛分析提示词 | 明确比赛双方和输出要求 |
| 3 | 等待 Codex 生成 | 核查数据、填充模板并输出 HTML |
| 4 | 打开输出文件 | 在浏览器中查看最终报告 |

### 1. 指定本地项目地址

在 Codex 中打开或指定本地项目目录，例如：

```text
W:\世界杯球赛分析项目
```

确认 Codex 可以看到这些核心文件：

- `世界杯分析规则.md`
- `分析结果网页模版.html`
- `GPT/` 或 `豆包/` 中已有的生成脚本与输出示例

### 2. 输入分析提示词

把比赛双方写进提示词，让 Codex 按项目内规则分析比赛，并根据模板重新生成文件。

```text
按照我设定好的规则，帮我分析【西班牙】VS【奥地利】的那场世界杯比赛，然后将分析到的结果根据模版重新生成一个文件给我。
```

<p align="center">
  <img src="docs/images/codex-step-01-prompt.png" alt="在 Codex 中输入比赛分析提示词" width="820">
</p>

### 3. 等待 Codex 分析并生成文件

Codex 会读取规则、核查比赛信息、整理分析数据，并修改或新增生成脚本，最后输出新的 HTML 报告文件。

<p align="center">
  <img src="docs/images/codex-step-02-running.png" alt="Codex 根据规则生成分析报告" width="820">
</p>

### 4. 在输出目录中查看结果

生成完成后，可以在输出目录中找到新的 `.html` 文件：

```text
GPT/outputs/
豆包/output/
```

<p align="center">
  <img src="docs/images/codex-step-03-output-file.png" alt="在输出目录中找到生成的 HTML 文件" width="760">
</p>

打开 HTML 文件后，即可查看完整比赛预测分析页面。

<p align="center">
  <img src="docs/images/codex-step-04-report-page.png" alt="打开生成后的比赛预测分析页面" width="820">
</p>

## 使用豆包生成报告

豆包也可以读取本地项目中的规则和模板，按同样流程生成比赛分析 HTML 文件。

| 步骤 | 操作 | 目标 |
| --- | --- | --- |
| 1 | 新建办公任务并指定本地项目 | 让豆包访问规则、模板和示例文件 |
| 2 | 输入比赛分析提示词 | 指定比赛双方与生成目标 |
| 3 | 等待豆包读取规则并生成 | 根据模板输出 HTML 分析报告 |
| 4 | 打开输出目录 | 检查生成结果和页面效果 |
| 5 | 分享文件或长截图 | 方便归档、移动端查看和群聊分享 |

### 1. 指定本地项目地址

在豆包中新建办公任务，选择本地电脑或本地项目目录，并指定项目地址，例如：

```text
W:\世界杯球赛分析项目
```

建议确认豆包可以访问这些文件：

- `世界杯分析规则.md`
- `分析结果网页模版.html`
- `豆包/` 中已有的生成脚本与输出示例

### 2. 输入分析提示词

把比赛双方写进提示词，让豆包按照规则文件分析比赛，并根据网页模板重新生成文件。

```text
按照我设定好的规则，帮我分析【西班牙】VS【奥地利】的那场世界杯比赛，然后将分析到的结果根据模版重新生成一个文件给我。
```

<p align="center">
  <img src="docs/images/doubao-step-01-prompt.png" alt="在豆包中指定本地项目并输入分析提示词" width="820">
</p>

### 3. 等待豆包读取规则并生成报告

豆包会定位规则文件和模板文件，读取项目内已有示例，再补充比赛数据、生成分析内容和新的 HTML 文件。

<p align="center">
  <img src="docs/images/doubao-step-02-running.png" alt="豆包读取规则和模板并生成报告" width="820">
</p>

### 4. 在豆包输出目录查看结果

生成完成后，可以在豆包输出目录中找到新的 `.html` 文件：

```text
豆包/output/
```

<p align="center">
  <img src="docs/images/doubao-step-03-output-file.png" alt="在豆包输出目录中查看生成的 HTML 文件" width="760">
</p>

打开报告后即可查看完整的比赛预测分析页面。如果需要图片版，也可以配合 LShot 导出长截图。

<p align="center">
  <img src="docs/images/doubao-step-04-report-page.png" alt="打开豆包生成的比赛预测分析页面" width="820">
</p>

### 5. 分享报告文件或长截图

生成后的 `.html` 文件适合在电脑端查看和归档；导出的长截图适合在聊天工具、移动端或群聊中快速分享。

<p align="center">
  <img src="docs/images/doubao-step-05-share.png" alt="分享豆包生成的 HTML 文件和长截图" width="520">
</p>

## 标准生成流程

1. 参考 `世界杯分析规则.md` 确认分析结构、数据口径和风险提示要求。
2. 在 `分析结果网页模版.html` 中维护页面结构、样式和占位符。
3. 在生成脚本中准备比赛双方、市场数据、概率模型、比分分布、风险提示等字段。
4. 运行脚本生成 HTML 报告。
5. 打开 HTML 文件检查页面展示、数据一致性和免责声明。

## 推荐查看方式

报告默认以网页形式展示，适合在浏览器中阅读和归档。

如果用户不喜欢网页查看，更喜欢把完整报告保存成一张长图，推荐使用油猴脚本插件：

- [guliacer/LShot](https://github.com/guliacer/LShot)：可将网页长截图为一个图像，方便保存、分享或在移动端查看。

使用方式：打开生成后的 HTML 报告页面，点击 LShot 的「长截图」按钮，即可将完整网页导出为一张图片。

<p align="center">
  <img src="docs/images/codex-step-05-lshot-download.png" alt="使用 LShot 将网页导出为长截图" width="520">
</p>

导出的长图可以直接用于移动端查看、聊天分享或归档。

<p align="center">
  <img src="docs/images/codex-step-06-share.png" alt="分享 HTML 文件和长截图" width="520">
</p>

## 仓库更新建议

首次推送前可以执行：

```bash
git add .
git commit -m "init world cup analysis project"
git branch -M main
git remote add origin <你的仓库地址>
git push -u origin main
```

后续更新报告或模板时：

```bash
git add .
git commit -m "update match analysis reports"
git push
```

## 内容规范

| 要求 | 说明 |
| --- | --- |
| 数据真实 | 不编造数据来源，无法确认的数据应标注为「待核验」或「部分核验」 |
| 结论一致 | 概率、比分、盘口和主推结论之间应避免互相矛盾 |
| 风险明确 | 临场伤停、首发、天气、赔率和盘口变化都应写入风险提示 |
| 输出清晰 | HTML 报告应适合提交到仓库、离线查看或部署到静态站点 |

## 免责声明

本项目仅用于足球比赛数据分析、预测建模和网页展示研究。所有预测结果均存在不确定性，不保证准确率，不构成投资、博彩或任何形式的决策建议。

请理性看球，拒绝赌博。
