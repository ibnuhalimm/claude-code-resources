---
description: Generate a commit
argument-hint: [task-id]
model: haiku
allowed-tools: Bash(git branch:*), Bash(git diff:*)
---

## Your Task
Follow best practices to write clear and concise commit messages that accurately describe the changes made in the codebase. Explain what and why, not how.
Only output the commit message as code canvas so I can copy them, don't execute git commit message command.

## Context
- Current git diff (staged): !`git diff --cached`
- Current branch: !`git branch --show-current`

## Custom Instructions
1. Analyze the staged changes in the codebase
2. Commit message must follow these rules:
  - Start with a type (feat/fix/docs/chore/refactor) according your judgement of the changes
  - Understand the code changes and summarize under 150 characters
  - Use present tense and imperative mood
  - Add task number #$ARGUMENTS at the end or added by you if I'm not provided the [task-id] based on current branch name
  - Provide a short detailed description of the change in the next two lines bellow the title
  - If it's a massive or drastical logic code changes, add minimum 2 and maximum 5 detailed bullet points explaining the change. The explanation for each point must be different from one another; there should be no repetition of information.
