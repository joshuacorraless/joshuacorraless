<p><img src="assets/tec-emprende-lab.png" alt="TEC Emprende Lab" width="160"></p>

# Engineering contributions at TEC Emprende Lab

**Joshua Corrales Retana · Software Development Assistant · July 2026–present**

I work on internal applications at TEC Emprende Lab, part of Instituto Tecnológico de Costa Rica. This page describes my contributions to shared projects and links to the corresponding code reviews. It is a personal work record, not official project documentation.

## Course platform

The platform manages participants and course assignments using React, Flask and Supabase.

### Preventing partial saves

Participant fields and course assignments previously passed through separate persistence operations. I contributed transactional PostgreSQL updates, validation and regression tests so related changes commit or roll back together. I also corrected interface flows that could report success before persistence completed.

[Persistence changes — PR #4](https://github.com/TEC-Emprende-Lab/Plataforma-de-Cursos/pull/4)

### Security controls

I strengthened authentication and SVG handling through Supabase JWT validation, sanitization, upload limits and automated security tests.

[Security changes — PR #2](https://github.com/TEC-Emprende-Lab/Plataforma-de-Cursos/pull/2)

## SIA

SIA is an internal platform for tracking entrepreneurship projects. Its application roles cover coordination, project management and entrepreneurs.

### Data model and background jobs

I documented the entity–relationship model against the existing migrations, separating implemented constraints from pending decisions. I then implemented a PostgreSQL queue foundation with idempotency keys, delayed retries and atomic job claims, supported by migration-backed tests.

[Data model — PR #8](https://github.com/TEC-Emprende-Lab/SIA/pull/8) · [Queue foundation — PR #14](https://github.com/TEC-Emprende-Lab/SIA/pull/14)

### Reports and human approval

I added FastAPI endpoints for report drafts, edits, explicit human approval and corrected versions. Approved content is preserved, and approval queues a PDF job within the transaction.

The backend includes a consumer function, but the default PDF renderer/storage and deployable worker integration remain incomplete. This work establishes the report workflow and queue integration; it does not claim a finished PDF delivery service.

[Report APIs — PR #15](https://github.com/TEC-Emprende-Lab/SIA/pull/15)

## Collaboration

I proposed a modular architecture, gained support for its adoption and presented technical decisions to the team. I also proposed consolidating services distributed across Render and Supabase accounts. The platforms are team projects; the linked pull requests identify the scope of my recorded contributions.

The source repositories contain the implementation, current status and licensing information.

[Back to profile](../../README.md)
