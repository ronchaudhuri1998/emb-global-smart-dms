# EMB Global -- Smart Document Management System (Smart DMS)

An AI-powered **Smart Document Management System (DMS)** designed to
ingest, process, validate, monitor, and query enterprise documents such
as **Purchase Orders, Invoices, Service Agreements, and RFPs**.

The system combines **OCR, document intelligence, dashboards, alerts,
and an LLM-powered assistant** built using **AWS Bedrock Agents and
Retrieval-Augmented Generation (RAG)**.

> ⚠️ This is a **parent / overview repository**.\
> Source code for frontend and backend services is maintained in
> separate repositories.

------------------------------------------------------------------------

## Problem Context

Enterprise finance and operations teams handle large volumes of
**unstructured and semi-structured documents** that:

-   Do not follow fixed templates\
-   Often arrive as scanned PDFs\
-   Contain inconsistent identifiers\
-   Require manual reconciliation and follow-ups

These challenges lead to: - Missed contract renewals\
- Invoice mismatches and delayed payments\
- Poor visibility into PO utilization\
- Reactive and error-prone workflows

This project demonstrates how **AI-driven document intelligence** can
automate these processes and provide **real-time operational
visibility**.

------------------------------------------------------------------------

## System Overview

The Smart DMS consists of three core components:

### 1. Document Ingestion & Processing

-   Multi-file PDF upload
-   OCR-based text extraction
-   Structured field extraction (client, amount, dates, references)
-   Validation and exception detection

### 2. Monitoring & Dashboard

-   Centralized document inventory
-   MSA-based document grouping
-   KPI tracking (PO usage, invoice utilization, exceptions)
-   Alerts for thresholds and expirations

### 3. AI-Powered Document Assistant

-   Conversational querying over enterprise documents
-   RAG-based grounding via AWS Bedrock Knowledge Base
-   Context-aware summaries and lookups

------------------------------------------------------------------------

## Solution Architecture

![Detailed Solution
Architecture](assets/architecture/detailed-solution-architecture.png)

### High-Level Flow

1.  User uploads documents via the DMS Console\
2.  Backend performs OCR and document extraction\
3.  Structured data is validated and stored\
4.  Documents are indexed into a knowledge base\
5.  Dashboards reflect real-time metrics\
6.  Users query documents via the AI assistant

------------------------------------------------------------------------

## Application Screenshots

### Operations Dashboard

![Operations
Dashboard](assets/screenshots/01-dashboard-operations-pulse.png)

### AI Assistant -- Capability Overview

![Chatbot
Overview](assets/screenshots/02-chatbot-assistant-overview.png)

### AI Assistant -- PO Query Example

![PO Query via
Chatbot](assets/screenshots/03-chatbot-po-query-response.png)

### Documents View -- MSA Buckets

![MSA Buckets](assets/screenshots/04-documents-msa-buckets.png)

### Document Details & OCR Extraction

![Document
Details](assets/screenshots/05-document-details-extracted-fields.png)

### Document Inventory

![Document Inventory](assets/screenshots/06-document-inventory-list.png)

------------------------------------------------------------------------

## Demo Walkthrough

A guided demo flow describing how to present and navigate the system is
available here:

📄 **[demo/demo-flow.md](demo/demo-flow.md)**

------------------------------------------------------------------------

## Technology Stack

-   **Frontend:** Next.js, Tailwind CSS\
-   **Backend:** Node.js / API-based services\
-   **AI Services:** AWS Bedrock (Claude Haiku)\
-   **OCR:** AWS Textract\
-   **RAG:** Bedrock Knowledge Base (semantic retrieval + generation)\
-   **Storage:** Amazon S3, PostgreSQL\
-   **Deployment:** Serverless (AWS Lambda, Function URLs)

------------------------------------------------------------------------

## Key Challenges Addressed

-   Inconsistent document formats across vendors and clients\
-   OCR noise from scanned PDFs\
-   Missing or ambiguous identifiers\
-   Linking related documents across multiple document types\
-   Controlling hallucinations in LLM responses\
-   Balancing cost and performance for LLM inference

------------------------------------------------------------------------

## Related Repositories

### Frontend -- DMS Console

https://github.com/rishabh15b/DMSDashboard_frontend

### Backend -- DMS Services & AI

https://github.com/ronchaudhuri1998/DMS_Dashboard_backend

------------------------------------------------------------------------

## Project Status

This is an **academic and demonstration project** created to showcase:

-   End-to-end AI system design\
-   Enterprise document intelligence workflows\
-   Practical LLM integration using AWS Bedrock\
-   Clear separation of frontend, backend, and system architecture

------------------------------------------------------------------------

## References

-   📄 Project Deck: `docs/EMB-Global-Smart-DMS.pdf`
