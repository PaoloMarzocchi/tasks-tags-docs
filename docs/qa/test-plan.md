# Test Plan — v1.0.0

## Obiettivi
Verificare i contratti API minimi per Task/Tag e le regole di compatibilità.

## Scope Test
- Endpoint: `/health`, `/tasks`, `/tasks/{id}`, `/tags`, `/tags/{id}`.
- Validazioni schema (tipi, enum, required).
- Ricerca e filtri basilari.

## Strategia
1. **Contract tests** contro `docs/api.yaml`.
2. **Happy path** CRUD Task/Tag.
3. **Edge**:
   - `status` fuori enum ⇒ 400.
   - `parent_slug` inesistente ⇒ 422.
   - Delete su ID inesistente ⇒ 404.

## Casi (minimo)
- Tasks:
  - Create (solo title) ⇒ 201.
  - Update `status` ⇒ 200.
  - List con `q`, `tag`, `status`.
- Tags:
  - Create parent, poi child con `parent_slug`.
  - Update rename `name`, conferma `slug` invariato (no breaking).

## Non-Functional (smoke)
- /health ⇒ 200 in < 100ms su env locale.

## Uscite
- Report contract test (pass/fail).
- Log incompatibilità con versione attesa.
# Test Plan — v1.0.0

## Obiettivi
Verificare i contratti API minimi per Task/Tag e le regole di compatibilità.

## Scope Test
- Endpoint: `/health`, `/tasks`, `/tasks/{id}`, `/tags`, `/tags/{id}`.
- Validazioni schema (tipi, enum, required).
- Ricerca e filtri basilari.

## Strategia
1. **Contract tests** contro `docs/api.yaml`.
2. **Happy path** CRUD Task/Tag.
3. **Edge**:
   - `status` fuori enum ⇒ 400.
   - `parent_slug` inesistente ⇒ 422.
   - Delete su ID inesistente ⇒ 404.

## Casi (minimo)
- Tasks:
  - Create (solo title) ⇒ 201.
  - Update `status` ⇒ 200.
  - List con `q`, `tag`, `status`.
- Tags:
  - Create parent, poi child con `parent_slug`.
  - Update rename `name`, conferma `slug` invariato (no breaking).

## Non-Functional (smoke)
- /health ⇒ 200 in < 100ms su env locale.

## Uscite
- Report contract test (pass/fail).
- Log incompatibilità con versione attesa.
# Test Plan — v1.0.0

## Obiettivi
Verificare i contratti API minimi per Task/Tag e le regole di compatibilità.

## Scope Test
- Endpoint: `/health`, `/tasks`, `/tasks/{id}`, `/tags`, `/tags/{id}`.
- Validazioni schema (tipi, enum, required).
- Ricerca e filtri basilari.

## Strategia
1. **Contract tests** contro `docs/api.yaml`.
2. **Happy path** CRUD Task/Tag.
3. **Edge**:
   - `status` fuori enum ⇒ 400.
   - `parent_slug` inesistente ⇒ 422.
   - Delete su ID inesistente ⇒ 404.

## Casi (minimo)
- Tasks:
  - Create (solo title) ⇒ 201.
  - Update `status` ⇒ 200.
  - List con `q`, `tag`, `status`.
- Tags:
  - Create parent, poi child con `parent_slug`.
  - Update rename `name`, conferma `slug` invariato (no breaking).

## Non-Functional (smoke)
- /health ⇒ 200 in < 100ms su env locale.

## Uscite
- Report contract test (pass/fail).
- Log incompatibilità con versione attesa.
# Test Plan — v1.0.0

## Obiettivi
Verificare i contratti API minimi per Task/Tag e le regole di compatibilità.

## Scope Test
- Endpoint: `/health`, `/tasks`, `/tasks/{id}`, `/tags`, `/tags/{id}`.
- Validazioni schema (tipi, enum, required).
- Ricerca e filtri basilari.

## Strategia
1. **Contract tests** contro `docs/api.yaml`.
2. **Happy path** CRUD Task/Tag.
3. **Edge**:
   - `status` fuori enum ⇒ 400.
   - `parent_slug` inesistente ⇒ 422.
   - Delete su ID inesistente ⇒ 404.

## Casi (minimo)
- Tasks:
  - Create (solo title) ⇒ 201.
  - Update `status` ⇒ 200.
  - List con `q`, `tag`, `status`.
- Tags:
  - Create parent, poi child con `parent_slug`.
  - Update rename `name`, conferma `slug` invariato (no breaking).

## Non-Functional (smoke)
- /health ⇒ 200 in < 100ms su env locale.

## Uscite
- Report contract test (pass/fail).
- Log incompatibilità con versione attesa.