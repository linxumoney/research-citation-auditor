# Research Citation Auditor：别让一条假引用毁掉整篇研究

论文和研究报告最危险的错误，往往不是观点不同，而是引用根本不支持这句话：作者写错、年份写错、二手来源冒充原始研究，甚至文献不存在。

`research-citation-auditor` 是一个面向研究人员、学生和专业写作者的开源 Agent Skill。它用“论断-证据账本”逐条检查引用是否存在、元数据是否一致、来源是否真正支持论断。

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

## 方法参考

本项目独立实现。引用管理问题域参考了 [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) 的公开研究工作流，该项目采用 MIT License。本项目不包含其脚本、数据库集成、环境变量设计或原文内容。

## License

MIT License。
