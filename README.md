# Research Citation Auditor：论文引用核验与参考文献审计 Skill

论文和研究报告最危险的错误，往往不是观点不同，而是引用根本不支持这句话：作者写错、年份写错、二手来源冒充原始研究，甚至文献不存在。

`research-citation-auditor` 是一个面向研究人员、学生和专业写作者的开源论文引用核验与参考文献审计 Agent Skill。它通过“论断-证据账本”检查 DOI、PMID、arXiv、作者、年份和来源是否真实，以及文献是否真正支持当前论断。兼容 Codex、Claude Code、Cursor 和 OpenCode 等支持 `SKILL.md` 的工具。

## 它会检查

- DOI、PMID、arXiv ID 或正式页面能否验证
- 作者、标题、年份、期刊是否一致
- 原文到底支持、部分支持，还是不支持当前论断
- 是否把综述、新闻或二手引用当成原始证据
- 哪些重要论断没有引用，哪些引用重复或失效

## 使用示例

```text
用 $research-citation-auditor 审核这篇稿子的引用。
先建立论断-证据账本，不确定的文献不要补写。
```

## 安装

```bash
cp -R skills/research-citation-auditor ~/.codex/skills/
```

## 适用场景

- 论文、毕业设计、文献综述和研究报告引用核验
- 检查 DOI、PMID、arXiv ID、作者、年份和期刊信息
- 识别假引用、错引、二手引用和过度推断
- 审核 BibTeX、参考文献列表和重复引用
- 建立论断与证据的对应关系，找出缺失引用

## 常见问题

### 它会自动补充参考文献吗？

只有找到并核验真实来源后才会建议替换引用。无法验证的文献会明确标记，不会生成看起来正确的虚构 DOI。

### 只检查格式吗？

不只检查格式。它会分别判断“文献是否真实存在”和“文献是否支持这句话”，这是引用审计最关键的两个问题。

### 能代替同行评审吗？

不能。它适合发现引用和证据链问题，领域结论、统计方法和研究质量仍需要专业审查。

## 方法参考

本项目独立实现。引用管理问题域参考了 [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) 的公开研究工作流，该项目采用 MIT License。本项目不包含其脚本、数据库集成、环境变量设计或原文内容。

## License

MIT License。
