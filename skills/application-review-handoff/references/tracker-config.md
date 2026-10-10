# Private tracking configuration

Store this configuration only in the user's private workspace, outside the public skill package. Resolve the user-provided path; do not guess a personal folder or search unrelated private files. The values below are deliberately invalid synthetic placeholders, not usable Google Sheets IDs.

```yaml
application_tracker:
  spreadsheet_id: "SYNTHETIC_MAIN_SHEET"
  gid: "42"
  spreadsheet_title: "Synthetic application tracker"
  tab_title: "Applications"
  columns:
    company: "Company"
    role_id: "Role ID"
    status: "Status"
    evidence: "Evidence"
    material_version: "Materials"
    next_action: "Next action"
    submitted_at: "Submitted at"
```

These are semantic column mappings, not fixed column letters. Read the actual header row before determining a write range. Additional fields may be mapped when present; do not create columns or change the schema without authorization.

Precedence: latest explicit user designation → compatible private configuration → no resolved target. Historical selection lists are not fallback trackers. A new explicit target invalidates the old target but does not remove the need to read new metadata, resolve its tab and map its columns. If the same target has unexpected metadata, stop writes and resolve the mismatch.

No spreadsheet access or write permission is supplied by this example. Never copy a real user's configuration into the public repository.
