# Hi, I'm Muhammad Yafizham 👋
### AI Engineer | Backend, Agentic AI & LLM Systems Specialist

I specialize in building production AI systems, agentic workflows, RAG pipelines, and high-performance enterprise backend architectures. Fluent in English (IELTS Band 7), I have a proven track record of designing, deploying, and maintaining 14+ production business applications as a sole engineer.

[📄 Download My Resume (PDF)](https://github.com/Ham144/Ham144/raw/main/Resume_Muhammad_Yafizham_Batubara.pdf) | [💼 LinkedIn](https://www.linkedin.com/in/muhammad-yafizham-batubara/)

---

### 🛠️ Core Technology Stack

| Focus Area | Technologies |
| :--- | :--- |
| **Agentic AI & LLM Systems** | Python, LangGraph, LangChain, RAG Pipelines, Vector Databases (Pgvector, Qdrant), Langfuse Tracing, Token/Cost Monitoring |
| **Backend & Databases** | NestJS, FastAPI, Node.js, Express.js, Pydantic, PostgreSQL, MongoDB, Redis, RESTful APIs, WebSockets |
| **Frontend & Mobile** | React, Next.js, React Native, Expo, React Flow, Tailwind CSS (v3/v4), Zustand |
| **Infrastructure & DevOps** | Docker, Linux VPS, Nginx, CI/CD Pipelines (GitHub Actions), LDAP/Active Directory |

---

### 📈 GitHub Stats & Analytics

<p align="left">
  <img src="https://github-readme-stats-eight-theta.vercel.app/api?username=Ham144&show_icons=true&theme=tokyonight&count_private=true" alt="Ham144's GitHub Stats" height="180px" />
  <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=Ham144&layout=compact&theme=tokyonight&langs_count=6" alt="Ham144's Top Languages" height="180px" />
</p>

---

> 🔒 **Notice on Codebase Visibility & IP Protection:**  
> The underlying production source codes for the flagship projects below have been transitioned to **Private Repositories** to protect proprietary business logic, custom AI engines, and enterprise IP. The complete architectural specifications, system design diagrams, technical highlights, screenshot galleries, and documentation are unified below as the primary public showcase etalase. Code review access can be requested for technical evaluations.

---

## 🏛️ Master Showcase — Flagship Projects

---

### 1. 🔄 Approval Workflow Engine AI
> **Dynamic Multi-Tenant Approval System with Visual Drag-and-Drop Workflow Designer**

![React Flow](https://img.shields.io/badge/Frontend-React%20Flow%20V11-FF007A?style=flat-square&logo=react)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=flat-square&logo=nodedotjs)
![Active Directory](https://img.shields.io/badge/Auth-Active%20Directory%20%2F%20LDAP-0078D4?style=flat-square&logo=windows)

Replaces hardcoded business approval paths, allowing administrators to visually configure conditional routing (e.g., jump based on pricing thresholds or department categories) with digital signatures and instant notification dispatches.

#### 📸 Screenshots & UI Showcase
<p align="center">
  <img src="assets/screenshots/approval-designer.png" width="90%" alt="Visual Drag-and-Drop Workflow Designer" />
</p>

#### 💼 Business Value & Real-World Impact
* **Eliminates Hardcoded Logic:** Allows business ops to dynamically build multi-tier approval chains without redeploying code.
* **Conditional Routing:** Evaluates submitter roles, transaction values, and department rules to route approvals dynamically.
* **Corporate Integration:** Connects directly with local Active Directory (LDAP) for unified enterprise Single Sign-On (SSO).
* **Multi-Channel Alerts:** Sends real-time approval requests and updates via Telegram Bot APIs and SMTP emails.

#### 🛠️ Architecture & Core Components
```mermaid
graph TD
    User[React Flow V11 Frontend] -->|Visual Graph Specs| API[Node.js Workflow Gateway]
    API -->|LDAP Protocol| AD[Active Directory]
    API -->|Condition Evaluator| Engine[Approval Decision Engine]
    Engine -->|Webhooks / API| Telegram[Telegram Bot Alerts]
    Engine -->|SMTP| Mail[Email Notifications]
```

---

### 2. 🗓️ Warehouse Queue Management System (WQMS)
> **Real-Time Loading Dock Booking & Gantt Board Carrier Scheduler**

![NestJS](https://img.shields.io/badge/Backend-NestJS-E0234E?style=flat-square&logo=nestjs)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square&logo=postgresql)
![Redis](https://img.shields.io/badge/Cache-Redis-DC382D?style=flat-square&logo=redis)
![Next.js](https://img.shields.io/badge/Frontend-Next.js-000000?style=flat-square&logo=nextdotjs)

A real-time, multi-tenant enterprise platform designed to optimize warehouse loading/unloading dock schedules, manage carrier queues, and eliminate truck congestion.

#### 📸 Screenshots & Operations Showcase
<p align="center">
  <img src="assets/screenshots/wqms-gantt-board.png" width="90%" alt="Real-time Loading Dock Gantt Scheduler" />
</p>

#### 💼 Business Value & Real-World Impact
* **Reduces Queue Bottlenecks:** Enables vendors and drivers to pre-book specific arrival time slots.
* **Automatic Collision Resolution:** Prevents double-booking of docks using a custom allocation algorithm backed by Redis cache locks.
* **Live Operations Visibility:** Provides warehouse guards and dock managers with a live Gantt board and real-time queue monitors.

#### 🛠️ Architecture & Tech Stack
```mermaid
graph TD
    Carrier[Carrier / Driver] -->|Pre-Booking Slot| Portal[Driver Portal Web App]
    Portal --> Gateway[NestJS API Gateway]
    Gateway --> QueueEngine[Queue & Dock Allocation Engine]
    QueueEngine --> RedisCache[(Redis Lock & Real-time Queue)]
    QueueEngine --> DB[(PostgreSQL Master DB)]
    QueueEngine -->|WebSockets| Display[Warehouse Gate Display & Guard Monitor]
```

---

### 3. 🗺️ Field Sales CRM (S-BIT)
> **Location-Verified Sales Routing & Client Order-Taking CRM**

![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react)
![Express.js](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![Leaflet](https://img.shields.io/badge/Mapping-Leaflet%20GPS-199900?style=flat-square&logo=leaflet)
![Dynamics NAV](https://img.shields.io/badge/ERP-MS%20Dynamics%20NAV-0078D4?style=flat-square)

An enterprise-grade Field Sales Customer Relationship Management platform designed for route planning, real-time GPS visit tracking, direct WhatsApp notifications, and deep ERP integration.

#### 📸 Screenshots & Field Visit Showcase
<p align="center">
  <img src="assets/screenshots/sbit-sales-map.png" width="90%" alt="Field Sales GPS Route & Visit Auditing" />
</p>

#### 💼 Business Value & Real-World Impact
* **Verifiable Field Visits:** Eliminates fake check-ins by auditing real-time GPS coordinates against geofenced client shop locations.
* **Direct ERP Synchronization:** Connects seamlessly with Microsoft Dynamics NAV (via SOAP/NTLM) to push sales orders, pull customer credit limits, and sync sales targets.
* **Automated WhatsApp Receipts:** Sends automated visit confirmations and order receipts to clients upon checkout via `whatsapp-web.js`.

#### 🛠️ Architecture & Dynamics NAV Sync Pipeline
```mermaid
graph TD
    MobileClient[Field Sales Web App] -->|GPS Check-in / Orders| Backend[Express Backend Gateway]
    Backend <-->|SOAP + NTLM Auth| ERP[Microsoft Dynamics NAV ERP]
    Backend -->|WhatsApp API| WA[Client WhatsApp Dispatcher]
    Backend -->|Geo Auditing| Leaflet[Leaflet GPS Geofencing Engine]
```

---

### 4. 📱 Super POS Mobile
> **Offline-First Mobile Point of Sale (POS) App for Sales Reps & Retail Outlets**

![React Native](https://img.shields.io/badge/Mobile-React%20Native%200.76-61DAFB?style=flat-square&logo=react)
![Expo](https://img.shields.io/badge/Framework-Expo%2052-000020?style=flat-square&logo=expo)
![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb)
![Midtrans](https://img.shields.io/badge/Payment-Midtrans-002D62?style=flat-square)

A high-performance, offline-first mobile Point of Sale application featuring direct local network thermal receipt printing and payment gateway integration.

#### 📸 Screenshots & Mobile UI Gallery

<p align="center">
  <img src="assets/screenshots/home.png" width="90%" alt="Super POS Mobile Main Dashboard" />
</p>

| Tablet Settlement View | Invoice Register List |
| :---: | :---: |
| <img src="assets/screenshots/settlement-android-tab.png" width="100%" alt="Settlement" /> | <img src="assets/screenshots/invoices-page.webp" width="100%" alt="Invoices" /> |

| Pending Invoice Bill | Product Library Catalog |
| :---: | :---: |
| <img src="assets/screenshots/pending-invoice.webp" width="100%" alt="Pending Bill" /> | <img src="assets/screenshots/library-page.png" width="100%" alt="Catalog" /> |

| Promotional Rules & Vouchers | Sales Performance Analytics |
| :---: | :---: |
| <img src="assets/screenshots/promo-page.webp" width="100%" alt="Promos" /> | <img src="assets/screenshots/sales-report.webp" width="100%" alt="Sales Analytics" /> |

| Purchase Orders (PO) Flow | Technical Stack Trace Reports |
| :---: | :---: |
| <img src="assets/screenshots/purchase-order-create.webp" width="100%" alt="PO Creation" /> | <img src="assets/screenshots/stack-trace.webp" width="100%" alt="Crash Tracing" /> |

#### 💼 Business Value & Real-World Impact
* **Offline-First Transactions:** Cashiers checkout customers completely offline; transactions queue locally in `AsyncStorage` and auto-reconcile with central MongoDB central servers once connection returns.
* **Direct Network Printing:** Generates raw ESC/POS command buffers and streams them via TCP Sockets directly to local network/WiFi thermal printers.
* **Cashless Payments:** Integrated Midtrans payment gateway for processing QRIS and local electronic payments.

#### 🛠️ Architecture & Offline Sync Pipeline
```mermaid
graph TD
    Client[Expo 52 Mobile Client] <-->|Sync Engine / REST| Server[Express API Server]
    Client -->|TCP Direct Socket| ThermalPrinter[WiFi / Network Thermal POS Printer]
    Server <-->|Mongoose ODM| DB[(MongoDB Database)]
    Server <-->|REST APIs| Midtrans[Midtrans Payment Gateway]
```

---

### 5. 📦 Inventory Audit System (Stock Opname)
> **Physical Stock Auditing & Recount Delegation Dashboard**

![React Router v7](https://img.shields.io/badge/Framework-React%20Router%20v7-CA4245?style=flat-square&logo=reactrouter)
![Tailwind CSS v4](https://img.shields.io/badge/Styling-Tailwind%20v4-06B6D4?style=flat-square&logo=tailwindcss)
![Express](https://img.shields.io/badge/Backend-Express.js-000000?style=flat-square&logo=express)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square&logo=postgresql)

A high-concurrency inventory reconciliation and stock audit platform built to automate physical count tracking, compute stock discrepancies, and sync physical warehouse assets with ERP ledgers.

#### 📸 Screenshots & Audit Dashboard
<p align="center">
  <img src="assets/screenshots/stock-opname-audit.png" width="90%" alt="Physical Stock Audit & Discrepancy Reconciliation" />
</p>

#### 💼 Business Value & Real-World Impact
* **Digital Scan Logging:** Operators audit warehouse inventory by scanning barcodes directly to specific shelves and racks in real-time.
* **Discrepancy Reconciliation Engine:** Automatically compares physical counts against system ERP ledgers ($\text{Physical Qty} = \sum\text{ScanLog.qty}$), categorizing items into `SESUAI` vs `SELISIH`.
* **Recount Delegation:** Audit managers can delegate specific discrepant items back to operators for blind recounts or perform direct override corrections (`finalCorrectionQty`).

#### 🛠️ Architecture & Workflow Engine
```mermaid
graph TD
    Scanner[Warehouse Barcode Operator] -->|Barcode Scan Logs| App[React Router v7 Frontend]
    App --> Gateway[Express API Server]
    Gateway <-->|Prisma ORM| DB[(PostgreSQL Database)]
    Gateway <-->|ioredis| Redis[(Redis Cache)]
    Gateway -->|LDAP Protocol| AD[Active Directory SSO]
```

---

### 6. 💰 Petty Cash Manager (Kas Kecil)
> **Multi-Warehouse Petty Cash Journal & Monthly Budgeting System**

![NestJS](https://img.shields.io/badge/Backend-NestJS%2010-E0234E?style=flat-square&logo=nestjs)
![Next.js](https://img.shields.io/badge/Frontend-Next.js%2015-000000?style=flat-square&logo=nextdotjs)
![Prisma](https://img.shields.io/badge/ORM-Prisma-2D3748?style=flat-square&logo=prisma)
![Cloudflare R2](https://img.shields.io/badge/Storage-Cloudflare%20R2-F38020?style=flat-square&logo=cloudflare)

A secure, multi-warehouse petty cash journal and monthly budgeting platform designed for enterprise branch expense auditing, receipt storage, and Active Directory verification.

#### 📸 Screenshots & Expense Audit UI
<p align="center">
  <img src="assets/screenshots/petty-cash-dashboard.png" width="90%" alt="Petty Cash Category Budgeting & Receipt Storage" />
</p>

#### 💼 Business Value & Real-World Impact
* **Branch Cash Isolation:** Scopes cash journals strictly to specific warehouses, ensuring cashiers only manage their designated branch accounts.
* **Budgeting Safeguards:** Limits monthly category expenses against admin-defined monthly caps (`Budget`), preventing unapproved overspending.
* **Digital Receipt Archival:** Direct uploads of expense attachments to Cloudflare R2 object storage during transaction logging, creating an immutable audit trail.

#### 🛠️ Architecture & Tech Stack
```mermaid
graph TD
    Client[Next.js 15 Client] <-->|REST APIs| Server[NestJS Gateway]
    Server <-->|Prisma ORM| DB[(PostgreSQL Database)]
    Server -->|AWS S3 SDK| R2[Cloudflare R2 Bucket Storage]
    Server -->|LDAP Protocol| AD[Active Directory SSO]
```

---

### 🤝 Let's Connect!

* 💼 **LinkedIn:** [linkedin.com/in/muhammad-yafizham-batubara](https://www.linkedin.com/in/muhammad-yafizham-batubara/)
* 📧 **Email:** [24434muhammad.yafizham@gmail.com](mailto:24434muhammad.yafizham@gmail.com)
* 💬 **WhatsApp:** [+62 838-5402-6650](https://wa.me/6283854026650)
* 📸 **Instagram:** [@yafizhambb](https://www.instagram.com/yafizhambb)
* 🏢 **Business:** [pethalvoid.com](https://pethalvoid.com)
