# Hi, I'm Muhammad Yafizham 👋
### Full-Stack Software Engineer | High-Concurrency Systems & Enterprise Backend

I am a Software Engineer at PT Catur Sukses Internasional specializing in high-concurrency backend architecture, real-time logistics engines, and enterprise ERP integrations. I have architected and deployed mission-critical operational platforms — including a DAG-based Approval Workflow Engine, a Redis-clustered Warehouse Queue System, and an Offline-First Mobile POS — handling distributed synchronization, concurrent transaction locking, and multi-tenant enterprise workflows at production scale. Fluent in English.

 [💼 LinkedIn](https://www.linkedin.com/in/muhammad-yafizham-batubara/)

---

### 📈 GitHub Stats

<p align="left">
  <img src="https://github-readme-stats-eight-theta.vercel.app/api?username=Ham144&show_icons=true&theme=tokyonight&count_private=true" alt="Ham144's GitHub Stats" height="180px" />
  <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=Ham144&layout=compact&theme=tokyonight&langs_count=6" alt="Ham144's Top Languages" height="180px" />
</p>

---

### 🛠️ Core Technology Stack

| Focus Area | Technologies |
| :--- | :--- |
| **AI & LLM Workflows** | OpenRouter, Gemini 2.5 Flash, OpenAI APIs, Custom Prompt Orchestration, Structured JSON Outputs, Spaced Repetition Algorithms, Telegram Bot Webhooks |
| **Backend & APIs** | NestJS, Express.js, Node.js, RESTful APIs, WebSockets (RedisIoAdapter), SOAP/NTLM |
| **Databases & Caching** | PostgreSQL, MongoDB, Redis (ioredis), SQLite/LibSQL, Prisma ORM, Mongoose |
| **Frontend & Mobile** | React 18, Next.js 15, React Native 0.76, Expo 52, React Flow, Tailwind CSS v4, Zustand |
| **Infrastructure & DevOps** | Docker, Linux VPS, Nginx, CI/CD (GitHub Actions), LDAP/Active Directory |
| **Integrations** | MS Dynamics NAV (ERP), Midtrans Payment Gateway, Cloudflare R2 / Turnstile, Telegram Bot API, WhatsApp Web API |

---

> 📂 **Source Code & Live Demos:**
> Selected production repositories are publicly available on GitHub. Full architectural specifications, system design diagrams, UI screenshot galleries, and **Live Production Web Applications** are available below for evaluation.

---

## Featured Production Projects

---

### 1. 🔄 Approval Workflow Engine (Approva.ai)

> Dynamic multi-tenant & super-tenant approval system with a visual drag-and-drop workflow designer  
> 🔗 **Live Web Application:** [approva-ai.hexadim.com](https://approva-ai.hexadim.com)  
> 📊 **Scale & Impact:** Adopted across 5+ corporate departments, automating 800+ multi-tier approval workflows monthly.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-approva--ai.hexadim.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://approva-ai.hexadim.com)
![React Flow](https://img.shields.io/badge/Frontend-React%20Flow%20V11-FF007A?style=flat-square&logo=react)
![React](https://img.shields.io/badge/UI-React%2018%20%2B%20Vite-61DAFB?style=flat-square&logo=react)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=flat-square&logo=nodedotjs)
![Redis](https://img.shields.io/badge/Cache-Redis-DC382D?style=flat-square&logo=redis)
![Active Directory](https://img.shields.io/badge/Auth-LDAP%20%2F%20Active%20Directory-0078D4?style=flat-square&logo=windows)
![Cloudflare](https://img.shields.io/badge/Security-Cloudflare%20Turnstile-F38020?style=flat-square&logo=cloudflare)

Replaces hardcoded business approval paths with a visual graph editor. Enterprise administrators visually configure conditional routing (e.g., auto-escalating based on department categories, monetary thresholds, or custom logic matrices) with digital canvas signatures, Redis caching, and automated multi-channel alert dispatches.

<p align="center">
  <img src="assets/screenshots/approval-interactive-workflow.png" width="90%" alt="Interactive Workflow Hub" />
</p>

<p align="center">
  <img src="assets/screenshots/history.png" width="48%" alt="Approva.ai Application" />
  <img src="assets/screenshots/approval-motto.png" width="48%" alt="Approva.ai Branding" />
</p>

**Key capabilities:**
* **Visual Workflow Designer:** Drag-and-drop graph nodes (React Flow V11) to construct multi-tier approval chains, custom form inputs, and dynamic decision logic — no code changes, no redeployment.
* **Super-Tenant & Cross-Org Flow Duplication:** Multi-tenant architecture with super-admin controls allowing instant replication of complex workflow templates across independent organizational domains.
* **Redis High-Concurrency Caching Layer:** Custom `RedisService` middleware caching active flow instances, department hierarchies, and rate-limiting high-volume approval submissions.
* **Digital Signature & ROI PDF Exporter:** Built-in html5 canvas digital signature capture (`SignatureInput`), SHA-256 audit trails, and automated jsPDF financial ROI statement generation (`RoiStatementModal`).
* **Active Directory SSO & Cloudflare Security:** Integrates local Active Directory (LDAP) for corporate Single Sign-On and Cloudflare Turnstile Captcha to prevent automated bot submissions.

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

---

### 2. 🗓️ Warehouse Queue Management System (WQMS)

> Real-time loading dock booking, RedisIoAdapter WebSocket cluster, and Gantt board carrier scheduler  
> 🔗 **Live Web Application:** [orbit.pethalvoid.com](https://orbit.pethalvoid.com)  
> 📂 **Source Code:** [github.com/Ham144/warehouse-queue-management-system](https://github.com/Ham144/warehouse-queue-management-system)  
> 📊 **Scale & Impact:** Serves 12+ enterprise warehouse facilities, managing ~2,500+ monthly dock bookings with zero booking collisions.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-orbit.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://orbit.pethalvoid.com)
[![Source Code](https://img.shields.io/badge/Source%20Code-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/Ham144/warehouse-queue-management-system)
![NestJS](https://img.shields.io/badge/Backend-NestJS-E0234E?style=flat-square&logo=nestjs)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square&logo=postgresql)
![Redis](https://img.shields.io/badge/Cache-Redis%20(RedisIoAdapter)-DC382D?style=flat-square&logo=redis)
![Next.js](https://img.shields.io/badge/Frontend-Next.js-000000?style=flat-square&logo=nextdotjs)
![Playwright](https://img.shields.io/badge/Testing-Playwright-2EAD33?style=flat-square&logo=playwright)

A multi-tenant enterprise platform that optimizes warehouse loading/unloading dock schedules, manages carrier queues, and eliminates truck congestion through automated time-slot allocation.

<p align="center">
  <img src="assets/screenshots/wqms-realtime-drag-drop-area.webp" width="90%" alt="Real-time Drag & Drop Dock Queue Board" />
</p>

| Busy Time Management | Auto Time Picker |
| :---: | :---: |
| <img src="assets/screenshots/wqms-busy-time-management.webp" width="100%" alt="Busy Time Management" /> | <img src="assets/screenshots/wqms-auto-efficient-time-picker-support.webp" width="100%" alt="Auto Efficient Time Picker" /> |

| Multi-Tenancy Support | Multiple Warehouse Rules |
| :---: | :---: |
| <img src="assets/screenshots/wqms-multi-tenancy-support.webp" width="100%" alt="Multi-Tenancy Support" /> | <img src="assets/screenshots/wqms-multiple-warehouse-and-multiple-rules.webp" width="100%" alt="Multiple Warehouse Rules" /> |

| Driver & Duration Setup | Booking Approvals & History |
| :---: | :---: |
| <img src="assets/screenshots/wqms-driver-template-and-duration-setup.webp" width="100%" alt="Driver Fleet Setup" /> | <img src="assets/screenshots/wqms-booking-approval-and-history-booking.webp" width="100%" alt="Booking History" /> |

| Real-time Messenger | Organization Members |
| :---: | :---: |
| <img src="assets/screenshots/wqms-realtime-messanger.webp" width="100%" alt="Driver-Staff Messenger" /> | <img src="assets/screenshots/wqms-all-members-in-1-organization-management.webp" width="100%" alt="Organization Members" /> |

**Key capabilities:**
* **RedisIoAdapter Cluster WebSockets:** Custom `RedisIoAdapter` service scaling NestJS Socket.io gateways across multi-node server deployments for zero-latency live board updates (`booking.gateway.ts`).
* **Busy-Time Blackout Manager:** Dynamic slot allocation engine (`busy-time.service`) auto-blocking loading docks for warehouse maintenance, shift changes, or holiday breaks.
* **Collision-Free Queue Algorithm:** Prevents double-booking using Redis distributed cache locks and automatic open-slot suggestions.
* **Integrated Driver-Staff Messenger:** Real-time persistent WebSocket chat rooms between drivers and warehouse dispatchers (`chat.gateway.ts`).
* **Active Directory SSO:** Unique LDAP configuration per tenant organization.
* **E2E Testing:** Full Playwright test suite for critical booking workflows.

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

---

### 3. 📱 Super POS Mobile

> Offline-first mobile Point of Sale with dual outlet modes, multi-tier promo engine, thermal printing, and payment gateway  
> 🔗 **Live Web Application:** [pos.pethalvoid.com](https://pos.pethalvoid.com)  
> 📂 **Source Code:** [github.com/Ham144/super-pos-mobile](https://github.com/Ham144/super-pos-mobile)  
> 📊 **Scale & Impact:** Deployed across 40+ retail outlets & sales reps, processing ~15,000+ monthly transactions with zero transaction loss.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-pos.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://pos.pethalvoid.com)
[![Source Code](https://img.shields.io/badge/Source%20Code-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/Ham144/super-pos-mobile)
[![React Native](https://img.shields.io/badge/Mobile-React%20Native%200.76-61DAFB?style=flat-square&logo=react)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Framework-Expo%2052-000020?style=flat-square&logo=expo)](https://expo.dev/)
[![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)](https://www.mongodb.com/)
[![Midtrans](https://img.shields.io/badge/Payment-Midtrans%20(Indonesian%20Stripe)-002D62?style=flat-square)](https://midtrans.com/)

A high-performance, offline-first mobile Point of Sale application designed for sales representatives and retail outlet clerks, featuring local WiFi thermal printing, cashless payment gateway integration, and deep Microsoft Dynamics NAV ERP connectivity.

<p align="center">
  <img src="assets/screenshots/home.png" width="90%" alt="Super POS Mobile Dashboard" />
</p>

---

## 💼 Business Value & Real-World Impact

For mobile sales forces, field agents, or retail popups, internet connection drops shouldn't halt business. **Super POS Mobile** addresses this challenge by:
* **Offline-First Transactions**: Cashiers check out customers offline; transactions queue locally and sync automatically with the main office once a connection returns.
* **Direct Mobile Printing**: Sales reps print official invoices on-the-go to network/WiFi thermal printers directly from their phone.
* **Cashless Payments**: Accelerates checkouts using integrated Midtrans payment APIs (Indonesian Stripe) to process local electronic payments (QRIS, bank transfers, credit cards).
* **Flexible Promo Engine**: Evaluates active discount structures, item combos, and vouchers directly on the device.

---

## 🛠️ Tech Stack & Architecture

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

Super POS ships **three clients that talk to one Express backend**:
- **Mobile** — the field-facing POS, tuned for offline resilience and NAV-backed stock.
- **Web Admin** — catalog, promo/voucher configuration, sales reports, RBAC, and system settings.
- **Backend** — API gateway, sync engine, SOAP↔NAV bridge, payment orchestration, LDAP auth, and receipt/WhatsApp delivery.

### Mobile Client (Expo)
* **React Native (0.76) & Expo (52)**: Multi-platform mobile app development.
* **Expo Router (V4)**: Typed file-based routing.
* **NativeWind (V4)**: High-performance React Native styling based on Tailwind utility classes.
* **TCP Socket (`react-native-tcp-socket`)**: Direct network communication with thermal POS printers.
* **AsyncStorage & NetInfo**: Local offline database cache and connectivity listeners.

### Backend Server
* **Express.js (Node.js)**: API Gateway handling sync engines, promo evaluations, and transaction pipelines.
* **Mongoose (MongoDB)**: Document database for catalogs, outlet allocations, vouchers, and transactions.
* **ESC/POS & Node Thermal Printer**: Server-side layout builders for receipt generation.
* **Midtrans Client**: Payment settlement integration (Indonesian Stripe).

---

## 🚀 Key Architectural Features

### 1. Dual Outlet Modes: `offline` vs `stateless`

Every outlet is provisioned with an explicit `mode`, and the mobile app switches its entire data-flow strategy based on that flag. This lets one binary serve two very different retail realities:

| Aspect | `offline` mode | `stateless` mode |
|---|---|---|
| Intended use case | Event booths, pop-ups, unstable network locations | Permanent outlets integrated with the ERP warehouse |
| Source of truth for stock | Local `AsyncStorage` dump, reconciled on sync | **Microsoft Dynamics NAV** via SOAP (live) |
| Catalog fetch | Bulk paginated dump into `AsyncStorage` | Live partial fetch + infinite scroll per screen |
| Can sell without internet | **Yes** — transactions queue locally | **No** — cetak bill / bayar require connectivity |
| Sync engine | `syncronizeOfflineMode` → `/api/v1/sinkronisasi/sync-offline-mode` | Not used — every action hits NAV in real time |
| Bill endpoints | Local storage + sync mobile route | `/api/v1/stateless/{cetak-bill,edit-lines,bayar,void}` |
| Post-payment stock deduction | Local `updateInventoryAndStats` | Already reflected via NAV `WsPostInvoiceSO` |
| Discount below web price | Applied locally | Requires **pending approval** flow before shipment |
| Void flow | Local flag + sync | SOAP `GetSalesShipmentLines` → `WsUndoShipment` |

#### Offline mode — battle-tested sync pipeline

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

#### Stateless mode — always-online NAV integration

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

#### One codebase, two personas

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

The switch is driven by a single field on the outlet document — head office can migrate a booth from `offline` to `stateless` once permanent NAV connectivity is available, **no app reinstall required**.

### 2. Offline-to-Online Sync Pipeline (`syncMobile`) — offline mode only

When network connectivity returns on an outlet running in `offline` mode:
1. Mobile client tracks local sales registers and stock deductions in offline storage.
2. Once online, client initiates a sync process calling `POST /api/v1/sinkronisasi/sync-offline-mode`.
3. Backend resolves conflict checks, records transactions, and updates warehouse inventory balances.

Auto-sync respects an interval configured in `AsyncStorage.sinkronisasiInterval`, and is **skipped entirely for stateless outlets** since their state already lives on the server.

<p align="center">
  <img src="assets/screenshots/settlement-android-tab.png" width="90%" alt="Tablet POS Settlement Page" />
</p>

### 3. Network Thermal Printing
Generates ESC/POS command buffers and streams them over TCP sockets (WiFi/Ethernet) directly to configured printer IP addresses — no drivers or spoolers needed.

### 4. Dynamic API Configuration
Since field agents work across different local subnets, the app features an administrative settings modal where users can type, test, and save custom backend URL endpoints, stored securely via `AsyncStorage` and `react-native-keychain`.

### 5. Midtrans Payment Integration
Generates dynamic QRIS codes and payment links in-app, listening to webhook settlements to close open invoice bills automatically.

### 6. Enterprise Auth & Messaging (Web Admin)
* **LDAP / Active Directory** — accepts both local app accounts and AD users. First LDAP login auto-provisions a `Kasir` (or `Super Admin` for `description == "IT"`).
* **Fonnte WhatsApp Gateway** — pending receipts can be delivered directly to the customer's WhatsApp.
* **Configurable AD / SMTP / WhatsApp** — all three integrations are editable at runtime from the Application Setting menu; no redeploy needed to rotate credentials.

<p align="center">
  <img src="assets/screenshots/invoices-page.webp" width="48%" alt="Invoices List Page" />
  <img src="assets/screenshots/settlement-android-tab.png" width="48%" alt="Pending Invoice Bill Details" />
</p>

---

## 📸 Admin Dashboard & Operations Showcase

### 1. Promotional Rules & Vouchers
<p align="center">
  <img src="assets/screenshots/promo-page.webp" width="48%" alt="Promo Config" />
</p>

### 2. Purchase Orders (PO) Flow
<p align="center">
  <img src="assets/screenshots/purchase-order-create.webp" width="90%" alt="Create Purchase Order" />
</p>

### 3. Master Data & Analytics
<p align="center">
  <img src="assets/screenshots/sales-report.webp" width="48%" alt="Sales Performance Report" />
  <img src="assets/screenshots/library-page.png" width="48%" alt="Product Library Catalog" />
</p>

<p align="center">
  <img src="assets/screenshots/customer-database.webp" width="48%" alt="Customer Registry" />
  <img src="assets/screenshots/accounts-management.webp" width="48%" alt="Accounts & Users Management" />
</p>

### 4. Technical Stack Trace Reports
<p align="center">
  <img src="assets/screenshots/stack-trace.webp" width="90%" alt="Mobile Crash Logging & Stack Tracing" />
</p>

---

### 4. 🧠 Spaced Retention Bot & Cognitive AI Engine

> AI-powered cognitive manager, LLM note slicer, spaced repetition scheduler, and knowledge conflict guard  
> 📂 **Source Code:** [github.com/Ham144/principle-retention-bot](https://github.com/Ham144/principle-retention-bot)  
> 📊 **Scale & Impact:** Automates personal strategy retention, parses unstructured research notes with AI, and enforces decision consistency via automated Telegram dispatchers.

[![Source Code](https://img.shields.io/badge/Source%20Code-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/Ham144/principle-retention-bot)
![Next.js](https://img.shields.io/badge/Frontend-Next.js%2015-000000?style=flat-square&logo=nextdotjs)
![OpenRouter](https://img.shields.io/badge/AI-OpenRouter%20(Gemini%202.5%20Flash)-6366F1?style=flat-square&logo=openai)
![Telegram](https://img.shields.io/badge/Bot-Telegram%20Webhook-26A5E4?style=flat-square&logo=telegram)
![SQLite](https://img.shields.io/badge/Database-LibSQL%20%2F%20SQLite-003B57?style=flat-square&logo=sqlite)
![Vercel Cron](https://img.shields.io/badge/Scheduler-Vercel%20Cron-000000?style=flat-square&logo=vercel)

An intelligent knowledge management engine built to control cognitive capacity, eliminate decision fatigue, and enforce long-term memory retention using spaced repetition algorithms combined with LLM-powered note parsing.

**Key capabilities:**
* **LLM Note Slicing & Auto-Categorization:** Uses structured JSON mode (`response_format: { type: "json_object" }`) via OpenRouter (`google/gemini-2.5-flash`) to parse raw text dumps into core principles and auto-map them to domain threads (`pethalvoid`, `nutra`, `career-search`).
* **AI Conflict Guard:** Evaluates new rules against historical database entries in real-time. Duplicates are auto-bypassed, while contradictions trigger a side-by-side resolution panel. Low confidence scores held for manual review.
* **Spaced Repetition Engine (SuperMemo / Ebbinghaus Curve):** Computes memory decay intervals and dispatches automated reminder sessions via Telegram Webhook APIs.
* **Interactive Telegram Bot & Strategy Advisor:** Remote control via `/focus` (RAM slot management), `/load` (10-second contextual cheatsheets), `/review` (inline mastery checks), and `/tanya` (AI business strategy consultant filtering internet queries through custom principles).
* **Vercel Cron Integration:** Automated daily trigger pipeline executing spaced review dispatches with authorization header validation.

```mermaid
graph TB
    subgraph Ingress_Layer["Multi-Channel Ingress"]
        Dashboard["Next.js 15 App Router Dashboard"]
        TG_Hook["Telegram Bot Webhook Endpoint"]
    end

    subgraph AI_Intelligence["AI Agent & Conflict Engine"]
        Slicer["LLM Note Slicer (OpenRouter / Gemini 2.5)"]
        Guard["Side-by-Side Conflict & Duplicate Evaluator"]
        Consult["AI Contextual Strategy Advisor"]
    end

    subgraph Memory_Engine["Retention Core & Storage"]
        Spaced["SuperMemo / Ebbinghaus Spaced Repetition Engine"]
        DB[(LibSQL / SQLite Database)]
    end

    subgraph Automation["Background Dispatcher"]
        Cron["Vercel Daily Cron Worker"]
        Dispatch["Telegram Interactive Session Dispatcher"]
    end

    Dashboard -->|Raw Text Dump| Slicer
    TG_Hook -->|Commands / Log| Slicer
    Slicer --> Guard
    Guard -->|Validation Passed| DB
    Guard -->|Contradiction Detected| Dashboard
    Dashboard -->|Query AI| Consult
    Cron -->|Daily Trigger| Spaced
    Spaced -->|Due Principles| DB
    Spaced -->|Build Reminders| Dispatch
    Dispatch -->|Interactive Keyboards| TG_Hook
```

---

### 5. 📦 Inventory Audit System

> Physical stock auditing, high-concurrency ioredis caching, barcode scanning, and recount delegation dashboard  
> 📂 **Source Code:** [github.com/Ham144/inventory-audit-system](https://github.com/Ham144/inventory-audit-system)  
> 📊 **Scale & Impact:** Reconciles physical warehouse inventory across 100,000+ total SKU line items annually with automated discrepancy flagging.

[![Source Code](https://img.shields.io/badge/Source%20Code-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/Ham144/inventory-audit-system)
![React Router v7](https://img.shields.io/badge/Framework-React%20Router%20v7-CA4245?style=flat-square&logo=reactrouter)
![Tailwind CSS v4](https://img.shields.io/badge/Styling-Tailwind%20v4-06B6D4?style=flat-square&logo=tailwindcss)
![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square&logo=postgresql)
![Redis](https://img.shields.io/badge/Cache-Redis%20(ioredis)-DC382D?style=flat-square&logo=redis)

A high-concurrency inventory reconciliation platform that automates physical count tracking, computes stock discrepancies against ERP ledgers, and manages recount delegation workflows.

**Key capabilities:**
* **High-Concurrency ioredis Caching:** Custom `ioredis` service caching hot SKU catalog filters, rack mappings (`office-mapping.ts`), and scan approval logs for instant barcode verification.
* **Digital Scan Logging:** Warehouse operators scan barcodes and register physical counts mapped to specific shelves, racks, and warehouse branches in real-time.
* **Discrepancy Reconciliation Engine:** Automatically sums physical logs per SKU/rack and compares against ERP system values — flagging items as `MATCHED` or `DISCREPANCY`.
* **Recount Delegation Workflow:** Audit managers delegate specific discrepant items to operators for blind recounts, or apply authorized correction overrides with full audit logging.
* **Active Directory SSO:** Corporate LDAP authentication for large warehouse user management.

```mermaid
graph TB
    subgraph Warehouse_Floor["Warehouse Floor Operations"]
        BarcodeScanner["Barcode Scanner & Mobile Web App"]
        ScanBuffer["Real-time Rack Scan Buffer"]
    end

    subgraph Reconciliation_Gateway["Backend API & Caching"]
        ExpressGateway["Express.js API Gateway"]
        RedisCache["ioredis High-Concurrency Cache Store"]
        LDAP["Active Directory Corporate SSO"]
    end

    subgraph Discrepancy_Engine["Reconciliation & Delegation Core"]
        PrismaORM["Prisma ORM Query Engine"]
        DiscrepancyCalc["Physical vs Ledger Discrepancy Engine"]
        DelegationWorkflow["Blind Recount Delegation Manager"]
        OpnameCron["Automated Stock Opname Cron Scheduler"]
        Postgres[(PostgreSQL Master DB)]
    end

    BarcodeScanner -->|Scan Item Barcode & Rack ID| ScanBuffer
    ScanBuffer --> ExpressGateway
    ExpressGateway -->|Auth Staff| LDAP
    ExpressGateway <-->|Cache Hot Inventory & Racks| RedisCache
    ExpressGateway --> DiscrepancyCalc
    DiscrepancyCalc -->|Compare Physical Qty vs ERP Ledger| PrismaORM
    PrismaORM --> Postgres
    DiscrepancyCalc -->|Discrepancy Detected| DelegationWorkflow
    DelegationWorkflow -->|Trigger Re-Scan Request| BarcodeScanner
    OpnameCron -->|Periodic Audit Snapshot| Postgres
```

---

### 6. 🗺️ Field Sales CRM (S-BIT)

> Location-verified sales routing and client order-taking CRM with dual-backend ERP microservices  
> 📊 **Scale & Impact:** Tracks 50+ active field sales reps, auditing ~3,000+ geofenced client visits monthly with direct MS Dynamics NAV ERP synchronization.

![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react)
![Express.js](https://img.shields.io/badge/Primary%20Backend-Express.js-000000?style=flat-square&logo=express)
![SO Microservice](https://img.shields.io/badge/SO%20Microservice-MIDCSI%20Backend-FF6C37?style=flat-square&logo=node.js)
![Leaflet](https://img.shields.io/badge/Mapping-Leaflet%20GPS-199900?style=flat-square&logo=leaflet)
![WhatsApp](https://img.shields.io/badge/Notifications-WhatsApp-25D366?style=flat-square&logo=whatsapp)
![Dynamics NAV](https://img.shields.io/badge/ERP-MS%20Dynamics%20NAV-0078D4?style=flat-square)

An enterprise-grade Field Sales CRM for route planning, real-time GPS visit tracking, automated WhatsApp notifications, and deep Microsoft Dynamics NAV ERP integration operating on a decoupled **Dual-Backend Microservice Architecture**.

<p align="center">
  <img src="assets/screenshots/sbit-home.png" width="90%" alt="Field Sales CRM Dashboard" />
</p>

**Key capabilities:**
* **Dual-Backend Microservice Architecture:** Decouples core CRM operations (visits, geofencing, agendas) from the specialized Sales Order (SO) & ERP Integration Microservice (`MIDCSI Backend`) for maximum fault tolerance and isolated scaling.
* **GPS Geofence Auditing:** Records real-time GPS coordinates during sales visits (Leaflet maps), eliminating fake check-ins.
* **Dynamics NAV ERP Sync:** Hourly NTLM v2 SOAP XML cron jobs query ERP endpoints to synchronize customer master data, credit limits, sales targets, and push field-generated Sales Orders.
* **Automated WhatsApp Dispatcher:** Sends order confirmations and visit receipts directly to customer WhatsApp contacts via `whatsapp-web.js`.
* **Dynamic Audit Forms:** Admins modify required visit questions (photo uploads, stock counts) without redeploying code.
* **Sales Analytics:** Recharts-powered dashboards for target tracking and performance reporting.

```mermaid
graph TB
    subgraph Mobile_Client["Field Sales Web Application"]
        SalesUI["React + Vite Single Page App"]
        GPSModule["Leaflet Geofence Verification Engine"]
        FormBuilder["Dynamic Visit Audit Form Engine"]
    end

    subgraph Primary_Backend["Primary CRM Backend Gateway (Node.js/Express)"]
        CRM_API["CRM Core API Controller"]
        VisitEngine["Customer Visit & Agenda Manager"]
        WA_Dispatcher["WhatsApp Web Dispatcher (whatsapp-web.js)"]
        MongoDB[(MongoDB Master Database)]
    end

    subgraph SO_Microservice["Sales Order (SO) Microservice Backend (MIDCSI)"]
        SO_Gateway["Sales Order Gateway & Proxy"]
        NTLM_Auth["NTLM v2 SOAP Authentication Service"]
        CronSync["Hourly ERP Sync Engine"]
    end

    subgraph Enterprise_ERP["Enterprise ERP Infrastructure"]
        DynamicsERP[(MS Dynamics NAV ERP)]
        ClientWA[Client WhatsApp Contacts]
    end

    SalesUI -->|Check-in GPS & Visit Audits| CRM_API
    GPSModule -->|Verified Coordinates| CRM_API
    FormBuilder -->|Dynamic Form Logs| CRM_API
    CRM_API <-->|Mongoose ODM| MongoDB
    CRM_API -->|Dispatch Receipts| WA_Dispatcher
    WA_Dispatcher -->|Automated WA Message| ClientWA

    SalesUI -->|Submit Sales Orders| SO_Gateway
    SO_Gateway <-->|NTLM v2 Encrypted SOAP XML| DynamicsERP
    CronSync <-->|Hourly Sync: Customers & Credit Limits| DynamicsERP
    CronSync -->|Update Local Master Data| MongoDB
```

---

### 🤝 Let's Connect

* 💼 **LinkedIn:** [linkedin.com/in/muhammad-yafizham-batubara](https://www.linkedin.com/in/muhammad-yafizham-batubara/)
* 📧 **Email:** [24434muhammad.yafizham@gmail.com](mailto:24434muhammad.yafizham@gmail.com)
* 💬 **WhatsApp:** [+62 838-5402-6650](https://wa.me/6283854026650)
* 📸 **Instagram:** [@yafizhambb](https://www.instagram.com/yafizhambb)

