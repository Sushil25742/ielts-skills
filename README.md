# IELTS Claude Skills

A set of AI coaching skills for IELTS preparation, designed specifically for Claude Code. These skills are completely stateless, require no dependencies, and rely entirely on pure text prompts. Just install and start practicing!

---

## Overview

This repository includes four distinct Claude Code Skills that together form a lightweight, highly effective IELTS assistant:

| Skill Command | Functionality | Example Triggers |
|-------|------|--------|
| `/ielts` | Acts as the main router. Assesses your level and provides tailored advice. | "I want to prepare for IELTS", "IELTS" |
| `/ielts-writing` | Provides four-dimensional essay correction, rewriting comparisons, and prompt analysis. | "Correct my essay", "Look at this essay" |
| `/ielts-reading` | Extracts synonym replacements, breaks down T/F/NG logic, and diagnoses mistakes. | "Analyze reading", "Why is this wrong" |
| `/ielts-speaking` | Generates universal stories to cover the vast majority of Part 2 speaking topics. | "Speaking materials", "Part 2 prep" |

**Key Features:**
- **Stateless:** Does not save or write to local files. Every conversation is independent.
- **Zero Dependencies:** Uses pure Markdown prompts. No need for npm, Python, or a database.
- **Bilingual Interface:** Built to handle diverse language interactions while maintaining English terminology for IELTS concepts.
- **Open Source:** Released under the MIT License. Feel free to modify and adapt!

---

## Target Audience

- IELTS candidates looking for an AI practice companion.
- Developers currently using Claude Code.
- Anyone interested in learning how to write custom skills for Claude (you can use this as a template to build your own).

---

## Installation Guide

### Prerequisites
Make sure you have [Claude Code](https://docs.claude.com/en/docs/claude-code) installed on your system.

### Option 1: Direct Copy (If downloaded locally)

**Mac / Linux:**
```bash
cp -r ielts ielts-writing ielts-reading ielts-speaking ~/.claude/skills/
```

**Windows PowerShell:**
```powershell
Copy-Item -Recurse ielts, ielts-writing, ielts-reading, ielts-speaking $env:USERPROFILE\.claude\skills\
```

### Option 2: Clone & Install

```bash
git clone https://github.com/YANZHANLIN/ielts-claude-skills.git
cd ielts-claude-skills
cp -r ielts ielts-writing ielts-reading ielts-speaking ~/.claude/skills/
```

After copying the folders, restart Claude Code and type `/ielts` to begin!

---

## How to Use

### Scenario 1: General Guidance
If you aren't sure where to start, use the main router:
```text
You: /ielts
AI: (Asks about your target score, exam date, and what you want to practice today)
    → Routes you to the appropriate specialized skill.
```

### Scenario 2: Essay Correction
```text
You: /ielts-writing
    [Paste your prompt + essay]
AI:
- Scores your essay based on the four official criteria (TR / CC / LR / GRA).
- Annotates issues sentence by sentence.
- Provides a rewritten version aiming for your target score.
- Suggests priorities for improvement.
```

### Scenario 3: Reading Mistake Analysis
```text
You: /ielts-reading
    [Paste the passage + questions + your answers + correct answers]
AI:
- Breaks down the reason behind each mistake.
- Extracts a table of synonym replacements.
- Analyzes the logic for True/False/Not Given questions.
```

### Scenario 4: Speaking Preparation
```text
You: /ielts-speaking
    "Help me prepare a Part 2 response about a trip"
AI:
- Generates a 200-250 word response for Part 2.
- Predicts 4-6 follow-up questions for Part 3.
- Highlights key expressions to learn.
```

---

## Directory Structure

```text
ielts-claude-skills/
├── ielts/SKILL.md              # The main routing coach
├── ielts-writing/SKILL.md      # Writing correction module
├── ielts-reading/SKILL.md      # Reading analysis module
└── ielts-speaking/SKILL.md     # Speaking material generator
```
"Inspired by the original Chinese version by YANZHANLIN"
