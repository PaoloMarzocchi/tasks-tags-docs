# Charter — Tasks & Tags

## Mission
Definire un sistema minimale ma rigoroso per: (1) tracciare **task** atomici, (2) aplicarci **tag** gerarchici/relazionali, (3) esporre un'API stabile per orchestrazione e automazioni.

## Scope
- **In scope**: modelli concettuali di Task/Tag, CRUD, linking Task↔Tag, search/filtering, lifecycle degli stati, audit minimo.
- **Out of scope** (per ora): billing, auth OIDC completa, analytics avanzate, marketplace integrazioni.

## Principi
1. **SoT-first**: ogni fonte di verità vive in `tasks-tags-docs`; implementazioni devono allinearsi.
2. **Compatibilità esplicita**: versionamento semantico (`VERSION`, `docs/api.yaml.info.version`).
3. **Change control**: nessun breaking change senza ADR e bump *major*.
4. **Testing serio, semplice**: piano di test pragmatico che copre contratti API.

## Glossario (minimo)
- **Task**: unità di lavoro con `title`, `status`, `assignee?`, `due_date?`, `tags[]`.
- **Tag**: etichetta con `name`, `slug`, `parent?`, `color?`.
- **Link**: relazione N:M tra Task e Tag.

## KPI baseline
- Copertura test contratti API (happy path e principali edge).
- Zero *schema drift* tra SoT e codice.

+## Stakeholder
- **Owner**: @PaoloMarzocchi
- **Maintainers**: Core team (CODEOWNERS).

## Roadmap (alto livello)
- v1.0.0: CRUD Task/Tag, relazione Task↔Tag, search di base.
- v1.1.x: bulk operations, import/export.
- v2.0.0: breaking per advanced querying e rule engine (da ADR).