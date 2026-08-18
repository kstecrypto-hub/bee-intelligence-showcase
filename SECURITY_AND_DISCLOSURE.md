# Security and Disclosure

This public showcase is intentionally incomplete from an implementation perspective. It is designed to demonstrate progress and direction without exposing the private system.

## Intentionally Excluded

The package excludes:

- proprietary source code
- private prompts and prompt templates
- credentials, tokens, secrets, API keys, salts, hashes, and connection strings
- `.env` values and private deployment settings
- raw private datasets
- raw private telemetry
- uploaded documents and source corpus files
- detailed database schemas
- ontology internals and full KG contracts
- implementation-specific retrieval, ranking, validation, and orchestration algorithms
- full API surface details
- internal infrastructure configuration that would make replication easy
- customer, user, tenant, or operator data
- Git history, commit metadata, remotes, branches, and private repository metadata

## Public Package Intent

The public package is intended to show:

- the product direction
- the implemented high-level technical areas
- the evidence-grounded architecture philosophy
- the agriculture-first and future-robotics vision
- safe synthetic examples of interaction shape
- the boundary between implemented, tested, unvalidated, and future work

It is not intended to be a runnable application, SDK, or architecture blueprint sufficient to recreate the private implementation.

## Data Handling

Example files in this directory are synthetic. They are not copied from private sensor logs, customer data, uploaded documents, database exports, prompts, or production source files.

Any future public repository based on this package should keep the same boundary: publish sanitized narrative artifacts and synthetic examples only, unless a specific dataset or artifact has been reviewed and approved for public release.

## Claim Boundaries

This package avoids claiming:

- public deployment
- live in-hive validation
- scientific validation
- robotic actuation
- autonomous interventions
- commercial scale
- complete source availability
- diagnostic accuracy without supporting evidence

The current project should be described as a private technical prototype and platform foundation with substantial implemented backend, retrieval, KG, telemetry, operations, and frontend work.

## Recommended Public-Release Checklist

Before publishing this directory anywhere:

- run a secret scan on the public package
- confirm no source files were copied
- confirm all examples are synthetic
- confirm no private prompts or schema definitions appear
- confirm robotics is described as future work
- confirm live-hive validation is not claimed
- confirm the repository itself remains private
