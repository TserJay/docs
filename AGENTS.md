# 个人博客项目说明

## About this project

- 这是 TserJay 的个人博客，基于 [Mintlify](https://mintlify.com) 构建
- 站点地址：[tserjay.club](https://tserjay.club)
- 页面为 MDX 文件，带 YAML frontmatter
- 配置文件为 `docs.json`
- 本地预览：`mint dev`
- 提交前检查：`mint validate` 与 `mint broken-links`

## Site structure

- `index.mdx` — 首页
- `resources.mdx` — 学习资源
- `notes/vllm/` — vLLM 学习笔记
  - `v1-features.mdx` — vLLM V1 新增特征
  - `paged-attention.mdx` — PagedAttention 与 KV Cache
- `notes/cuda/` — CUDA 算子笔记
  - `flash-attention.mdx` — FlashAttention 分块计算
  - `reduce.mdx` — Reduce 算子
- `images/` — 笔记配图

## Adding a new note

1. 在 `notes/<分类>/` 下新建 MDX 文件，例如 `notes/cuda/softmax.mdx`
2. 在 `docs.json` 的 `navigation.tabs` → 「学习记录」对应 group 的 `pages` 中加入路径（不带 `.mdx` 后缀）
3. 如果更换了已有页面的路径，在 `docs.json` 的 `redirects` 中补一条重定向

## Writing guidelines

- 中文内容为主，技术术语保留英文原文
- 标题使用名词短语或陈述句，避免「为什么」「这一章」「下面」这类引导性措辞
- 引用外部资料时，在首次提及处直接给出链接，而不是只堆在文末
- 代码、文件名、命令、路径使用行内代码格式
- 段落之间留空行；Markdown 有序列表用 `1.` 加缩进，避免多条内容挤成一段

## Content boundaries

- 只记录个人学习过程中的理解与实践，不复制整篇受版权保护的书籍或论文内容
- 引用他人文章时标注来源链接
