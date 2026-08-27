---
name: update-github-info
on:
  schedule: daily
  workflow_dispatch:
permissions:
  contents: read
  issues: read
  pull-requests: read
engine: copilot
model: claude-haiku-4.5
network:
  allowed:
    - github.blog
    - github.com
    - awesome-copilot.github.com
tools:
  github:
    toolsets: [default, repos]
  web-fetch:
  edit:
safe-outputs:
  create-pull-request:
    draft: true
    labels: [automation]
    title-prefix: "[github-info] "
---

# Update GitHub Info

Keep `site/content/github-info.md` current for Mona's review.

1. Read `notes/mona-notes.md` before making any changes.
2. Use the GitHub repository API tools to read repository guidance or reference files. Do not use terminal, CLI, or sandboxed commands for that repository reading.
3. Web fetch `https://github.blog/latest/`, `https://github.blog/changelog/`, and `https://awesome-copilot.github.com/workflows/`.
4. Identify useful, recent updates for developers. Prefer short, practical summaries and mention the source for every update.
5. Update only `site/content/github-info.md`, preserving its existing structure and removing stale or superseded information when appropriate.
6. Review the resulting diff for accuracy, clarity, and unintended changes.
7. Open one draft pull request with the `create-pull-request` safe output for Mona to review. Include a concise title and body that summarize the sourced updates and link to the GitHub Blog or Changelog sources.

Do not write directly to the default branch, publish changes outside the pull request, or create a pull request when there are no meaningful updates.