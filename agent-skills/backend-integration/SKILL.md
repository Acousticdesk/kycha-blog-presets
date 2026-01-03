---
name: backend-integration
description: Ensure the front-end application remains fully compatible with the backend API by referencing and adhering to the Server API Specification.
---

# Skill: Backend Integration

## Purpose

Ensure the front-end application remains fully compatible with the backend API by referencing and adhering to the Server API Specification.

## Capabilities

- Read and interpret the Server API Specification.
- Validate that front-end API calls strictly match the defined contract.
- Identify discrepancies between implementation and API spec.
- Propose safe updates when the contract changes.

## Inputs

- front-end network layer source files
- `Server API Specification - ENDPOINTS.md`

## Compatibility Rules

The implementation must match the specification for:

- HTTP methods, paths, and query params
- Request/response JSON schema
- Authentication and headers
- Pagination and rate limits
- Error handling contract
- Versioned endpoints

## Reference

- The Server API Specification is located in the `ENDPOINTS.md` file in the root folder of the `backend-integration` skill. Path: `.claude/skills/backend-integration/ENDPOINTS.md`.
