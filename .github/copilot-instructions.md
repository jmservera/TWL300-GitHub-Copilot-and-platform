# Copilot instructions for this repository

## Core source-of-truth rules

- Treat Confluence as the source of truth for project documentation, meeting transcripts, BRDs, PRDs, and ADRs.
- Read the relevant Confluence pages through Atlassian MCP before drafting, changing, or implementing requirements or architecture decisions.
- Use meeting transcripts stored in Confluence as the starting evidence for BRD and PRD creation.
- Distinguish recorded decisions from assumptions. Clearly label assumptions when evidence is incomplete.
- Preserve the source page URL, page ID, and version in any generated artifact that cites Confluence content.
- Publish approved BRDs, PRDs, ADRs, and durable documentation to Confluence.
- Repository drafts are working artifacts only and are not authoritative unless a Confluence page explicitly identifies them as such.

## Delivery and work tracking

- Treat Jira as the source of truth for work items and delivery status.
- Every commit message and pull request title must include the relevant Jira issue key, such as PROJ-123, so GitHub for Jira links development activity to the work item.
- Every pull request description must include:
  - a direct link to the Jira work item
  - links to the relevant supporting Confluence pages
- Do not create an untracked commit or pull request.
- If no Jira issue is available, ask for the Jira issue before proceeding with GitHub work.

## Evidence, verification, and review

- Do not invent missing source material.
- Do not claim a Confluence, Jira, or GitHub operation succeeded unless tool evidence confirms it.
- Ask for clarification when authoritative information is missing or conflicting.
- Require human review before publishing documentation or mutating Jira.
- Never place credentials, API tokens, secrets, or sensitive environment values in instructions, prompts, commit messages, or chat.

## Working expectations for Copilot agents

- Prefer evidence from Confluence and Jira over informal assumptions or local memory.
- When a requirement or architectural decision is changed, trace it back to the source Confluence page before editing the repository.
- When creating or updating artifacts in the repository, treat them as drafts unless the relevant Confluence page explicitly marks them as approved or authoritative.
- If a source dependency cannot be verified, say so plainly and request the missing source material.

## Copilot tracking artifacts

- Keep `.copilot-tracking/` and all files beneath it available for version control.
- Do not add `.copilot-tracking/` or any of its contents to `.gitignore`, `.git/info/exclude`, or other ignore rules.
- Apply the repository's data handling and secret-management requirements to all tracked artifacts.
