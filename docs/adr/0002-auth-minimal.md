# ADR 0002 — Auth minimale (login/logout/me)
Date: 2025-08-27
Status: Accepted

## Context
La v1.0.0 del SoT non includeva endpoint di autenticazione. Per abilitare un MVP utilizzabile e roteggere CRUD Task/Tag, serve un meccanismo di auth minimale.

## Decision
- Aggiungere **3 endpoint**:
  - `POST /auth/login` con `email` e `password` ⇒ ritorna `token` bearer e `user`.
  - `POST /auth/logout` ⇒ invalida la sessione/il token.
  - `GET /auth/me` ⇒ ritorna il profilo dell'utente autenticato.
- Introdurre `securitySchemes.bearerAuth` (JWT bearer) in OpenAPI e applicare `security` sugli ndpoint (eccetto `/health` e `POST /auth/login`).
- **Version bump**: `1.0.0` → `1.1.0` (MINOR, backward compatible per consumer che non usano uth).

## Consequences
- Gli endpoint CRUD esistenti richiederanno un bearer token.
- QA deve aggiungere contract test per i 3 endpoint auth.
- FE può integrare un flusso di sessione standard.

## Alternatives Considered
- Sessioni cookie-based: scartato per MVP (più vincoli su CORS/same-site).
- OAuth/OIDC: eccessivo per lo scope di Sprint 1; si valuterà in ADR futuri.

## Rollout
1. Merge PR su SoT (questa ADR + `docs/api.yaml` + bump `VERSION`).
2. Implementazione in `tasks-tags-app` (BE/FE), con contract test verde.
3. QA esegue E2E e contratti per auth.