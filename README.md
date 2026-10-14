# paper-ppt-outline

将单篇学术论文、论文笔记或文献总结整理成中文组会/学术汇报的 Markdown 幻灯片提纲。它生成的是面向讲述者的提纲，不会直接生成 PPTX。

## 安装

将整个 `paper-ppt-outline` 文件夹复制到目标电脑的 Codex 全局技能目录：

```text
~/.codex/skills/paper-ppt-outline/
```

Windows 的常见位置是：

```text
C:\Users\<用户名>\.codex\skills\paper-ppt-outline\
```

重启 Codex 或新开一个对话后，即可用中文的“把这篇论文整理成组会 PPT 提纲”等请求触发它。

## 打包发布

将此目录作为一个 Git 仓库发布即可。安装者只需要保留 `SKILL.md`；`README.md` 仅提供说明。

## 设计边界

- 面向单篇论文的汇报提纲；多篇文献的系统综述应使用单独的综述工作流。
- 需要生成实际 `.pptx` 时，请在提纲完成后交给演示文稿工具或模板处理。
- 保留证据与推测的边界，不会补造论文未给出的结论。
