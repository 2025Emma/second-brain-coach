# second-brain-coach

面向中文用户的 PARA/CODE 教练型 Skill，帮助你把蒂亚戈·福特《打造第二大脑》的理念落地。它会根据对话自动判定：是需要做系统诊断、文件归档，还是回答理论/实践问题；并在全过程中强制执行 PARA 四问脚本，并引用我们整理的 BASB 摘要。

## 仓库结构

`
second-brain-coach/
├── SKILL.md                       # Skill 元信息、工作流、守则
├── README.md                      # 使用说明（本文件）
├── LICENSE                        # MIT 许可
└── references/                    # 可引用的知识速查
    ├── basb-concepts.md           # BASB 定位、CODE 表格、常见问答
    ├── para-decision-tree.md      # PARA 定义、四问脚本、分类示例
    ├── system-diagnosis-checklist.md  # 诊断所需输入、常见差距、启动步骤
    └── practice-prompts.md        # Capture→Express 各阶段练习题
`

## 安装方式

1. 克隆或下载本仓库：
   `ash
   git clone https://github.com/2025Emma/second-brain-coach.git
   `
2. 将 second-brain-coach/ 整个文件夹复制到 Codex/WorkBuddy 读取的 skills 目录（默认 ~/.codex/skills/）。
3. 重启 Codex 或在界面中 “Reload Skills”。系统会自动加载该 Skill。

## 使用说明

- 触发条件：对话中出现 “第二大脑”“PARA”“CODE”“文件放哪里”“知识管理困惑”等关键词。
- Skill 初始化时，会请用户选择【系统诊断】【文件归档】【实践问答】，或根据描述自行路由。
- 回答过程中，必须引用 eferences/ 中对应条目（示例：（参见 basb-concepts:承诺#2）），避免粘贴原书大段文字。

## 自检 / 校验

在发布前，可以使用 skill-creator 提供的校验脚本快速检查结构是否合规：

`ash
python /path/to/skill-creator/scripts/quick_validate.py second-brain-coach
`

脚本依赖 pyyaml。如未安装，可先运行 pip install pyyaml。

## 关于引用

- eferences/ 里的内容为我们手写的概括，确保不包含长篇原文。
- 欢迎自行扩充参考笔记，但也请遵守 SKILL.md 中的引用指引，避免版权风险。

## 开源许可

本 Skill 以 MIT License 发布，可免费使用、修改和二次分发（保留版权声明即可）。如你喜欢这个 Skill，也欢迎分享或提交改进建议。
