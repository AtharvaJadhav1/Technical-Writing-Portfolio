# ChatCSV AI — API Reference

> **Authoring worksheet — not a finished writing sample.** Inspect the FastAPI route definitions and schemas, exercise the API, and write the final reference independently. Do not invent routes, authentication requirements, fields, or response examples.

## Overview

Explain the API's purpose and the relationship between the API and the application.

## Base URL

Record the base URL for the local development setup and explain how it changes in deployment. Verify the value from the current configuration.

## Authentication

State whether authentication is required. If it is, document the verified mechanism and safe credential handling. If it is not, say so explicitly.

## Endpoint reference

Create one subsection for each endpoint that is intended for external or frontend use.

### METHOD /actual/path

- **Purpose:**
- **When to use it:**
- **Path parameters:**
- **Query parameters:**
- **Headers:**
- **Request body:**
- **Successful response:**
- **Error responses:**
- **Example request:**
- **Example response:**

Repeat the subsection for each verified endpoint. Include only fields and status codes observed in the implementation or confirmed by tests.

## Common error responses

Describe actual error formats and status codes. Explain what a caller can do next.

## End-to-end example

Document a realistic API workflow in the correct order, using safe example data and verified requests.

## Versioning and compatibility

Document the current versioning policy. If no formal policy exists, state that rather than implying one.

## Verification notes

Record how the examples were tested, the source commit tested, and any limitations.
