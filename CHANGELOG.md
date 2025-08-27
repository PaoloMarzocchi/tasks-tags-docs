# Changelog

All notable changes to this project will be documented in this file.

## [1.0.0] - 2025-08-27
### Added
- Initial SoT bootstrap:
  - `docs/charter.md`
  - `docs/process.md` (con DoR/DoD)
  - `docs/api.yaml` (OpenAPI 3.0 stub, version 1.0.0)
  - `docs/adr/0001-sot-and-versioning.md`
  - `docs/qa/test-plan.md`
- Guardrails:
  - `.github/workflows/verify-version-and-schemas.yml`
  - `.github/PULL_REQUEST_TEMPLATE.md`
  - `.github/CODEOWNERS`

+### Policy
- Nessun cambio agli schemi senza PR su SoT + bump versione (major/minor/patch in `VERSION` e `docs/api.yaml.info.version`).

[1.0.0]: https://github.com/PaoloMarzocchi/tasks-tags-docs/releases/tag/v1.0.0