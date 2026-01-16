---
description: Create a PR description
argument-hint: [context]
model: haiku
allowed-tools: Bash(git branch:*), Bash(git log:*)
---

## Tools
- Current branch name: !`git branch --show-current`
- List committed message: !`git log`

## Your Task
Your role as senior software developer.
Put the $ARGUMENTS [context] as additional context to write clear, concise, and developer friendly pull request description.
Only output the commit message as markdown-friendly format, so I can copy them, don't execute git commit message command.

## Custom Instructions
1. List the commit history on current working branch
2. Make a pull request description which consists of the following parts:
  - Summary : contains one sentence explaining the summary of the changes and what has been fixed in the related issue.
  - What's changed : contains list of changes according to the committed message. Don't list each file changes, summarize them. Write clear, concise, and developer-friendly sentences under 250 characters of each item.
    If there's a need to refer a file, no need to mentioned full path of the file, just mention the filename.
  - Test Coverage : list of what added and changed component or e2e tests (if exists). Each item must contains file name of .cy.ts file, and summarize how many test cases what it's covered.
3. Wrapped the mentioned filename, class, or function with ` character.
