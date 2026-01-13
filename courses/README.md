# Automation Starter — Evidence-Based Notes

This directory contains structured notes and observations from the
**UiPath Automation Starter** course.

Notes are written **after completing each module** and focus on:
- Core concepts
- One concrete example
- Documentation gaps or ambiguity
- Integration assumptions (if any)

---

## Course Metadata

- **Provider:** UiPath Academy
- **Format:** Video + Studio Web labs
- **Intent:** Introduce automation concepts and cloud-based RPA execution

---

## Progress Status

| Module | Status | Evidence |
|------|-------|----------|
| Introduction to Automation | ✅ Completed | Daily Log Day 01 |
| UiPath Studio Web | 🟨 In progress | Days 02–06 |
| Agentic Automation | ⬜ Not started | — |
| Prompt Engineering | ⬜ Not started | — |

---

## Notable Findings

### Studio Web Lab Constraints
- Assumes Microsoft ecosystem (OneDrive / Excel Online)
- Google Workspace introduces connector and file-handling limitations
- Folder-based workflows are not universally supported

These constraints were not clearly documented in the course material and
were discovered through execution failures.

---

## Evidence Index

- OAuth failure (Day 02):
  - `assets/day-02/oauth-403-error.png`
  - `assets/day-02/raw-error.json`

- Google Drive limitation (Day 06):
  - `assets/day-06/gdrive-folder-download-error.txt`

---

## Documentation Gaps Identified

- Lack of explicit environment assumptions
- No warning about Google Drive folder limitations
- OAuth consent steps insufficiently emphasized

These gaps informed later documentation judgment during external contributions.

---

## Notes

This course is treated as **input**, not authority.
Observed behavior during execution takes precedence over advertised workflows.
