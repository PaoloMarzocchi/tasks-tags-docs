# tasks-tags-docs — Sorgente di Verità (SoT)

Questo repository contiene i **contratti** e la **documentazione** di Tasks & Tags.

## Documenti chiave
- Charter: [`/docs/charter.md`](docs/charter.md)
- OpenAPI: [`/docs/api.yaml`](docs/api.yaml)
- ADR: [`/docs/adr/`](docs/adr/)
- Process (DoR/DoD): [`/docs/process.md`](docs/process.md)
- Test Plan: [`/docs/qa/test-plan.md`](docs/qa/test-plan.md)

## Versione
La versione attuale vive in [`VERSION`](VERSION) e deve combaciare con `info.version` in `docs/api.yaml`.

## Regole
- **Nessun cambio agli schemi** senza PR su SoT + bump versione.
- Segui `docs/process.md` per DoR/DoD, SemVer e flusso PR.

## Implementazione
Il codice vive in [`tasks-tags-app`](https://github.com/PaoloMarzocchi/tasks-tags-app) ed è allineato alla versione del SoT.