# Hi, I'm Muhammad Yafizham 👋
### AI & Full-Stack Software Engineer | Enterprise Systems & LLM Workflows

I am a Software Engineer at PT Catur Sukses Internasional with a proven track record of single-handedly architecting, deploying, and operating **14+ enterprise production systems** across logistics, AI agent workflows, sales routing, and backend automation. Fluent in English, I specialize in building production AI/LLM pipelines, high-concurrency backend services, real-time logistics engines, and enterprise ERP integrations.

[📄 Download My Resume (PDF)](https://github.com/Ham144/Ham144/raw/main/Resume_Muhammad_Yafizham_Batubara.pdf) | [💼 LinkedIn](https://www.linkedin.com/in/muhammad-yafizham-batubara/)

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
| **Backend & APIs** | NestJS, Express.js, Node.js, FastAPI, RESTful APIs, WebSockets (RedisIoAdapter), SOAP/NTLM |
| **Databases & Caching** | PostgreSQL, MongoDB, Redis (ioredis), SQLite/LibSQL, Prisma ORM, Mongoose, Pgvector |
| **Frontend & Mobile** | React 18, Next.js 15, React Native 0.76, Expo 52, React Flow, Tailwind CSS v4, Zustand |
| **Infrastructure & DevOps** | Docker, Linux VPS, Nginx, CI/CD (GitHub Actions), LDAP/Active Directory |
| **Integrations** | MS Dynamics NAV (ERP), Midtrans Payment Gateway, Cloudflare R2 / Turnstile, Telegram Bot API, WhatsApp Web API |

---

> 🔒 **Proprietary Commercial IP & Source Code Notice:**
> The source code for the flagship platforms featured below represents proprietary commercial IP owned and architected by Muhammad Yafizham (Founder & Principal Systems Architect). All source repositories are strictly **Private** to protect custom engines, business logic, and commercial licensing rights.
> 
> Full architectural specifications, system design diagrams, UI screenshot galleries, and **Live Production Web Applications** are available below for evaluation. Private code audits or temporary read-only repository access can be arranged for technical hiring evaluations under mutual non-disclosure agreements (NDA).

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
  <img src="assets/screenshots/approval-app.jpeg" width="48%" alt="Approva.ai Application" />
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

### 2. 🧠 Spaced Retention Bot & Cognitive AI Engine

> AI-powered cognitive manager, LLM note slicer, spaced repetition scheduler, and knowledge conflict guard  
> 🔗 **Live Web Application:** [retention.pethalvoid.com](https://retention.pethalvoid.com)  
> 📊 **Scale & Impact:** Automates personal strategy retention, parses unstructured research notes with AI, and enforces decision consistency via automated Telegram dispatchers.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-retention.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://retention.pethalvoid.com)
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

### 3. 🗓️ Warehouse Queue Management System (WQMS)

> Real-time loading dock booking, RedisIoAdapter WebSocket cluster, and Gantt board carrier scheduler  
> 🔗 **Live Web Application:** [orbit.pethalvoid.com](https://orbit.pethalvoid.com)  
> 📊 **Scale & Impact:** Serves 12+ enterprise warehouse facilities, managing ~2,500+ monthly dock bookings with zero booking collisions.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-orbit.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://orbit.pethalvoid.com)
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

### 4. 🗺️ Field Sales CRM (S-BIT)

> Location-verified sales routing and client order-taking CRM with dual-backend ERP microservices  
> 🔗 **Live Web Application:** [sfa.pethalvoid.com](https://sfa.pethalvoid.com)  
> 📊 **Scale & Impact:** Tracks 50+ active field sales reps, auditing ~3,000+ geofenced client visits monthly with direct MS Dynamics NAV ERP synchronization.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-sfa.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://sfa.pethalvoid.com)
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

### 5. 📱 Super POS Mobile

> Offline-first mobile Point of Sale with multi-tier promo engine, thermal printing, and payment gateway  
> 🔗 **Live Web Application:** [pos.pethalvoid.com](https://pos.pethalvoid.com)  
> 📊 **Scale & Impact:** Deployed across 40+ retail outlets & sales reps, processing ~15,000+ monthly transactions with zero transaction loss.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-pos.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://pos.pethalvoid.com)
![React Native](https://img.shields.io/badge/Mobile-React%20Native%200.76-61DAFB?style=flat-square&logo=react)
![Expo](https://img.shields.io/badge/Framework-Expo%2052-000020?style=flat-square&logo=expo)
![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)
![Midtrans](https://img.shields.io/badge/Payment-Midtrans-002D62?style=flat-square)

A high-performance mobile POS application for sales representatives and retail outlet clerks, featuring offline transaction queueing, direct WiFi thermal printing, and cashless payment integration.

<p align="center">
  <img src="assets/screenshots/home.png" width="90%" alt="Super POS Mobile Dashboard" />
</p>

| Tablet Settlement | Invoice Management |
| :---: | :---: |
| <img src="assets/screenshots/settlement-android-tab.png" width="100%" alt="Settlement Page" /> | <img src="assets/screenshots/invoices-page.webp" width="100%" alt="Invoices List" /> |

| Pending Invoice | Product Library |
| :---: | :---: |
| <img src="assets/screenshots/pending-invoice.webp" width="100%" alt="Pending Bill" /> | <img src="assets/screenshots/library-page.png" width="100%" alt="Product Catalog" /> |

| Promotions & Vouchers | Sales Analytics |
| :---: | :---: |
| <img src="assets/screenshots/promo-page.webp" width="100%" alt="Promo Config" /> | <img src="assets/screenshots/sales-report.webp" width="100%" alt="Sales Report" /> |

| Purchase Orders | Accounts Management |
| :---: | :---: |
| <img src="assets/screenshots/purchase-order-create.webp" width="100%" alt="PO Creation" /> | <img src="assets/screenshots/accounts-management.webp" width="100%" alt="Accounts" /> |

| Customer Database | Crash Stack Traces |
| :---: | :---: |
| <img src="assets/screenshots/customer-database.webp" width="100%" alt="Customer Registry" /> | <img src="assets/screenshots/stack-trace.webp" width="100%" alt="Stack Tracing" /> |

**Key capabilities:**
* **Multi-Layer Voucher & Promo Engine:** Middleware evaluation stack (`checkDiskon`, `checkPromo`, `checkVoucher`, `generateVoucherCheck`) validating multi-tier vouchers, item bundle discounts, and outlet-specific rules.
* **Offline-First Sync Engine:** Transactions complete fully offline in `AsyncStorage`, then auto-reconcile with the central MongoDB server once connectivity returns.
* **Direct ESC/POS Thermal Printing:** Generates raw ESC/POS command buffers and streams them over TCP sockets to network/WiFi thermal printers — no drivers or spoolers needed.
* **Midtrans Payment Gateway:** Generates dynamic QRIS codes and payment links in-app with automated webhook settlement listeners.
* **Automated Invoice & Voucher Crons:** Background cron services (`emailKwitansi.js`, `pengirimanVoucherCode.js`) dispatching automated PDF receipts and digital voucher dispatches to customers.

```mermaid
graph TB
    subgraph Mobile_Device["Mobile Client (Expo 52 + React Native 0.76)"]
        MobileUI["POS Mobile Interface"]
        OfflineQueue["AsyncStorage Offline Transaction Queue"]
        PrinterDriver["Raw ESC/POS Buffer & Direct TCP Socket Streamer"]
        VoucherEngine["On-Device Voucher & Ledger Lock Service"]
    end

    subgraph Local_Hardware["Retail Hardware Layer"]
        ThermalPrinter["WiFi / Network Thermal Receipt Printer"]
    end

    subgraph Backend_Cloud["Central Cloud Services & Promo Engine"]
        ExpressServer["Express.js API Gateway"]
        PromoStack["Promo, Diskon & Voucher Middleware Stack"]
        SyncService["Auto Reconciler & Conflict Resolver"]
        MongoDB[(MongoDB Master Database)]
        Midtrans["Midtrans QRIS Payment Gateway"]
        CronServices["Automated Kwitansi & Voucher Cron Jobs"]
    end

    MobileUI -->|Cashier Checkout| OfflineQueue
    MobileUI -->|Generate ESC/POS Bytes| PrinterDriver
    PrinterDriver -->|TCP Socket Raw Buffer| ThermalPrinter
    OfflineQueue -->|Connection Restored| SyncService
    SyncService --> ExpressServer
    ExpressServer --> PromoStack
    PromoStack --> MongoDB
    ExpressServer <-->|QRIS Webhooks| Midtrans
    CronServices -->|Send PDF Receipt & Vouchers| Customer[Customer Email / Phone]
    MobileUI <-->|Online Voucher Check| VoucherEngine
```

---

### 6. 📦 Inventory Audit System

> Physical stock auditing, high-concurrency ioredis caching, barcode scanning, and recount delegation dashboard  
> 🔗 **Live Web Application:** [inventory.pethalvoid.com](https://inventory.pethalvoid.com)  
> 📊 **Scale & Impact:** Reconciles physical warehouse inventory across 100,000+ total SKU line items annually with automated discrepancy flagging.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-inventory.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://inventory.pethalvoid.com)
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

### 🤝 Let's Connect

* 💼 **LinkedIn:** [linkedin.com/in/muhammad-yafizham-batubara](https://www.linkedin.com/in/muhammad-yafizham-batubara/)
* 📧 **Email:** [24434muhammad.yafizham@gmail.com](mailto:24434muhammad.yafizham@gmail.com)
* 💬 **WhatsApp:** [+62 838-5402-6650](https://wa.me/6283854026650)
* 📸 **Instagram:** [@yafizhambb](https://www.instagram.com/yafizhambb)
* 🏢 **Business:** [pethalvoid.com](https://pethalvoid.com)
