# Yafizham Batubara

**Backend Engineer · Applied AI Engineer · Enterprise Systems**

Jakarta, Indonesia · Open to worldwide remote roles and on-site relocation with visa sponsorship

I build software that teams use to run daily operations. At **PT Catur Sukses Internasional**, I have built and maintained **15+ production applications** across logistics, sales, finance, and internal workflows. These systems support multiple tenants and use custom role-based access control (RBAC) shaped around each business workflow. My core stack is **TypeScript, Node.js, NestJS, PostgreSQL, and Redis**. I also work on AI agents, LLM orchestration, and enterprise integrations.

**[Email me](mailto:yafizham@pethalvoid.com) · [LinkedIn](https://www.linkedin.com/in/muhammad-yafizham-batubara/) · [Explore my repositories](https://github.com/Ham144?tab=repositories)**

## Current focus: AI agent for Microsoft Dynamics NAV

I am building an enterprise chatbot that connects authenticated, persistent conversations to internal workflows and **Microsoft Dynamics NAV** through **SOAP/NTLM**. Its goal-oriented agent uses conversation context to support e-commerce customers, warehouse administrators, and telemarketing staff. The backend keeps ERP credentials and privileged operations server-side.

**In development:** a permission-aware **Retrieval-Augmented Generation (RAG)** pipeline over ERP data, using PostgreSQL for structured retrieval data and Redis as a planned retrieval/vector cache. It is intended to answer inventory and approval questions with current, authorized data. I do not present this pipeline as deployed or measured yet.

## Selected production work

| Project | What I built | Scale and outcome |
| --- | --- | --- |
| [Warehouse Queue Management System](https://github.com/Ham144/warehouse-queue-management-system) | Booking and queue management for warehouse operations | **12+ facilities**, **~2,500 bookings/month**, with no reported booking collisions |
| [Super POS Mobile](https://github.com/Ham144/super-pos-mobile) | Mobile point-of-sale workflows for outlets and field teams | **40+ outlets and field reps**, **~15,000 transactions/month**, with no reported transaction loss |
| [Approva](https://approva-ai.hexadim.com/) | Multi-level approval workflows for cross-department operations | **800+ workflows/month** across **5+ departments** |
| [Inventory Audit System](https://github.com/Ham144/inventory-audit-system) | Inventory counting and audit workflows | **100,000+ SKU line items/year** |
| [Field Sales CRM (S-BIT)](https://github.com/Ham144/field-sales-crm-sbit) | Geofenced visit and reporting workflows for field sales | **50+ sales reps**, **~3,000 client visits/month** |

These figures describe the systems in use at my current employer; the linked repositories provide implementation details where public source is available.

### Product screenshots

| Warehouse queue board | Approva workflow interface | Mobile POS checkout |
| :---: | :---: | :---: |
| <img src="assets/screenshots/wqms-realtime-drag-drop-area.webp" width="100%" alt="Warehouse Queue Management System real-time dock board" /> | <img src="assets/screenshots/approval-interactive-workflow.png" width="100%" alt="Approva workflow interface preview" /> | <img src="assets/screenshots/android-pos-small.png" width="100%" alt="Super POS Mobile checkout screens" /> |

## AI and automation projects

- **[Aca](https://aca.pethalvoid.com/)** — WhatsApp customer-service assistant built around workflow automation and knowledge retrieval.
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

**Languages:** Indonesian (native), English (IELTS General Training 7.0)

**Contact:** [yafizham@pethalvoid.com](mailto:yafizham@pethalvoid.com)

