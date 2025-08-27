# Process

Questo file definisce DoR/DoD, flow PR e regole di versioning per Tasks & Tags.

## Definition of Ready (DoR)
- Obiettivo chiaro e *scoped* (1 feature o fix).
- Impatto sui contratti (OpenAPI, schemi) esplicitato.
- Test di accettazione elencati (happy path + edge principali).
- ADR richiesti identificati (se decisionali).

## Definition of Done (DoD)
- Codice + test passano localmente e in CI.
- Documentazione aggiornata (SoT + eventuale README app).
- Se tocca **schemi/API**:
  - Bump coerente in `VERSION` e `docs/api.yaml.info.version`.
  - CHANGELOG aggiornato.
  - Nuovi test contratti.

## Policy “Nessun cambio agli schemi senza PR su SoT + bump versione”
1. Ogni modifica a `docs/api.yaml` o ad altri schemi richiede **PR su `tasks-tags-docs`**.
2. La PR deve:
   - Aggiornare `VERSION` e `docs/api.yaml.info.version`.
   - Aggiornare `CHANGELOG.md`.
   - Citare l’ADR se breaking.
3. Solo dopo merge su SoT, l’implementazione può essere adeguata in `tasks-tags-app`.

## Flusso PR sintetico
1. **Issue** con DoR.
2. **Branch** feature: `feat/<slug>` o `fix/<slug>`.
3. **PR SoT** (se cambia schema/API): revisione CODEOWNERS.
4. **PR App**: implementazione coerente con SoT versionato.

## Testing
Rimando a `docs/qa/test-plan.md` per il piano; qui resta la checklist DoD.

## SemVer
- **MAJOR**: breaking (rimozioni/rename campi, risposte incompatibili).
- **MINOR**: nuove feature retrocompatibili.
- **PATCH**: bugfix/documentazione.