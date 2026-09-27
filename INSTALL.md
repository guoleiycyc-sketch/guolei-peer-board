# 郭磊私董专家团 · 安装与使用说明

> 版本 1.0.0（2026-09-27）｜七人编制：board-facilitator 私董官岳察秋 / board-strategy 战略幕僚方致远 / board-model 商业模式幕僚盛意达 / board-growth 增长幕僚曾长青 / board-org 组织幕僚杨沃土 / board-review 复盘幕僚史鉴今 / board-challenger 黑帽子幕僚邓不同 ＋ board-intake 案前收纳

## 这是什么

一组对话式私董 skill：企业主（中小企业主/创业者）对自己的生意提出困惑，私董官接手——先案前打磨，把模糊主诉磨成一个真问题（案题）、建立案主档案，再主持六位幕僚的圆桌（幕僚之问只提问不给建议、反馈走三段式与「如果我是你」通道），最后以「可量化 + 监督人 + 复查日」的行动承诺收口。跨会话累积案主档案。

纯对话型 skill，不依赖任何专有工具调用。单技能可独立运行（点名某位幕僚），整团可开完整私董会。

## 安装

### 方式一 · Claude Code Plugin（推荐）

```
/plugin marketplace add guoleiycyc-sketch/guolei-peer-board
/plugin install guolei-peer-board@guolei-peer-board
```

一条命令装齐私董官＋六幕僚＋案前收纳，支持版本化升级（`/plugin update guolei-peer-board`）。

### 方式二 · 手动复制（Claude Code / Codex / 其他 agentskills.io 平台）

把 `skills/` 下八个目录（board-* 七件 + board-intake）平铺到平台 skill 目录（如 `~/.claude/skills/`）。

⚠️ 不要把整个仓库或 `skills/` 文件夹整个放进去——skill 目录的每个一级子目录必须直接含 SKILL.md，否则报「找不到 SKILL.md」。

### 方式三 · WorkBuddy（CodeBuddy）专家市场

用 Releases 里的 `guolei-peer-board.zip` 整包上传——这是 Team 型专家包（`.codebuddy-plugin/plugin.json` + `agents/` 七剧本 + `avatars/` + `rules/`），WorkBuddy 侧以私董官岳察秋为入口的整团调度（TeamCreate 建团、幕僚 spawn、产出回传汇编）。

## 使用（四种开始方式）

1. **开一场私董会**（推荐第一次用）：对 AI 说「帮我开一场私董会，盘一盘我生意上最大的难题」——私董官 board-facilitator 会开场定调、磨案题、主持八 Phase 圆桌
2. **直接说困惑**：「我公司的生意增长没劲」「人留不住」「天天救火」——私董官同样先接手，聚焦问题、建档定向
3. **点名幕僚**：如「让商业模式幕僚看看我这个生意」「帮我挑挑刺」（黑帽子）
4. **续会**：把上次案主档案粘贴回来，说「接着上次聊」——私董官第一件事核对上次行动承诺的兑现情况

## 专家团编制

| 角色 | 管什么 |
|------|--------|
| 私董官 board-facilitator（岳察秋） | 磨案题、主持八 Phase、护场域、落承诺；不给商业建议 |
| 战略幕僚 board-strategy（方致远） | 方向与定位：市场怎么看、往哪打、聚焦谁；收口 2-3 个必赢之战 |
| 商业模式幕僚 board-model（盛意达） | 生意设计：卖给谁、凭什么赚钱、客户为何回来 |
| 增长幕僚 board-growth（曾长青） | 增长使不上劲拆杠杆，订单一多就乱查流程 |
| 组织幕僚 board-org（杨沃土） | 人与土壤：留人/激励/人才盘点，先查土壤再怪种子 |
| 复盘幕僚 board-review（史鉴今） | 仗怎么盘、会怎么开：差距二分、五个为什么 |
| 黑帽子幕僚 board-challenger（邓不同） | 专职唱反调：事实缺口、逻辑漏洞、反例、共识盲区 |
| 案前收纳 board-intake | 四段陈述引导表、审题三规则、档案归档模板 |

## 常见问题

- **装了不触发？** 说「帮我开一场私董会」或点名某位幕僚即可直接激活；各 skill 的 description 已含大量中文口语触发词。
- **案主档案在哪？** 本地 `~/咨询档案/<企业简称>-档案.md`，不上传、不外发。
