# 文献阅读 Skill

将科研论文整理为中文精读讲解：研究问题、术语、实验设计、逐图证据、局限与实验启发。按需保存到 Notion。

## 文件布局

```text
skills/literature-reading/
  SKILL.md
  agents/openai.yaml
  references/note-template.md
  references/notion-workflow.md
```

## 本地安装

将 `skills/literature-reading` 整个文件夹复制到 `$CODEX_HOME/skills/`；没有设置 `CODEX_HOME` 时，使用 `~/.codex/skills/`。

最终路径应为 `~/.codex/skills/literature-reading/SKILL.md`，而不是额外嵌套一层仓库目录。重新打开 Codex 会话后检查 skill 是否出现在可用列表中。自动选择保持默认开启，也可显式调用。

## 使用示例

```text
$literature-reading 请按文献阅读模式讲解这篇 PDF，重点解释每张图的证据和局限。
```

```text
$literature-reading 精读这篇论文，并整理到 Notion 的“文献”页面下。
```

```text
$literature-reading 只讲 Figure 3：各面板做了什么，是否足以支持作者的结论？
```

可以直接说“按文献阅读模式精读这篇文章”。是否自动选中由当前环境决定；显式调用适合需要明确指定流程时。

## 运行条件

- 由支持本地 skills 的 Codex 环境读取；本仓库本身不是独立运行的软件。
- PDF 需要可用的文本提取和页面查看能力；skill 不附带或自动安装第三方依赖。
- Notion 是可选能力，仅在用户请求保存且连接可用时写入；仅讲解时不要求连接 Notion。
- 链接、DOI 或外部文献核验需要可用的联网能力；无法获取时应报告覆盖范围。

## 上传 GitHub

在自己的 GitHub 仓库中上传本目录的内容，保留 `skills/literature-reading` 的层级。也可将该 skill 文件夹放进已有 skills 仓库。其他人安装时使用实际仓库地址和路径 `skills/literature-reading`。

本包仅包含通用指令和使用说明，不包含论文 PDF、阅读笔记、私人 Notion 页面地址或访问凭据。上传前可按自己的分享意愿添加许可证。

## 设计原则

读图和读文相互校验；直接证据、计算推断、作者假说、阅读者建议分别表述。保留实际未核对之处，不把候选调控因子写成已证实机制，不把单篇研究结论推广到所有物种与实验条件。
