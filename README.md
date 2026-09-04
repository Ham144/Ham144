# Hi, I'm Muhammad Yafizham 👋
### AI & Full-Stack Software Engineer | Enterprise Systems & LLM Workflows

I am a Software Engineer at PT Catur Sukses Internasional with a proven track record of single-handedly architecting, deploying, and operating **14+ enterprise production systems** across logistics, AI agent workflows, sales routing, and backend automation. Fluent in English (**IELTS Band 7**), I specialize in building production AI/LLM pipelines, high-concurrency backend services, real-time logistics engines, and enterprise ERP integrations.

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
| **AI & LLM Workflows** | OpenRouter, OpenAI APIs, LangChain, LangGraph, Spaced Repetition Algorithms, Telegram Bot Webhooks |
| **Backend & APIs** | NestJS, Express.js, Node.js, FastAPI, RESTful APIs, WebSockets, SOAP/NTLM |
| **Databases & Caching** | PostgreSQL, MongoDB, Redis, SQLite/LibSQL, Prisma ORM, Mongoose, Pgvector |
| **Frontend & Mobile** | React, Next.js, React Native, Expo, React Flow, Tailwind CSS, Zustand |
| **Infrastructure & DevOps** | Docker, Linux VPS, Nginx, CI/CD (GitHub Actions), LDAP/Active Directory |
| **Integrations** | MS Dynamics NAV (ERP), Midtrans Payment Gateway, Cloudflare R2, Telegram Bot API, WhatsApp Web API |

---

> 🔒 **Proprietary Commercial IP & Source Code Notice:**
> The source code for the flagship platforms featured below represents proprietary commercial IP owned and architected by Muhammad Yafizham (Founder & Principal Systems Architect). All source repositories are strictly **Private** to protect custom engines, business logic, and commercial licensing rights.
> 
> Full architectural specifications, system design diagrams, UI screenshot galleries, and **Live Production Web Applications** are available below for evaluation. Private code audits or temporary read-only repository access can be arranged for technical hiring evaluations under mutual non-disclosure agreements (NDA).

---

## Featured Production Projects

---

### 1. 🔄 Approval Workflow Engine (Approva.ai)

> Dynamic multi-tenant approval system with a visual drag-and-drop workflow designer  
> 🔗 **Live Web Application:** [approva-ai.hexadim.com](https://approva-ai.hexadim.com)  
> 📊 **Scale & Impact:** Adopted across 5+ corporate departments, automating 800+ multi-tier approval workflows monthly.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-approva--ai.hexadim.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://approva-ai.hexadim.com)
![React Flow](https://img.shields.io/badge/Frontend-React%20Flow%20V11-FF007A?style=flat-square&logo=react)
![React](https://img.shields.io/badge/UI-React%2018-61DAFB?style=flat-square&logo=react)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=flat-square&logo=nodedotjs)
![Active Directory](https://img.shields.io/badge/Auth-LDAP%20%2F%20Active%20Directory-0078D4?style=flat-square&logo=windows)

Replaces hardcoded business approval paths with a visual graph editor. Administrators configure conditional routing (e.g., auto-escalate when purchase value exceeds threshold) with digital signatures and multi-channel alert dispatches.

<p align="center">
  <img src="assets/screenshots/approval-interactive-workflow.png" width="90%" alt="Interactive Workflow Hub" />
</p>

<p align="center">
  <img src="assets/screenshots/approval-app.jpeg" width="48%" alt="Approva.ai Application" />
  <img src="assets/screenshots/approval-motto.png" width="48%" alt="Approva.ai Branding" />
</p>

**Key capabilities:**
* **Visual Workflow Designer:** Drag-and-drop graph nodes (React Flow V11) to build multi-tier approval chains — no code changes, no redeployment.
* **Conditional Routing Engine:** Evaluates submitter roles, transaction values, and department rules to dynamically route each approval request.
* **Corporate SSO:** Authenticates via local Active Directory (LDAP) for unified enterprise identity management.
* **Multi-Channel Notifications:** Dispatches real-time alerts through Telegram Bot API and SMTP email upon each approval stage transition.
* **Digital Signatures & Audit Trail:** Every approval step is cryptographically signed and logged for compliance.

```mermaid
graph TD
    User[React Flow V11 Frontend] -->|Visual Graph Specs| API[Node.js Workflow Gateway]
    API -->|LDAP Protocol| AD[Active Directory]
    API -->|Condition Evaluator| Engine[Approval Decision Engine]
    Engine -->|Webhooks| Telegram[Telegram Bot Alerts]
    Engine -->|SMTP| Mail[Email Notifications]
```

---

### 2. 🧠 Spaced Retention Bot & Cognitive AI Engine

> AI-powered cognitive manager, spaced repetition scheduler, and knowledge conflict guard  
> 🔗 **Live Web Application:** [retention.pethalvoid.com](https://retention.pethalvoid.com)  
> 📊 **Scale & Impact:** Automates personal strategy retention, parses unstructured research notes with AI, and enforces decision consistency via automated Telegram dispatchers.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-retention.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://retention.pethalvoid.com)
![Next.js](https://img.shields.io/badge/Frontend-Next.js%2015-000000?style=flat-square&logo=nextdotjs)
![OpenRouter](https://img.shields.io/badge/AI-OpenRouter%20LLM-6366F1?style=flat-square&logo=openai)
![Telegram](https://img.shields.io/badge/Bot-Telegram%20Webhook-26A5E4?style=flat-square&logo=telegram)
![SQLite](https://img.shields.io/badge/Database-SQLite%20%2F%20LibSQL-003B57?style=flat-square&logo=sqlite)
![Vercel Cron](https://img.shields.io/badge/Scheduler-Vercel%20Cron-000000?style=flat-square&logo=vercel)

An intelligent knowledge management engine built to control cognitive capacity, eliminate decision fatigue, and enforce long-term memory retention using spaced repetition algorithms combined with LLM-powered note parsing.

**Key capabilities:**
* **AI Note Slicing & Auto-Categorization:** Automatically processes raw research notes or strategic logs, structuring them into core principles and mapping them to domain threads using OpenRouter LLMs.
* **AI Conflict Guard:** Prevents duplicate or contradictory strategic rules by performing side-by-side AI evaluation against historical database entries before persisting.
* **Spaced Repetition Engine (SuperMemo / Ebbinghaus Curve):** Computes optimal review intervals and dispatches automated reminder sessions via Telegram Webhook APIs.
* **Interactive Telegram Bot Interface:** Full remote control via `/focus` (RAM slot management), `/load` (10-second contextual cheatsheets), `/review` (inline mastery checks), and `/tanya` (AI business strategy consult).
* **Vercel Cron Integration:** Automated daily trigger pipeline executing spaced review dispatches with authorization header validation.

```mermaid
graph TD
    User[Web Dashboard / Telegram Bot] -->|Raw Research / Commands| Gateway[Next.js App Router API]
    Gateway <-->|Structured JSON| OpenRouter[OpenRouter LLM Engine]
    Gateway -->|Conflict Check| ConflictGuard[AI Contradiction Evaluator]
    ConflictGuard -->|Persist Principles| DB[(SQLite / LibSQL Database)]
    Cron[Vercel Daily Cron Job] -->|Trigger Interval Session| SpacedEngine[Spaced Repetition Algorithm]
    SpacedEngine -->|Webhook Dispatch| Telegram[Telegram Bot API]
```

---

### 3. 🗓️ Warehouse Queue Management System (WQMS)

> Real-time loading dock booking and Gantt board carrier scheduler  
> 🔗 **Live Web Application:** [orbit.pethalvoid.com](https://orbit.pethalvoid.com)  
> 📊 **Scale & Impact:** Serves 12+ enterprise warehouse facilities, managing ~2,500+ monthly dock bookings with zero booking collisions.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-orbit.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://orbit.pethalvoid.com)
![NestJS](https://img.shields.io/badge/Backend-NestJS-E0234E?style=flat-square&logo=nestjs)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square&logo=postgresql)
![Redis](https://img.shields.io/badge/Cache-Redis-DC382D?style=flat-square&logo=redis)
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
* **Dock Allocation Algorithm:** Prevents double-booking using Redis distributed cache locks and automatic collision resolution.
* **Live Gantt Board:** Warehouse guards and dock managers see real-time drag-and-drop queue boards via WebSocket updates.
* **Pre-Booking Portal:** Vendors and drivers reserve specific arrival time slots, reducing unscheduled congestion.
* **Real-time Messenger:** Persistent, authenticated chat rooms between drivers and warehouse dispatchers.
* **Active Directory SSO:** Unique LDAP configuration per tenant organization.
* **E2E Testing:** Full Playwright test suite for critical booking workflows.

```mermaid
graph TD
    Carrier[Carrier / Driver] -->|Pre-Booking| Portal[Driver Portal - Next.js]
    Portal --> Gateway[NestJS API Gateway]
    Gateway --> QueueEngine[Dock Allocation Engine]
    QueueEngine --> RedisCache[(Redis Lock & Queue)]
    QueueEngine --> DB[(PostgreSQL)]
    QueueEngine -->|WebSockets| Display[Gate Display & Guard Monitor]
```

---

### 4. 🗺️ Field Sales CRM (S-BIT)

> Location-verified sales routing and client order-taking CRM with ERP integration  
> 🔗 **Live Web Application:** [sfa.pethalvoid.com](https://sfa.pethalvoid.com)  
> 📊 **Scale & Impact:** Tracks 50+ active field sales reps, auditing ~3,000+ geofenced client visits monthly with direct MS Dynamics NAV ERP synchronization.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-sfa.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://sfa.pethalvoid.com)
![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react)
![Express.js](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![Leaflet](https://img.shields.io/badge/Mapping-Leaflet%20GPS-199900?style=flat-square&logo=leaflet)
![WhatsApp](https://img.shields.io/badge/Notifications-WhatsApp-25D366?style=flat-square&logo=whatsapp)
![Dynamics NAV](https://img.shields.io/badge/ERP-MS%20Dynamics%20NAV-0078D4?style=flat-square)

An enterprise-grade Field Sales CRM for route planning, real-time GPS visit tracking, automated WhatsApp notifications, and deep Microsoft Dynamics NAV ERP integration.

<p align="center">
  <img src="assets/screenshots/sbit-home.png" width="90%" alt="Field Sales CRM Dashboard" />
</p>

**Key capabilities:**
* **GPS Geofence Auditing:** Records real-time GPS coordinates during sales visits (Leaflet maps), eliminating fake check-ins.
* **Dynamics NAV ERP Sync:** Hourly SOAP/NTLM cron jobs synchronize customer registers, credit limits, sales targets, and push field-generated orders back to ERP.
* **Automated WhatsApp Dispatcher:** Sends order confirmations and visit receipts directly to customer WhatsApp contacts via `whatsapp-web.js`.
* **Dynamic Audit Forms:** Admins modify required visit questions (photo uploads, stock counts) without redeploying code.
* **Sales Analytics:** Recharts-powered dashboards for target tracking and performance reporting.

```mermaid
graph TD
    Client[React + Leaflet GPS] <-->|REST / HTTPS| Backend[Express API Gateway]
    Backend <-->|SOAP + NTLM| ERP[Microsoft Dynamics NAV]
    Backend -->|WhatsApp Web| WA[Customer WhatsApp Dispatcher]
    Backend <-->|Mongoose| DB[(MongoDB)]
```

---

### 5. 📱 Super POS Mobile

> Offline-first mobile Point of Sale with direct thermal printing and payment gateway  
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
* **Offline-First Sync Engine:** Transactions complete fully offline in `AsyncStorage`, then auto-reconcile with the central MongoDB server once connectivity returns.
* **Direct ESC/POS Thermal Printing:** Generates raw ESC/POS command buffers and streams them over TCP sockets to network/WiFi thermal printers — no drivers or spoolers needed.
* **Midtrans Payment Gateway:** Generates dynamic QRIS codes and payment links in-app with automated webhook settlement listeners.
* **Promo & Discount Engine:** Evaluates multi-tier vouchers, item bundles, and outlet-specific discounts locally on-device.
* **Dynamic API Configuration:** Field agents configure and test custom backend URLs per subnet via an admin settings modal.

```mermaid
graph TD
    Client[Expo 52 Mobile Client] <-->|Sync Engine / REST| Server[Express API Server]
    Client -->|TCP Socket| Printer[WiFi Thermal POS Printer]
    Server <-->|Mongoose| DB[(MongoDB)]
    Server <-->|REST API| Midtrans[Midtrans Payment Gateway]
```

---

### 6. 📦 Inventory Audit System

> Physical stock auditing, barcode scanning, and recount delegation dashboard  
> 🔗 **Live Web Application:** [inventory.pethalvoid.com](https://inventory.pethalvoid.com)  
> 📊 **Scale & Impact:** Reconciles physical warehouse inventory across 100,000+ total SKU line items annually with automated discrepancy flagging.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-inventory.pethalvoid.com-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://inventory.pethalvoid.com)
![React Router v7](https://img.shields.io/badge/Framework-React%20Router%20v7-CA4245?style=flat-square&logo=reactrouter)
![Tailwind CSS v4](https://img.shields.io/badge/Styling-Tailwind%20v4-06B6D4?style=flat-square&logo=tailwindcss)
![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square&logo=postgresql)
![Redis](https://img.shields.io/badge/Cache-Redis-DC382D?style=flat-square&logo=redis)

A high-concurrency inventory reconciliation platform that automates physical count tracking, computes stock discrepancies against ERP ledgers, and manages recount delegation workflows.

**Key capabilities:**
* **Digital Scan Logging:** Operators scan barcodes and register physical counts mapped to specific shelves, racks, and warehouse branches in real-time.
* **Discrepancy Reconciliation Engine:** Automatically sums physical logs per SKU/rack and compares against ERP system values — flagging items as `MATCHED` or `DISCREPANCY`.
* **Recount Delegation Workflow:** Audit managers delegate specific discrepant items to operators for blind recounts, or apply authorized correction overrides with full audit logging.
* **Active Directory SSO:** Corporate LDAP authentication for large warehouse user management.

```mermaid
graph TD
    Scanner[Barcode Operator] -->|Scan Logs| App[React Router v7 Frontend]
    App --> Gateway[Express API Server]
    Gateway <-->|Prisma ORM| DB[(PostgreSQL)]
    Gateway <-->|ioredis| Redis[(Redis Cache)]
    Gateway -->|LDAP| AD[Active Directory]
```

---

### 🤝 Let's Connect

* 💼 **LinkedIn:** [linkedin.com/in/muhammad-yafizham-batubara](https://www.linkedin.com/in/muhammad-yafizham-batubara/)
* 📧 **Email:** [24434muhammad.yafizham@gmail.com](mailto:24434muhammad.yafizham@gmail.com)
* 💬 **WhatsApp:** [+62 838-5402-6650](https://wa.me/6283854026650)
* 📸 **Instagram:** [@yafizhambb](https://www.instagram.com/yafizhambb)
* 🏢 **Business:** [pethalvoid.com](https://pethalvoid.com)
