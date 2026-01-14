# Deep Research

[中文文档](README_CN.md)

A Claude Code Skill that transforms vague topics into high-quality, deliverable research reports using a systematic 8-step methodology.

## The Problem

When researching complex topics, you often face:

- **Information overload**: Too many sources, hard to distinguish quality
- **Fuzzy conclusions**: "I feel like X" instead of evidence-based reasoning
- **Missing traceability**: Can't verify where conclusions came from
- **Time-sensitivity blindness**: Using outdated information in fast-moving fields like AI

Traditional research is time-consuming, and conclusions are often unreliable.

## The Solution

Deep Research provides a **systematic 8-step methodology** that:

- **Tiered source evaluation**: L1 (official docs) > L2 (blogs) > L3 (media) > L4 (community)
- **Fact cards with citations**: Every claim traceable to its source
- **Time-sensitivity assessment**: Automatic handling of fast-changing fields
- **Verifiable conclusions**: "Fact → Comparison → Conclusion" explicit chains
- **Deliverable output**: Boss-readable reports with one-line summaries

## Requirements

- Claude Code CLI
- Web search tools (WebSearch, Tavily MCP, or Exa MCP)

## Installation

### Option 1: Git Clone (Simplest)

```bash
git clone https://github.com/wshuyi/deep-research.git
cp -r deep-research/skills/deep-research ~/.claude/skills/
```

### Option 2: Plugin Marketplace

```bash
/plugin marketplace add wshuyi/deep-research
/plugin install deep-research@wshuyi/deep-research
```

### Option 3: Third-party Marketplaces

After the repo gets 2+ stars, it will be automatically indexed by [SkillsMP](https://skillsmp.com). Search for "deep-research" there.

## Usage

Natural language triggers:

- "深度调研 [topic]" / "Deep research on [topic]"
- "帮我调研 [topic]" / "Research [topic] for me"
- "对比分析 X 和 Y" / "Compare X and Y"
- "写调研报告" / "Write a research report"

## Workflow (8 Steps)

```
Step 0: Problem type identification
Step 0.5: Time-sensitivity assessment (BLOCKING for AI/tech topics)
Step 1: Problem decomposition & boundary definition
Step 2: Source tiering & authority locking
Step 3: Fact extraction & evidence cards
Step 4: Build comparison framework
Step 5: Reference alignment
Step 6: Fact → Conclusion derivation chain
Step 7: Use case validation (sanity check)
Step 8: Deliverable formatting
```

## Output Structure

```
~/Downloads/research/<topic>/
├── 00_问题拆解.md          # Problem decomposition
├── 01_资料来源.md          # Source documentation
├── 02_事实卡片.md          # Fact cards
├── 03_对比框架.md          # Comparison framework
├── 04_推导过程.md          # Derivation process
├── 05_验证记录.md          # Validation records
└── FINAL_调研报告.md       # Final deliverable
```

## Example

```
User: 深度调研 REST API 和 GraphQL 的区别

Claude: [Executes 8-step methodology]
- Identifies as: Concept Comparison type
- Creates fact cards from official specs
- Uses 8-dimension comparison framework
- Validates with real-world scenarios
- Outputs structured report with citations
```

## Key Features

| Feature | Description |
|---------|-------------|
| **Source Tiering** | L1-L4 hierarchy ensures conclusion traceability |
| **Time-sensitivity** | Auto-detects fast-moving fields (AI, crypto, etc.) |
| **Fact Cards** | Every claim has source, confidence level, applicability |
| **Explicit Derivation** | No "I feel like" - only mechanism-based conclusions |
| **Deliverable Output** | One-line summary + structured chapters + citations |

## FAQ

**Q: How is this different from just asking Claude to research something?**

A: This skill enforces a systematic methodology with intermediate artifacts, source verification, and explicit reasoning chains. Results are traceable and verifiable.

**Q: Does it work for non-technical topics?**

A: Yes, the methodology applies to any research topic. The 5 problem types (concept comparison, decision support, trend analysis, problem diagnosis, knowledge organization) cover most use cases.

**Q: How does it handle outdated information?**

A: Step 0.5 assesses time-sensitivity. For high-sensitivity fields (AI, blockchain), it enforces 6-month time windows and requires version number citations.

## License

MIT License - see [LICENSE](LICENSE)

## Author

- **wshuyi** - [GitHub](https://github.com/wshuyi)

---

*Generated with [Claude Code](https://claude.ai/code)*
