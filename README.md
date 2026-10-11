# 王国维·把审美判断落到作品细节

把审美判断落到作品细节：有资料依据、有使用边界、可复核的中文 Agent Skill。

**把熟悉的思想，变成下一次任务可用的方法。**

适合：评论诗词或创作只有好美、需要说明景与情如何相连。

交付：选定作品与版本 → 分开人物感受、叙述者态度和读者投射 → 观察情感怎样借具体景物形成 → 比较有我与无我阅读角度 → 用具体改写检验景情联系 → 交付细节评论与修改理由。

**一分钟看懂**：一句雨打空窗被评论为高级但无理由。

本 Skill 会这样处理：指出声响、空窗视角与孤独解释的证据；保留其他情境，不把感觉当唯一答案。

[用途与同类差异](references/positioning.md)。人物知名度提供发现入口，实际价值来自工作流与可复核产物；不保证星标增长。

## 安装与使用
公开仓库直接提供 Skill，不依赖 GitHub Release。
```sh
npx skills add constantin2088/wang-guowei-aesthetic-scenes-skill
```
也可将仓库内容复制到支持该格式的客户端 Skill 目录，保留以 `wang-guowei-aesthetic-scenes-skill` 命名的文件夹和根目录 SKILL.md。客户端支持范围以其文档为准。安装后提出具体任务，由客户端按描述加载。

**试用任务**：一句雨打空窗被评论为高级但无理由。

## 内容
- [执行说明](SKILL.md)
- [资料卡](references/sources.md)、[工作表](references/frameworks.md)、[边界](references/boundaries.md)
- [三个示例](examples/demo.md)、[十个行为评测场景](evals/test-cases.md)

## 验证与贡献
```sh
python scripts/check_skill.py . --release
python -m unittest discover -s tests -v
python scripts/check_links.py
```
`--release` 是完整性检查参数，不创建 GitHub Release。CI 在每次提交运行上述检查。独立客户端模型行为评测尚未执行；用例、结构检查与实际模型能力分开报告。
修改时提供来源和定位，区分原文与转译；运行检查后直接提交到仓库。不要创建发布附件作为必需安装步骤。系列标识、链接和推荐由总仓库 catalog/skills.json 同步，避免手工修改受管理区块。

## 许可
项目原创内容使用 [MIT](LICENSE)。链接所指第三方作品保留原权利，本仓库不重新许可它们。
