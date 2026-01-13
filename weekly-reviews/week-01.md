# Week 01 Review — Integration Boundaries & First Contact with Open Source
**Period:** 2026-01-06 → 2026-01-12  
**Status:** 🟥 Failure → 🟩 Recovery  
**Theme:** Systems fail at boundaries, not at intent

---

## Executive Summary

Week 01 focused on establishing a disciplined “learning-in-public” workflow and
encountering real-world system failures early.

Two independent failures occurred during UiPath labs:
- OAuth permission failure (Day 02)
- Google Drive file handling limitation (Day 06)

Instead of forcing workarounds, the failures were documented, analyzed, and
reframed using reliability engineering principles. The week concluded with a
validated external open-source contribution attempt.

---

## What Went Wrong (By Design)

### 1. OAuth Boundary Failure (Day 02)
- **Symptom:** HTTP 403 during Google Sheets provisioning
- **Root cause:** Missing OAuth consent at integration boundary
- **Lesson:** Permissions are a first-class dependency, not a setup detail

**Evidence:**
- Raw error JSON: `assets/day-02/raw-error.json`
- Screenshot: `assets/day-02/oauth-403-error.png`
- Source log:  
  https://github.com/dmurthy-dev/learning-in-public/blob/main/daily-logs/2026-01-07-day-02.md

---

### 2. Google Drive Folder Limitation (Day 06)
- **Symptom:** Studio Web could not download Google Drive folders
- **Root cause:** Connector supports files only, not folders
- **Lesson:** Templates encode hidden environment assumptions

**Evidence:**
- Raw error log: `assets/day-06/gdrive-folder-download-error.txt`
- Referenced in:  
  https://github.com/dmurthy-dev/learning-in-public/blob/main/daily-logs/2026-01-11-day-06.md

---

## Recovery & Reframing

Instead of retrying labs blindly, I shifted focus to:
- Reliability engineering
- Latent failure models
- Integration boundary analysis

Primary reference:
- *How Complex Systems Fail* — Dr. Richard I. Cook

This reframing directly informed how I approached documentation, tooling,
and open-source contribution decisions.

---

## External Contribution Outcome

### Repository
- **Project:** 1Password Kubernetes Operator
- **Issue:** https://github.com/1Password/onepassword-operator/issues/206
- **PR:** https://github.com/1Password/onepassword-operator/pull/234

### Result
- PR closed unmerged
- Maintainer confirmed issue was outdated and already resolved
- Contribution attempt explicitly acknowledged and appreciated

**Evidence:**
- Commit: `d774112`
- Screenshot: `assets/day-08/pr-234-maintainer-closure.png`

---

## Engineering Signals Demonstrated

- Correct issue triage
- Avoidance of redundant documentation changes
- Respect for maintainer time
- Evidence-backed documentation
- Professional open-source communication

---

## Key Insight of the Week

> Systems fail structurally, not personally.

Failures exposed *assumptions*, not incompetence.  
Documentation exists to surface those assumptions before users hit them.

---

## Week 02 Intent

- Shift from analysis → repeatable external contributions
- Target documentation-only PRs with clear freshness and scope
- Continue evidence-first documentation discipline

 ---
 ## 🤖 AI Disclosure
This review was written by me with assistance from AI tools for clarity, structure, and editing.
All technical decisions, code changes, and validations were performed and verified by me.
--- 
