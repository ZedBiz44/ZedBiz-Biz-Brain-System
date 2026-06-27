# Technical Updates

Date: 2026-06-23 | Author: Cody | Status: Draft

## 2026-06-23

### GitHub Tracking Setup

- Connected the ZedBiz Biz Brain system technical tracking workflow to `ZedBiz44/ZedBiz-Biz-Brain-System`.
- Added repo-level agent instructions in `AGENTS.md`.
- Added technical tracking docs under `docs/tracking/`.
- Added GitHub issue templates for technical issues and updates.
- Kept Notion as the daily journal and business-readable operating layer.

### Verification

- Confirmed the local starting folder was not a Git checkout.
- Confirmed the target GitHub repository was reachable and empty before setup.
- Confirmed the Notion `Technical Documentation` page contains the inline `Tech Updates` database.

## 2026-06-24

### Notion Z-Knowledge Architecture Review

- Reviewed the Notion `Notion-AI-BizBrain-Architecture-Plan` and `Notion-Folder-Structure` pages.
- Prepared feedback for the `Cody-Z-Knowledge-Feedback` Notion page.
- Main review themes: keep folder pages as dashboards, use shared master databases as the system backbone, normalize folder codes before buildout, add source-of-truth rules, add permission and sensitivity controls, and pilot one folder group before broad rollout.
- Confirmed the current folder structure database already has useful starter fields: `Name`, `Top Level Folder Category`, `Short Description`, `Long Description`, and `Example`.

### Notion Folder Code Cleanup

- Updated the architecture plan to use the current folder-code pattern: `Z1AM`, `Z1ZC`, `Z1ZP`, `ZMMS`, `ZCGZ`, `ZCGG`, `ZCRD`, and `ZZZR`.
- Changed `Core Initiatives` to `Core Ventures` where it referred to the Core Venture group.
- Updated the Notion Folder Structure database select option from `Core Initiatives` to `Core Ventures`.
- Updated the five Core Venture database rows to use `Core Ventures`.
- Standardized Resort Directories on `ZCRD-Resort-Directories`.
- Fixed the `Administrative` spelling error in the architecture plan.

### Notion Folder Structure Governance Fields

- Added operating fields to the Notion `Notion Folder Structure` database: `Folder Code`, `Official Name`, `Dashboard Page`, `Purpose`, `Google Drive Link`, `Owner`, `Review Cycle`, `Status`, `Sensitivity`, `Source`, `Related Master Databases`, `What Belongs Here`, and `What Does Not Belong Here`.
- Renamed `Top Level Folder Category` to `Top Level Category` to match the requested field naming while preserving the existing category values.
- Added controlled select options for `Review Cycle`, `Status`, `Sensitivity`, `Source`, and `Related Master Databases`.
- Added `Review Cycle` once because it appeared twice in the field request.

## 2026-06-27

### Z-Knowledge Page Research Templates

- Reviewed the Notion Z-Knowledge planning pages:
  - `Notion-AI-Z-Knowledge-Plan`
  - `Notion-Z-Knowledge-Folder-Structure`
  - `Notion-Z-Knowledge-Core-Databases`
- Reviewed the Notion `Page/Research-Templates` page and `Research-Template-Guide`.
- Updated the `Research-Template-Guide` with:
  - Compact, Standard, and Deep Page Research levels.
  - Z-Knowledge database-alignment rules.
  - Single-item versus collection rules, especially for marketing swipes and file/reference collections.
  - Expanded database-ready field guidance for new page types.
  - Template-specific guidance for services, offers, marketing content, campaigns, marketing ideas, templates, marketing swipes, research pages, and external files.
- Populated the blank additional Page/Research templates in Notion:
  - `Services-Page-Research-Template`
  - `Offers-Page-Research-Template`
  - `Marketing-Content-Page-Research-Template`
  - `Campaigns-Page-Research-Template`
  - `Marketing-Ideas-Page-Research-Template`
  - `Templates-Page-Research-Template`
  - `Marketing-Swipes-Page-Research-Template`
  - `Research-Page-Research-Template`
  - `External-File-Page-Research-Template`
- Created the Notion Tech Updates journal record: `2026-06-27 | Cody | Z-Knowledge Page Research Templates Completed`.
- Confirmed this repository is the correct GitHub technical record: `ZedBiz44/ZedBiz-Biz-Brain-System`.
- Added page icons to the created/completed research-template pages for easier scanning in Notion.
- Added icons to the `Research-Template-Guide` and the related Notion Tech Updates journal record.

### Verification

- Fetched the updated `Research-Template-Guide` in Notion and confirmed the new guide sections are present.
- Fetched the updated `Marketing-Swipes-Page-Research-Template` and confirmed the compact template content is present.
- Confirmed the local repo remote points to `https://github.com/ZedBiz44/ZedBiz-Biz-Brain-System.git`.

### Support Doc Ingestion SOP + Skill -- Review, Refinement, and Notion Update
- Reviewed all three Support Documentation Ingestion SOPs (Grok, Cody, Ruby versions) and selected Cody's as the strongest foundation.
- Applied the following refinements to Cody's SOP (Notion: `Support-Doc-Ingestion-SOP`):
  - Flat file naming convention: `{folder}/{toolname}_{topic}.md` -- no nested tool sub-folders inside wiki sections.
  - Context7 moved to first check in the source priority order; official docs remain the authority.
  - Source priority reframed as a 4-tier table: Context7 (1st), Official Docs (2nd), PDFs (3rd), Supplemental (4th).
  - 70/20/10 source mix described as a planning target, not a rigid rule.
  - Ingestion workflow restructured: Option A+B as the default combined path, Option C (Manual Curation) as a defined fallback with explicit use cases.
  - Docker Alpine chown workaround removed -- not relevant to this process.
  - Transfer section clarified: same-VPS uses `cp -a` (per-folder full bundle), cross-VPS uses `rsync` over SSH (per-folder full bundle).
  - `.openclaw-wiki/cache/` exclusion added to Operating Rules and Transfer section.
  - Verify Wiki Context step added to the Ordered SOP.
  - Required Transfer Record added to GitHub Tracking Model with full field list.
  - Completion Gate updated to include wiki context verification and receiving-agent test.
  - Refresh rule added: flag docs older than 6 months, re-research on major version release.
  - Real task-style test template added with exact question format.
  - Frontmatter status field expanded to: `draft | review | verified | partial | stale | deprecated`.
- Reviewed the OpenClaw `Support-Doc-Ingestion-Skill` (Notion: `Support-Doc-Ingestion-Skill`).
  - Confirmed skill is in sync with the updated SOP on all structural and technical content.
  - Identified two remaining gaps in the SOP vs. the skill: "When To Stop And Ask" section (missing from SOP) and Quick Reference block (nice-to-have).
- Architecture decisions confirmed:
  - Individual agent wiki paths: `/opt/openclaw/shared/knowledge/{agent}/wiki`
  - Shared main wiki is NOT used for tool documentation.
  - GitHub `docs-research-log/` structure is the index and tracking layer only.
  - Same-VPS transfers: `cp -a`. Cross-VPS transfers: `rsync -av --progress` over SSH.

### Verification
- Fetched the updated `Support-Doc-Ingestion-SOP` from Notion and confirmed all revised sections are present.
- Fetched the `Support-Doc-Ingestion-Skill` from Notion and confirmed the gap analysis is accurate.
- Confirmed this repository is the correct GitHub technical record: `ZedBiz44/ZedBiz-Biz-Brain-System`.

### Research Process SOP Evergreen Cleanup

- Checked the live Notion `Research-Process-SOP` against the requested dual-channel research workflow improvements.
- Confirmed the SOP now requires both channels: OpenClaw Memory Wiki for agent-readable Markdown and Notion Z-Knowledge Core Master Databases for human-readable operations.
- Replaced dated/agent-specific framing with evergreen operating language owned by ZedBiz Ops.
- Added the exact VPS1 shared wiki route: `/opt/openclaw/shared/knowledge/wiki`.
- Added the VPS2 personal workspace wiki route pattern and scheduled rsync handoff language.
- Added the ZedBiz wiki frontmatter lint requirement, including `zedbiz-wiki-lint-inner.sh` when it is the active enforcement script.
- Cleaned the recommended prompt so assignment instructions and completion-report requirements are separated.
- Added the official Core-Master-Databases page as the Notion routing index for selecting the correct Core Master Database before creating or updating research records.
- Created the Notion Tech Updates journal record: `2026-06-27 | Cody | Research Process SOP Evergreen Cleanup`.

### Verification

- Fetched the updated `Research-Process-SOP` from Notion and confirmed the dual-channel rule, wiki routing, Notion track, frontmatter alignment, and success standard are present.
- Confirmed the Core-Master-Databases routing-index instruction appears in the main Notion channel section, the recommended assignment prompt, and the human review check.
- Confirmed no named agent troubleshooting history remains in the SOP body; only system-level references such as OpenClaw Memory Wiki, VPS1, and VPS2 remain where needed.
- Confirmed the local tracking repo remote points to `https://github.com/ZedBiz44/ZedBiz-Biz-Brain-System.git`.
