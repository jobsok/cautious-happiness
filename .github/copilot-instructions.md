<!-- Auto-generated guidance for AI coding agents. Ask the repo owner before making large changes. -->
# Copilot instructions for this repository

Purpose
- Give AI coding agents the minimal, actionable context needed to start contributing to this repository.

Repository snapshot
- This repository is currently minimal: see [LICENSE](LICENSE) for an existing file. No source code or manifests (package.json, pyproject.toml, go.mod, etc.) were found at the time this guidance was generated.

What to do first
- If you are an agent assigned to work here, stop and ask the user these clarifying questions before changing code:
  - What language(s) and framework(s) should this repo use?
  - Is there an existing CI/CD workflow or preferred linters/test runners?
  - Are there example projects or design docs to mirror?

Repository exploration checklist (run these in the repo root)
```powershell
# list top-level files
Get-ChildItem -Force | Sort-Object Name

# quick language/manual detection (look for these files)
Test-Path package.json; Test-Path pyproject.toml; Test-Path requirements.txt; Test-Path go.mod; Test-Path Cargo.toml; Test-Path Dockerfile
```

How to make safe changes
- Do not add or modify production code until the user confirms the intended language and project layout.
- When the user confirms a language, create a minimal scaffold (hello-world or tests) and ask for review.

What to add when code appears
- If you find `package.json`: follow npm/yarn scripts and run `npm test` / `npm run build` to learn the tooling.
- If you find `pyproject.toml` or `requirements.txt`: run the project's tests with `pytest` after creating a venv.
- If you find `go.mod`: run `go test ./...` and `go vet`.

Conventions for agents (repo-specific notes)
- No project-specific conventions were discoverable. Prefer the following common, easily-reviewable layouts when scaffolding until told otherwise:
  - Python: `src/` for packages, `tests/` for tests, `pyproject.toml` for build tooling
  - Node: `src/` + `package.json` scripts, `jest` or `vitest` for tests
  - Go: `cmd/` for binaries, `internal/` for private packages

When you are unsure
- Ask before large changes. Provide a 1–2 file proof-of-concept or a small test and request a quick user review.

References
- Existing file snapshot: [LICENSE](LICENSE)

If this guidance is incomplete, tell me what additional repository files you expect and I will re-run discovery and update this file.
