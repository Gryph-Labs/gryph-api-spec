# Phoenix API Specification

This repository contains the OpenAPI specification for the Phoenix API.

Phoenix API is the HTTP interface used to connect external clients to Gryph Labs systems through a stable, controlled contract. It is intended for clients such as custom GPTs using GPT Actions, other AI models and agents, internal Gryph Labs services, and future applications that need to communicate with Phoenix or other Gryph systems.

The API is deliberately separate from any one AI provider or protocol. MCP may be used as an integration layer in some cases, but it is not a requirement for using Phoenix API. Clients should be able to integrate through normal HTTPS and OpenAPI-compatible tooling.

## What this repository contains

The OpenAPI source is kept under `src/` and split into smaller files for paths, schemas, responses, and other reusable components. Shared Gryph Labs OpenAPI components are consumed from the `gryph-common-spec` submodule under `common-spec/`. Redocly validates those files and bundles them into `phoenix-api-spec.yaml` at the repository root.

The bundled file is the version of the contract intended for consumers and tooling and remains self-contained.

## Development

Node.js 24 LTS is required.

Initialize the shared spec submodule:

```bash
git submodule update --init --remote
```

Install dependencies:

```bash
npm install
```

Validate the specification:

```bash
npm run lint
```

Bundle the specification:

```bash
npm run bundle
```

Run validation and bundling together:

```bash
npm run build
```

## License

The contents of this repository are licensed under the Apache License 2.0. See [LICENSE.md](LICENSE.md).

Copyright © Gryph Labs.

The license does not grant permission to use Gryph Labs or Phoenix names, logos, branding, or other trademarks. Forks and derivative distributions must use their own branding and must not imply endorsement by, sponsorship from, or affiliation with Gryph Labs without written permission.
