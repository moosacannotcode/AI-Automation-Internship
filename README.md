# AI Automation Internship

This repository contains my assignments, projects, documentation, and deliverables completed during the **MATalogics AI Automation (No-Code & Low-Code Systems Engineering) Internship**.

## Internship Work

### Day 03 — Lead Management API

Built a complete Lead Management API using:

- **n8n** — Workflow automation and webhook-based API layer
- **Postman** — API development and testing
- **Google Sheets** — Lead data storage and management

### APIs Implemented

| Method | Endpoint | Function |
|---|---|---|
| POST | `/create-lead` | Create a new lead |
| GET | `/get-leads` | Retrieve all leads |
| PUT | `/update-lead` | Update an existing lead |
| DELETE | `/delete-lead` | Delete a lead |

### Workflow

All four API operations are implemented within a single n8n workflow.

```text
POST /create-lead
        ↓
   Validate Data
        ↓
   Google Sheets
   (Append Row)
        ↓
 Respond to Webhook


GET /get-leads
        ↓
   Google Sheets
    (Read Rows)
        ↓
 Respond to Webhook


PUT /update-lead
        ↓
 Find Lead by Email
        ↓
   Update Row
        ↓
 Respond to Webhook


DELETE /delete-lead
        ↓
 Find Lead by Email
        ↓
   Delete Row
        ↓
 Respond to Webhook
