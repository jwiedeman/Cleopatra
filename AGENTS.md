# Repository Guidelines

- This repository is a private workspace for Universal Music Group (UMG) initiatives. Handle all data and credentials securely and avoid committing secrets.
- Maintain the directory structure documented in the README. Place automation assets under `automated_testing/`, shared SQLite resources under `db/`, research materials under `research/`, specifications under `spec/`, analytics tooling under `google_api/`, and reports under `reports/`.
- All tooling that persists structured data must use the shared SQLite database file inside `db/`. Do not create duplicate database files elsewhere; instead, extend the schema within the shared database.
- Update `README.md` and other documentation whenever you add new tooling or change repository conventions to keep collaborators aligned.
- Follow descriptive naming and include inline comments where necessary to clarify non-obvious logic. Keep scripts idempotent when feasible to support automation.
