School AI Assistant

A school-focused AI assistant designed to provide grounded, permission-aware access to institutional knowledge and documents.

The system is designed around a controlled knowledge base rather than unrestricted web-based generation. Its purpose is to help authorized users retrieve and work with school information while maintaining boundaries around protected and restricted data.

⸻

Table of Contents

1. I. Overview
    * A. Project Description
    * B. Project Goals
    * C. Current Status
2. II. System Architecture
    * A. High-Level Architecture
    * B. Core System Roles
3. III. Knowledge System
    * A. Markdown-Based Knowledge
    * B. Grounded Responses
    * C. File Citations
4. IV. Access Control
    * A. Permission Levels
    * B. Protected Information
    * C. Authorization-Aware Responses
5. V. External Integrations
    * A. Google Workspace
    * B. Document and Spreadsheet Data
6. VI. AI System
    * A. Assistant Responsibilities
    * B. Knowledge Boundaries
7. VII. Security Principles
8. VIII. Development Status
9. IX. Future Direction
    * A. Expanded Knowledge Operations
    * B. Improved Agent Coordination
10. X. Technologies
11. XI. Documentation

⸻

I. Overview

A. Project Description

School AI Assistant is a knowledge-grounded AI system designed for use within a school environment.

The system provides an interface for authorized users to interact with institutional knowledge while maintaining explicit boundaries between accessible, protected, and restricted information.

Rather than treating the AI model as the source of truth, the system is designed to ground responses in approved institutional documents.

The institution using the system is intentionally not identified in this public repository.

B. Project Goals

The project is designed around several goals:

* Provide useful AI-assisted access to institutional knowledge
* Ground responses in approved source material
* Provide citations to supporting files
* Respect user permissions
* Separate general knowledge from protected information
* Prevent unauthorized access to restricted records
* Support structured document and spreadsheet workflows
* Maintain a clear boundary between AI reasoning and authoritative source data

C. Current Status

Status: Active development

The project has an established architecture for:

* Knowledge-grounded AI assistance
* Markdown-based knowledge storage
* Permission-aware retrieval
* File citations
* Protected information boundaries
* Google Workspace integration
* Controlled document and spreadsheet workflows

The system continues to be developed and tested as a private project.

⸻

II. System Architecture

A. High-Level Architecture
                    User
                      │
                      ▼
              ┌──────────-────┐
              │ AI Assistant  │
              └───────┬───────┘
                      │
             Authorization Check
                      │
                      ▼
              ┌───────────────┐
              │ Knowledge /   │
              │ Retrieval     │
              │ Layer         │
              └───────┬───────┘
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
   Approved Knowledge       Protected Data
      Sources              Access-Controlled
          │                       │
          └───────────┬───────────┘
                      ▼
              Grounded Response
                      │
                      ▼
                File Citations

The architecture separates the AI assistant from the underlying knowledge sources and access-control mechanisms.

The model is not intended to independently determine whether a user should have access to protected information.

B. Core System Roles

A. AI Assistant

Provides the conversational interface and processes authorized information.

B. Knowledge Layer

Provides approved source material that can be retrieved and used to ground responses.

C. Authorization Layer

Determines which categories of information a user is permitted to access.

D. External Data Layer

Provides controlled access to supported external documents, spreadsheets, and other institutional resources.

⸻

III. Knowledge System

A. Markdown-Based Knowledge

The primary knowledge architecture uses structured Markdown files.

This provides a human-readable knowledge base that can be:

* Organized into folders
* Reviewed by administrators
* Version controlled
* Updated without retraining the model
* Retrieved by the assistant

The knowledge base is intended to contain information that has been explicitly approved for AI use.

B. Grounded Responses

The assistant is designed to prioritize information retrieved from the approved knowledge base.

The intended response flow is:

User Question
     │
     ▼
Permission / Scope Check
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

This reduces reliance on unsupported model-generated information when authoritative institutional material is available.

C. File Citations

Responses can identify the source files used to support an answer.

Citations provide users with a way to trace generated information back to the underlying institutional source.

⸻

IV. Access Control

A. Permission Levels

The system uses defined access levels for controlling knowledge availability:

Level-----------Purpose
READ_ONLY-------Information may be accessed but not modified
READ_WRITE------Authorized information may be read and modified
PROTECTED-------Restricted information requiring additional authorization
NO_ACCESS-------Information must not be accessed

These permissions are part of the system’s security boundary rather than merely instructions to the language model.

B. Protected Information

The architecture recognizes that school environments may contain information requiring stronger access controls.

Examples include:

* Student records
* Individual education information
* Disciplinary records
* Health-related information
* Personnel information
* Legal or administrative information

Sensitive institutional information should not be treated as general AI knowledge.

C. Authorization-Aware Responses

The system is designed so that authorization affects what information can be retrieved and used.

The goal is to prevent a user from obtaining restricted information simply by phrasing a request differently.

⸻

V. External Integrations

A. Google Workspace

The system is designed to work with supported Google Workspace resources through controlled authentication and access.

This can provide access to approved institutional:

* Google Drive
* Google Docs
* Google Sheets

B. Document and Spreadsheet Data

External documents and spreadsheets can serve as controlled information sources when explicitly made available to the system.

The architecture distinguishes between:

* Files available as knowledge
* Files created by the assistant
* Files that should remain outside the knowledge base
* Protected files requiring additional authorization

This separation helps prevent newly generated documents from automatically becoming authoritative knowledge.

⸻

VI. AI System

A. Assistant Responsibilities

The assistant is intended to:

* Answer questions using authorized knowledge
* Retrieve relevant institutional information
* Cite supporting sources
* Assist with document-based workflows
* Respect information boundaries
* Help users interact with approved school resources

B. Knowledge Boundaries

The system distinguishes between approved knowledge and temporary or generated content.

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

Generated content does not automatically become part of the knowledge base.

This helps prevent generated information from silently becoming an authoritative source.

⸻

VII. Security Principles

The system is designed around several security principles:

A. Least-Privilege Access

Users should receive only the information and operations required for their authorized role.

B. Explicit Knowledge Sources

Information should be intentionally designated as usable knowledge rather than automatically ingesting everything available to the system.

C. Protected Boundaries

Sensitive information should remain behind explicit access controls.

D. Separation of Concerns

The AI model should not be the sole enforcement mechanism for authorization.

E. Credential Isolation

Credentials and authentication secrets should remain outside the public repository and should not be embedded in source code or documentation.

⸻

VIII. Development Status

The project currently has an established architecture for:

* Knowledge storage
* Retrieval
* Source citations
* Permission levels
* Protected information boundaries
* External document access
* Controlled AI interaction

Implementation details continue to evolve as the system is developed and tested.

Public documentation intentionally describes the architecture at a high level and does not expose private institutional information or credentials.

⸻

IX. Future Direction

A. Expanded Knowledge Operations

Future development may expand:

* Knowledge organization
* Retrieval accuracy
* Source verification
* Document workflows
* Administrative tools
* Permission management

B. Improved Agent Coordination

The system may eventually use specialized AI components for different responsibilities while maintaining centralized authorization and knowledge boundaries.

Potential responsibilities could include:

* Retrieval
* Document processing
* Knowledge organization
* Administrative workflows
* Response verification

These components are planned directions rather than claims about currently implemented functionality.

⸻

X. Technologies

The project currently involves technologies including:

* Large Language Models
* Markdown
* Obsidian-based knowledge management
* Python
* Google Workspace
* Google Drive
* Google Docs
* Google Sheets
* OAuth-based authentication
* Agent-based AI workflows

⸻

XI. Documentation

Detailed technical architecture is maintained in a separate architecture documentation file within the project.
