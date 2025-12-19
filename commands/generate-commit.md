---
description: Generate a commit
argument-hint: [task-id]
model: sonnet
allowed-tools: Bash(git status:*), Bash(git log:*), Bash(git branch:*), Bash(git diff:*)
---

## Your Task
Follow best practices to write clear and concise commit messages that accurately describe the changes made in the codebase.
Only output the commit message as code canvas so I can copy them, don't execute git commit message directly.

## Context
- Current git status: !`git status`
- Current git diff (staged): !`git diff --cached`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10`

## Custom Instructions
1. Analyze the staged changes in the codebase
2. Commit message must follow these rules:
  - Start with a type (feat/fix/docs/chore) according your judgement of the changes
  - Keep the commit title under 100 characters
  - Add task number #$ARGUMENTS at the end or added by you if I'm not provided the [task-id] based on current branch name
  - Provide a short description of the change in the next two lines bellow the title
  - If it's a massive or drastical logic code changes, add minimum 2 and maximum 5 detailed bullet points explaining the change
  - Use imperative mood
