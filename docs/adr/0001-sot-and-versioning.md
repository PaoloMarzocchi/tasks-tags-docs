# ADR 0001 — SoT + Versioning & Change Control
Date: 2025-08-27
Status: Accepted

## Context
Serve una politica chiara per evitare drift tra documentazione e codice. Ogni modifica a schemi/PI deve essere tracciata e versionata.

## Decision
- La **Sorgente di Verità** per contratti (OpenAPI) vive in `tasks-tags-docs`.
- Ogni modifica agli schemi richiede PR su SoT e **bump** coerente (SemVer) in `VERSION` e `docs/pi.yaml.info.version`.
- Breaking change ⇒ bump **MAJOR** e ADR dedicato.
- La CI blocca PR che toccano `docs/api.yaml` senza bump di versione.

## Consequences
- Maggiore disciplina nel rilascio.
- Sincronizzazione esplicita con `tasks-tags-app`.
- Overhead minimo ma salutare (PR + CHANGELOG).