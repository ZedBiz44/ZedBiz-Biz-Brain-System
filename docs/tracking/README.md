# Technical Tracking Workflow

Date: 2026-06-23 | Author: Cody | Status: Draft

## Purpose

This folder keeps the durable technical tracking record for the ZedBiz Biz Brain system.

## What Goes In GitHub

Use GitHub for technical details that future agents or developers need:

- Issues and bugs
- Fixes and troubleshooting notes
- Config, prompt, and setup changes
- Infrastructure and deployment notes
- Technical decisions
- Reusable operating rules

## What Goes In Notion

Use Notion for business-readable operating notes:

- Daily journal records
- Strategy and planning
- Plain-English summaries
- Business impact
- Decisions that need human review

## How To Log Work

For technical updates:

- Add a GitHub issue using the `Technical Update` template when the update should be visible in issue tracking.
- Add a short entry to [technical-updates.md](technical-updates.md) when the update should be part of the durable log.
- Add a Notion `Tech Updates` journal record for the daily business-facing summary.

For technical problems:

- Add a GitHub issue using the `Technical Issue` template.
- Add a summary to [technical-issues.md](technical-issues.md) when the issue needs a durable troubleshooting trail.
- Close the issue only after the fix has been verified in the real surface where the problem appeared.

## Verification Standard

A technical update is not done until:

- The changed file, issue, page, or service was checked directly.
- The result was recorded in GitHub.
- The user-facing outcome is clear in plain language.
