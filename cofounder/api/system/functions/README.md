# System Functions Documentation

This directory contains various functions for different tasks within the system. Each function is designed to perform a specific task and can interact with other functions. Below is a detailed documentation for each function, explaining their interactions and usage.

## Table of Contents

- [Backend Functions](#backend-functions)
  - [AsyncAPI Definition](#asyncapi-definition)
  - [OpenAPI Definition](#openapi-definition)
  - [Server Generation](#server-generation)
- [Database Functions](#database-functions)
  - [Postgres Generation](#postgres-generation)
  - [Schema Generation](#schema-generation)
- [Project Management Functions](#project-management-functions)
  - [BRD Analysis](#brd-analysis)
- [Operational Functions](#operational-functions)
  - [Convert Markdown to PDF](#convert-markdown-to-pdf)

## Backend Functions

### AsyncAPI Definition

**File:** `backend/asyncapi.js`

**Description:** Defines the AsyncAPI specifications for the backend based on the provided requirements.

**Interactions:** 
- Interacts with the project state to update the AsyncAPI specifications.
- Uses LLM to generate the AsyncAPI structure.

### OpenAPI Definition

**File:** `backend/openapi.js`

**Description:** Defines the OpenAPI specifications for the backend based on the provided requirements.

**Interactions:** 
- Interacts with the project state to update the OpenAPI specifications.
- Uses LLM to generate the OpenAPI structure.

### Server Generation

**File:** `backend/server.js`

**Description:** Generates the full Node.js script for the backend server based on the provided specifications.

**Interactions:** 
- Interacts with the project state to update the server script.
- Uses LLM to generate the server code.
- Augments the server code with external API requirements if needed.

## Database Functions

### Postgres Generation

**File:** `db/postgres.js`

**Description:** Generates the PostgreSQL commands to create tables and seed the database based on the provided requirements.

**Interactions:** 
- Interacts with the project state to update the PostgreSQL commands.
- Uses LLM to generate the PostgreSQL commands.

### Schema Generation

**File:** `db/schemas.js`

**Description:** Generates the database schemas based on the provided requirements.

**Interactions:** 
- Interacts with the project state to update the database schemas.
- Uses LLM to generate the database schemas.

## Project Management Functions

### BRD Analysis

**File:** `pm/brd.js`

**Description:** Conducts a comprehensive analysis for the Backend Requirements Document (BRD) based on the provided project details.

**Interactions:** 
- Interacts with the project state to update the BRD.
- Uses LLM to generate the BRD.

## Operational Functions

### Convert Markdown to PDF

**File:** `op/convert.js`

**Description:** Converts a given markdown document to a PDF.

**Interactions:** 
- Uses external libraries to convert markdown to PDF.
