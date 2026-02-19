---
description: "GitHub Agentic Workflow Test"
name: "Agentic Workflow Test"
on:
  workflow_dispatch:
engine: copilot
safe-outputs:
  create-issue:
    expires: 2d
    title-prefix: "[Parent] "
    max: 5
    group: true
---

# Test GitHub Agentic Workflow

## Instructions

1. Investigate the project structure and files.
2. Create an issue and write a summary of the project.
