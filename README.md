# School AI Assistant

A school-focused AI assistant designed to provide grounded, permission-aware access to institutional knowledge and documents.

The system is designed around controlled knowledge sources rather than unrestricted AI generation. Its goal is to help authorized users retrieve and work with institutional information while maintaining boundaries around protected and restricted data.

The institution using the system is intentionally not identified in this public repository.

---

## Table of Contents

1. [I. Overview](#i-overview)
   - [A. Project Description](#a-project-description)
   - [B. Project Goals](#b-project-goals)
   - [C. Current Status](#c-current-status)
2. [II. System Architecture](#ii-system-architecture)
   - [A. High-Level Model](#a-high-level-model)
   - [B. System Roles](#b-system-roles)
3. [III. Knowledge System](#iii-knowledge-system)
   - [A. Knowledge Sources](#a-knowledge-sources)
   - [B. Grounded Responses](#b-grounded-responses)
   - [C. Source Citations](#c-source-citations)
4. [IV. Access Control](#iv-access-control)
   - [A. Permission Levels](#a-permission-levels)
   - [B. Protected Information](#b-protected-information)
   - [C. Authorization-Aware Retrieval](#c-authorization-aware-retrieval)
5. [V. External Integrations](#v-external-integrations)
   - [A. Google Workspace](#a-google-workspace)
   - [B. Documents and Spreadsheets](#b-documents-and-spreadsheets)
6. [VI. AI Responsibilities](#vi-ai-responsibilities)
   - [A. Assistant Functions](#a-assistant-functions)
   - [B. Knowledge Boundaries](#b-knowledge-boundaries)
7. [VII. Security Principles](#vii-security-principles)
8. [VIII. Development Status](#viii-development-status)
9. [IX. Future Direction](#ix-future-direction)
   - [A. Knowledge Operations](#a-knowledge-operations)
   - [B. Agent Coordination](#b-agent-coordination)
10. [X. Technologies](#x-technologies)
11. [XI. Documentation](#xi-documentation)

---

# I. Overview

## A. Project Description

School AI Assistant is a knowledge-grounded AI system designed for school-related workflows.

The system provides an interface through which authorized users can interact with institutional knowledge while maintaining explicit boundaries between accessible, protected, and restricted information.

The project is designed around the principle that institutional information should come from approved source material rather than being treated as knowledge generated solely by the language model.

## B. Project Goals

The project is designed to:

- Provide AI-assisted access to institutional knowledge
- Ground responses in approved source material
- Provide citations to supporting files
- Respect user permissions
- Separate general knowledge from protected information
- Prevent unauthorized access to restricted records
- Support controlled document and spreadsheet workflows
- Maintain a clear boundary between source information and generated content

## C. Current Status

**Status: Active development**

The project has established the core concepts for:

- Knowledge-grounded AI assistance
- Markdown-based knowledge management
- Permission-aware information access
- File citations
- Protected information boundaries
- Google Workspace integration
- Controlled document and spreadsheet workflows

The system continues to be developed and tested as a private project.

---

# II. System Architecture

## A. High-Level Model

The system separates the major responsibilities involved in providing grounded AI assistance:

```text
                    User
                      │
                      ▼
              ┌───────────────┐
              │ AI Assistant  │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Authorization │
              │    Layer      │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │   Knowledge   │
              │ / Retrieval   │
              └───────┬───────┘
                      │
             ┌────────┴────────┐
             ▼                 ▼
      Approved Sources   External Sources
             │                 │
             └────────┬────────┘
                      ▼
              Grounded Response
                      │
                      ▼
                  Citations
```

## B. System Roles

### A. AI Assistant

Provides the conversational interface and processes information made available through the system.

### B. Knowledge Layer

Provides approved institutional source material that can be retrieved and used to ground responses.

### C. Authorization Layer

Controls access to information according to defined permissions.

### D. External Data Layer

Provides controlled access to supported external resources such as documents and spreadsheets.

---

# III. Knowledge System

## A. Knowledge Sources

The system uses structured knowledge sources, primarily Markdown-based information organized within a controlled knowledge repository.

This allows knowledge to be:

- Human-readable
- Organized
- Reviewed
- Updated independently of model training
- Explicitly included in the AI knowledge system

Not every file accessible to the broader system is automatically considered AI knowledge.

## B. Grounded Responses

The assistant is designed to prioritize information retrieved from approved knowledge sources.

The general workflow is:

```text
User Question
     │
     ▼
Authorization / Scope Check
     │
     ▼
Knowledge Retrieval
     │
     ▼
Relevant Source Material
     │
     ▼
AI Processing
     │
     ▼
Grounded Response
```

This is intended to reduce unsupported responses when authoritative institutional information is available.

## C. Source Citations

The system is designed to identify the source files used to support an answer.

This allows users to trace generated information back to the underlying institutional material.

---

# IV. Access Control

## A. Permission Levels

The system uses four defined permission levels:

| Level | Purpose |
|---|---|
| `READ_ONLY` | Information may be accessed but not modified |
| `READ_WRITE` | Authorized information may be read and modified |
| `PROTECTED` | Restricted information requiring additional authorization |
| `NO_ACCESS` | Information must not be accessed |

## B. Protected Information

The architecture recognizes that school environments can contain information requiring additional protection.

Examples include:

- Student records
- Individual education information
- Disciplinary records
- Health-related information
- Personnel information
- Legal information
- Restricted administrative information

Real protected institutional records are not included in this public repository.

## C. Authorization-Aware Retrieval

Access permissions are intended to affect what information can be retrieved and used by the assistant.

The system should not rely solely on the language model to decide whether a user is allowed to access restricted information.

---

# V. External Integrations

## A. Google Workspace

The system is designed to work with authorized Google Workspace resources.

Supported resource types include:

- Google Drive
- Google Docs
- Google Sheets

## B. Documents and Spreadsheets

External files can have different roles within the system.

For example:

```text
External File
     │
     ├── Approved Knowledge
     │
     ├── Working File
     │
     ├── Generated Output
     │
     └── Protected Resource
```

These categories are intentionally kept separate.

A document created by the assistant should not automatically become authoritative knowledge.

---

# VI. AI Responsibilities

## A. Assistant Functions

The assistant is intended to:

- Answer questions using authorized information
- Retrieve relevant institutional information
- Cite supporting sources
- Assist with document-based workflows
- Respect information boundaries
- Help users interact with approved resources

## B. Knowledge Boundaries

The system distinguishes between approved knowledge and temporary or generated content.

```text
Approved Knowledge
       │
       ▼
Authorized Retrieval
       │
       ▼
AI Context
       │
       ▼
Grounded Response
```

Generated content does not automatically become part of the knowledge base.

This helps prevent generated information from silently becoming an authoritative source.

---

# VII. Security Principles

The project follows several core security principles:

### A. Least Privilege

Users and system components should receive only the permissions required for their intended operations.

### B. Explicit Knowledge Sources

Information should be intentionally designated as usable AI knowledge.

### C. Protected Boundaries

Sensitive information should remain behind explicit access controls.

### D. Separation of Responsibilities

Authorization should not depend solely on instructions given to the language model.

### E. Credential Isolation

Credentials, access tokens, private keys, and other secrets should remain outside the public repository.

---

# VIII. Development Status

The project currently has established work around:

- Knowledge storage
- Knowledge retrieval
- Source citations
- Permission levels
- Protected information boundaries
- External document access
- AI-assisted interaction

Implementation continues to evolve as the system is developed and tested.

Public documentation intentionally avoids exposing private institutional information, credentials, internal identifiers, or sensitive operational details.

---

# IX. Future Direction

## A. Knowledge Operations

Future development may expand:

- Knowledge organization
- Retrieval accuracy
- Source verification
- Document workflows
- Administrative tools
- Permission management

## B. Agent Coordination

The system may eventually use specialized AI components for different responsibilities while maintaining centralized authorization and knowledge boundaries.

Potential responsibilities include:

- Retrieval
- Document processing
- Knowledge organization
- Administrative workflows
- Response verification

These are planned directions and are not presented as currently implemented functionality.

---

# X. Technologies

The project involves technologies including:

- Large Language Models
- Markdown
- Obsidian
- Python
- Google Workspace
- Google Drive
- Google Docs
- Google Sheets
- OAuth
- Agent-based AI workflows

---

# XI. Documentation

Detailed technical architecture is maintained in a separate architecture documentation file within the project.
