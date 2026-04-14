# second-brain-coach

Coach-style PARA/CODE skill that helps users implement Tiago Forte's Building a Second Brain methods. It routes questions into system diagnosis, guided filing, or practice Q&A, while enforcing the four-question PARA decision tree and referencing curated BASB summaries.

## Repository Contents

```
second-brain-coach/
├── SKILL.md                     # Skill frontmatter + workflows + guardrails
├── README.md                    # You are here
├── LICENSE                      # MIT license for the skill
└── references/
    ├── basb-concepts.md         # BASB positioning, CODE table, FAQ snippets
    ├── para-decision-tree.md    # PARA definitions, four-question script, examples
    ├── system-diagnosis-checklist.md  # Intake questions, common gaps, starter steps
    └── practice-prompts.md      # Capture → Express reflection/activation exercises
```

## Installation

1. Clone or download this repository.
2. Copy the second-brain-coach/ folder into your Codex skills directory (default ~/.codex/skills/).
3. Restart Codex or reload skills so the new skill metadata is discovered.

## Usage Overview

- Trigger conditions: user mentions “第二大脑”, PARA, CODE, 文件归档, 或其他知识管理困惑。
- Initialization prompt asks the user to choose【系统诊断】【文件归档】【实践问答】, then the skill follows the respective workflow.
- Knowledge answers must cite the corresponding reference file sections (e.g., `basb-concepts:承诺#2`).

## Validation

You can quickly lint the skill before publishing by running the skill-creator validator:

```
# From this repository root
python /path/to/skill-creator/scripts/quick_validate.py second-brain-coach
```

The validator checks frontmatter, paths, and reference structure. It requires pyyaml; install with pip install pyyaml if needed.

## Notes on Source Material

- The reference files contain original summaries of Tiago Forte’s published work. They intentionally avoid quoting large verbatim passages to respect copyright.
- Feel free to extend references/ with your own notes, but keep citation guidance in SKILL.md so downstream users know how to reference material responsibly.

## License

Released under the MIT License (see LICENSE). You may use, modify, and distribute the skill for free—credit is appreciated but not required.
