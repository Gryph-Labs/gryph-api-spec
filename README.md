# Gryph API Specification

This repository contains the versioned OpenAPI specification for the Gryph Labs Phoenix API.

## Branching model

The active major API version is the default branch for this repository.

- `v1` — active version 1 specification
- Feature branches use `feature/<Jira issue key>`, for example `feature/PHX-2`
- Changes are merged into the active version branch through pull requests
- Future breaking API versions will use new major-version branches such as `v2`

## Specification structure

Human-maintained OpenAPI source lives under `src/`. Redocly validates and bundles that modular source into `gryph-api-spec.yaml` at the repository root.

The initial test endpoint is:

- `GET /api/status`

## Development

Requires Node.js 24 LTS.

```bash
npm install
npm run lint
npm run bundle
```

Run both validation and bundling with:

```bash
npm run build
```

## License

The contents of this repository are licensed under the Apache License 2.0. See [LICENSE.md](LICENSE.md).

Copyright © Gryph Labs.

## Branding and trademarks

The Apache License 2.0 covers the specification and other licensed material in this repository. It does not grant permission to use Gryph Labs branding, product names, logos, trademarks, or trade dress.

Forks and derivative distributions must use their own branding and must not imply endorsement by, sponsorship from, or affiliation with Gryph Labs. The names “Gryph Labs” and “Phoenix,” along with associated logos and branding, remain the property of Gryph Labs unless separate written permission is granted.
