# Yafizham Batubara

**Backend / Applied AI Engineer**

Fullstack TypeScript / Node.js / NestJS / React + AI Agent Engineer (LLM tool-calling, RAG)

Jakarta, Indonesia · Open to worldwide remote; open to relocation with visa sponsorship

Backend and applied AI engineer who has built and maintained **15+ production applications** across logistics, sales, finance, and internal workflows at **PT Catur Sukses Internasional**. These systems support multiple tenants with custom role-based access control (RBAC) shaped around each business workflow. Core stack: **TypeScript, Node.js, NestJS, PostgreSQL, and Redis**, with React/Next.js frontends and framework-free LLM agents in Node.js and Python (custom orchestration loop, tool calling, RAG). Currently building an enterprise AI agent integrated with **Microsoft Dynamics NAV**.

**[Email me](mailto:yafizham@pethalvoid.com) · [LinkedIn](https://www.linkedin.com/in/muhammad-yafizham-batubara-b589051a9) · [Explore my repositories](https://github.com/Ham144?tab=repositories)**

## Technical skills

- **Backend & APIs:** TypeScript, Node.js, NestJS, Express.js, Python, FastAPI, REST APIs, WebSockets
- **Frontend & Mobile:** React, Next.js, React Native (Expo), React Flow
- **Data & Infrastructure:** PostgreSQL, MongoDB, Redis, Prisma, Docker, Linux VPS, Nginx, GitHub Actions, Cloudflare
- **AI & LLM:** Custom agent orchestration (tool-calling loop), OpenAI / Anthropic / Gemini / OpenRouter APIs, structured outputs, RAG, pgvector, Qdrant, Langfuse observability, eval sets, guardrails
- **Enterprise Integrations:** Microsoft Dynamics NAV (SOAP/NTLM), LDAP/Active Directory, Midtrans, WhatsApp, Telegram

## Experience

**PT Catur Sukses Internasional — Software Engineer** · Jakarta · Oct 2024 – Present

- Built MIDCSI System Hub, the shared Microsoft Dynamics NAV integration platform behind internal apps and external vendors, now adding an AI agent layer.
- Built and maintain 15+ production applications across logistics, sales, finance, and internal workflows, owning data model, permission rules, APIs, integrations, deployment, and support.
- Designed multi-tenant systems with custom RBAC shaped around each business workflow.
- Resolved high-concurrency warehouse scheduling conflicts with Redis caching/locking and optimized PostgreSQL queries.

## Selected projects

### 1. [MIDCSI System Hub — Shared ERP Integration Platform & AI Agent (Microsoft Dynamics NAV)](https://github.com/Ham144/ninth--sales-app-)
*Node.js, Express, MongoDB, Redis, SOAP/NTLM (httpntlm, xml2js), node-cron, JWT, LDAP, TOTP, OpenRouter LLMs, React 19 + Vite*
- Built the shared integration backend reused by internal apps (e.g. S-BIT Field Sales CRM) and external vendor companies, with an X-API-key management portal: scoped keys (full / public-catalog), expiry, and revocation.
- Wrapped Microsoft Dynamics NAV SOAP/NTLM services and engineered nightly cron batch sync of products, customers, and overdue receivables into MongoDB, with SHA-256 change hashing to skip unchanged records; live NAV sales-order status on demand.
- Delivered a central hub for 16 company apps with login via JWT, LDAP/Active Directory, and TOTP two-factor auth, plus centralized docs and release updates.
- **AI agent layer (in progress, beta):** tool-calling agent built from scratch with no framework: own tool routing over 10+ ERP tools, public and internal-staff personas, prompt-injection guardrails, per-tenant rate limits and daily budgets, audit logs, embedding retrieval, and a tool-selection eval set.

### 2. [Warehouse Queue Management System](https://github.com/Ham144/warehouse-queue-management-system)
*NestJS, PostgreSQL, Redis, Next.js, WebSockets*
- Booking and queue management across **12+ facilities**, **~2,500 bookings/month**, with no reported booking collisions.
- Redis distributed locks, Redis-backed WebSocket scaling, live drag-and-drop dock board, LDAP auth, audit logging.

### 3. [Super POS Mobile](https://github.com/Ham144/super-pos-mobile)
*React Native (Expo), Express.js, MongoDB, Dynamics NAV, Midtrans*
- Mobile POS for **40+ outlets and field reps**, **~15,000 transactions/month**, with no reported transaction loss.
- Offline-first sync and reconciliation, Dynamics NAV SOAP/NTLM shipping/invoicing flows, thermal printing, Midtrans payments.

### 4. [Approva — Approval Workflow Engine](https://approva-ai.hexadim.com/)
*Node.js, Express, MongoDB, React Flow, Redis, LDAP*
- Multi-level approval workflows: **800+ workflows/month** across **5+ departments**.
- DAG-based workflow resolver, visual graph editor, tenant isolation, Redis caching/rate limiting, Telegram and email notifications.

### 5. [BuktiScan — Multi-tenant Invoice Scan & CCTV Evidence System](https://github.com/Ham144/invoTrack)
*NestJS, Prisma, Socket.IO, FFmpeg, Astro + React, Electron*
- Multi-tenant logistics system: barcode invoice scans at cashier PCs automatically trigger CCTV (RTSP) recording, with clips auto-cut and synced to the backend.
- Electron desktop agent ([agent_bukti_scan](https://github.com/Ham144/agent_bukti_scan)) reads USB serial scanners and supports up to 6 scanners + 6 CCTV streams in parallel per workstation; admin dashboard for workstations, scanners, and scan logs.

### 6. [Field Sales CRM (S-BIT)](https://github.com/Ham144/field-sales-crm-sbit)
*React, Express.js, MongoDB, Leaflet, Dynamics NAV*
- Geofenced visit and reporting workflows for **50+ sales reps**, **~3,000 client visits/month**, with ERP synchronization.

These figures describe systems in use at my current employer; linked repositories provide implementation details where public source is available.

### Product screenshots

| Warehouse queue board | Approva workflow interface | Mobile POS checkout |
| :---: | :---: | :---: |
| <img src="assets/screenshots/wqms-realtime-drag-drop-area.webp" width="100%" alt="Warehouse Queue Management System real-time dock board" /> | <img src="assets/screenshots/approval-interactive-workflow.png" width="100%" alt="Approva workflow interface preview" /> | <img src="assets/screenshots/android-pos-small.png" width="100%" alt="Super POS Mobile checkout screens" /> |

## AI and automation projects

- **[Aca](https://aca.pethalvoid.com/)** — WhatsApp AI customer-service assistant built around workflow automation and knowledge retrieval.
- **[Rachel](https://rachel.pethalvoid.com/)** — AI-assisted content production and distribution system. I work on its orchestration, infrastructure, and video rendering pipeline.

## System design

<details>
<summary><strong>Approva — approval workflow engine</strong></summary>

```mermaid
graph TB
    subgraph Client_Studio["Frontend Studio (React 18 + Vite 5)"]
        Canvas["React Flow V11 Graph Canvas Editor"]
        SignatureCanvas["Digital Signature Capture Canvas"]
        ROIExporter["jsPDF ROI Statement Exporter"]
        Turnstile["Cloudflare Turnstile Captcha"]
    end

    subgraph Security_Gateway["Express API Gateway & Security"]
        ExpressRouter["Express.js API Router"]
        RedisMiddleware["Redis Caching & Rate Limit Middleware"]
        LDAP_Auth["Active Directory (LDAP SSO Adapter)"]
        SuperTenantGuard["Super-Tenant Domain Isolator"]
    end

    subgraph Workflow_Engine["DAG Workflow & Logic Resolver"]
        DAG_Resolver["DAG Graph State Resolver"]
        LogicMatcher["Logic & Threshold Evaluator"]
        DeptMatrix["Department Hierarchy Matrix"]
    end

    subgraph Integration_Storage["Storage & Notification Bus"]
        RedisStore[(Redis Cache & Rate Store)]
        MongoDB[(MongoDB Master Cluster)]
        TelegramBot["Telegram Bot Alert Dispatcher"]
        SMTPMail["SMTP Email Service"]
    end

    Canvas -->|Visual Graph Schema| ExpressRouter
    SignatureCanvas -->|Signed Canvas Bytes| ExpressRouter
    Turnstile -->|Validate Token| ExpressRouter
    ExpressRouter --> RedisMiddleware
    RedisMiddleware <-->|Check Cached Flows| RedisStore
    ExpressRouter -->|Authenticate Staff| LDAP_Auth
    LDAP_Auth --> SuperTenantGuard
    SuperTenantGuard --> DAG_Resolver
    DAG_Resolver --> LogicMatcher
    LogicMatcher --> DeptMatrix
    DeptMatrix <-->|Mongoose ODM| MongoDB
    DeptMatrix -->|Dispatch Approval Stage| TelegramBot
    DeptMatrix -->|Send Notification Email| SMTPMail
    ROIExporter -->|Export PDF Report| ClientUser[End User Download]
```

</details>

<details>
<summary><strong>Warehouse Queue Management System — real-time scheduling</strong></summary>

```mermaid
graph TB
    subgraph Client_App["Client Operations Layer"]
        DriverPortal["Driver Pre-Booking Portal (Next.js)"]
        GuardGantt["Live Drag-and-Drop Gantt Board"]
        GateMonitor["Real-Time Gate Display Screen"]
    end

    subgraph Gateway_Auth["NestJS Gateway & Security"]
        NestAPI["NestJS API Gateway"]
        WSGateway["WebSocket Gateway (RedisIoAdapter Cluster)"]
        LDAP["Active Directory LDAP Auth"]
    end

    subgraph Allocation_Engine["Queue & Scheduling Engine"]
        SlotPicker["Auto Efficient Slot Allocator"]
        LockManager["Redis Distributed Lock Manager"]
        BusyTime["Busy-Time Blackout Allocator"]
        ChatEngine["Real-Time Driver-Staff Messenger"]
    end

    subgraph Storage_Audit["Data & Audit Trail"]
        Redis[(Redis Queue & IoAdapter Store)]
        Postgres[(PostgreSQL Master DB)]
        AuditLog["MoveTrace Audit Logger"]
    end

    DriverPortal -->|Slot Booking Request| NestAPI
    GuardGantt -->|Drag & Drop Reposition| WSGateway
    NestAPI -->|Authenticate User| LDAP
    NestAPI --> SlotPicker
    SlotPicker --> BusyTime
    SlotPicker -->|Acquire Lock| LockManager
    LockManager -->|Atomic Lock| Redis
    SlotPicker -->|Persist Schedule| Postgres
    SlotPicker -->|Record Audit| AuditLog
    WSGateway <-->|Redis Pub/Sub Sync| Redis
    WSGateway <-->|Live Updates Broadcast| GuardGantt
    WSGateway <-->|Live Queue Status| GateMonitor
    ChatEngine <-->|Real-Time WebSockets| DriverPortal
```

</details>

<details>
<summary><strong>Super POS Mobile — ERP integration and offline/online flows</strong></summary>

```mermaid
graph TD
    Client[Expo 52 Mobile Client] <-->|REST / Sync APIs| Server[Express API Server]
    Client -->|TCP Socket| Printer[WiFi Thermal POS Printer]
    Server <-->|Mongoose| DB[(MongoDB Database)]
    Server -->|REST APIs| Midtrans[Midtrans Payment Gateway]
    Server <-->|SOAP / NTLM| NAV[(Microsoft Dynamics NAV ERP)]
    Web[Web Admin Dashboard] <-->|REST APIs| Server
    Server <-->|LDAP| AD[(Active Directory)]
    Server -->|Fonnte API| WA[WhatsApp Gateway]
```

```mermaid
sequenceDiagram
    participant K as Kasir (Mobile)
    participant AS as AsyncStorage
    participant API as Express API
    participant DB as MongoDB

    Note over K,AS: 1. Cold start / manual "Sync" tap
    K->>API: syncronizeOfflineMode()
    API->>DB: fetch inventories, diskon, promo, voucher, SPG
    API-->>K: paginated batches
    K->>AS: dump into local cache

    Note over K,AS: 2. Selling — fully offline capable
    K->>AS: create bill, apply promo/diskon locally
    K->>K: print thermal receipt (TCP)
    K->>AS: mark bill paid + decrement local qty

    Note over K,API: 3. Reconciliation (auto or manual)
    K->>API: POST /sinkronisasi/sync-offline-mode (queued bills)
    API->>DB: persist invoices, adjust inventory, stack-trace SKU
    API-->>K: confirm + refresh cache
```

```mermaid
sequenceDiagram
    participant K as Kasir (Mobile)
    participant API as Express API
    participant NAV as Dynamics NAV (SOAP)
    participant DB as MongoDB

    Note over K,API: Catalog & stock are live per screen
    K->>API: GET /inventories/getAllinventoriesMobile (partial)
    API->>NAV: GetInventoryByLocationMultiple
    NAV-->>API: qty per location
    API-->>K: enriched inventory page

    Note over K,NAV: Print bill = ship in NAV
    K->>API: POST /stateless/cetak-bill
    API->>NAV: SalesOrderAutoPostingShip
    NAV-->>API: shipment doc
    API->>DB: persist bill (shipped)
    API-->>K: OK → print customer receipt

    Note over K,NAV: Edit / remove line after bill
    K->>API: POST /stateless/edit-lines
    API->>NAV: GetSalesShipmentLines → WsUndoShipment
    API-->>K: re-print required

    Note over K,NAV: Pay
    K->>API: POST /stateless/bayar
    API->>NAV: WsPostInvoiceSO
    API->>DB: mark done, save nomorTransaksi
    K->>K: print kwitansi

    Note over K,NAV: Void (next day, etc.)
    K->>API: POST /stateless/void
    API->>NAV: GetSalesShipmentLines → WsUndoShipment (all)
```

```mermaid
flowchart LR
    subgraph Mobile["Mobile Client"]
        BH[BillHeader / Sync UI]
        LS[LibrariesScreen]
        BO[useBillOperations]
    end

    BH -- outlet.mode == offline --> SYNC[syncronizeOfflineMode]
    BH -- outlet.mode == stateless --> LIVE[Skip sync UI]

    LS -- offline --> DUMP[AsyncStorage inventories]
    LS -- stateless --> FETCH[GET /inventories/getAllinventoriesMobile]

    BO -- offline --> LOCAL[Local bill + queue]
    BO -- stateless --> ST[/api/v1/stateless/*/]

    SYNC --> API1[POST /sinkronisasi/sync-offline-mode]
    ST --> SOAP[SOAP → NAV ERP]
```

</details>

## How I work

I started most of these projects by designing and coding their foundations myself, from the data model and permission rules to APIs, integrations, deployment, and support. I now use AI tools to speed up implementation, while I remain responsible for architecture, code review, testing, and production behavior. I am most interested in remote backend and applied-AI roles where reliability and measurable business outcomes matter.

**Languages:** Bahasa Indonesia (Native) · English (IELTS General Training: Band 7.0)

**Contact:** [yafizham@pethalvoid.com](mailto:yafizham@pethalvoid.com)

