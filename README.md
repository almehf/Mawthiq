# SovereignDoc KSA 🇸🇦

 

SovereignDoc KSA is an enterprise-grade, sovereign document management and data privacy compliance application. Built intentionally to address strict data residency rules, national governance, and privacy frameworks, the platform enables organizations to securely handle documentation, review Personally Identifiable Information (PII) violations, inspect audit trails, and engage with a secured internal document assistant.

---

## 🚀 Key Features

*   **Sovereign Document Management:** Secure file processing, storage categorization, and organizational mapping decoupled from standard public clouds.
*   **PII Inspection & Review Engine:** Automate the detection and masking of sensitive local variables, ensuring compliance with Saudi Arabia's data security frameworks (PDPL/NDMO guidelines).
*   **Contextual AI Document Chat:** Interact directly with uploaded compliance corpora via an insulated, secure chat environment featuring inline source citations.
*   **Immutability Logs & Timeline:** Comprehensive chronological audit log visualization to monitor user activity, file modifications, and permission shifts.
*   **Dual Language Optimization:** Seamless English/Arabic UI toggling (`LanguageToggle`) designed for domestic operational compliance.
*   **Granular RBAC Security:** Role-based access constraints built over protected view layouts to guarantee data silo boundaries.

---


sovereign-doc-ksa/
├── base/                    # Data Entity Definitions & Local Governance Specs
│   ├── entities/            # Schemas for Documents, Users, AuditLogs, Collections & PII Rules
│   └── config.jsonc         # Engine Configuration Matrices
├── src/
│   ├── api/                 # Integrated API Layer (baseClient)
│   ├── components/
│   │   ├── audit/           # Audit Timeline visualizations
│   │   ├── chat/            # Chat Input, Messages, and Source Citations
│   │   ├── documents/       # File Upload, Document cards
│   │   ├── pii/             # PII Reports & Violation panels
│   │   └── ui/              # Decoupled design components built over Radix UI primitives
│   ├── hooks/               # Optimized runtime React state abstractions
│   ├── lib/                 # AuthContext engines, Query client config, utility parsers
│   └── pages/               # Functional views (Dashboard, PIIReview, Collections, Settings, etc.)


### Core Technologies Used:
*   **Framework:** React (Vite-bundler runtime)
*   **State Management & Data Fetching:** TanStack Query (`@tanstack/react-query`)
*   **Styling & UI:** Tailwind CSS + Shadcn UI components (Radix primitives)
*   **Icons & Components:** Lucide React icons, customized Google assets
*   **Linting & Quality:** ESLint Flat Config style

---

## 📦 Getting Started

### Prerequisites
Ensure you have **Node.js (v18+)** and **npm/pnpm** installed on your server environment.

### Installation

1. Clone the repository into your local or air-gapped server environment:
   
bash
   git clone [https://github.com/your-organization/sovereign-doc-ksa.git](https://github.com/your-organization/sovereign-doc-ksa.git)
   cd sovereign-doc-ksa





3. Install runtime dependencies:

cp .env.local .env

3. Setup your environment values. Create a local environment variables profile:

cp .env.local .env

Modify variables inside .env to attach to your corresponding base data streaming targets.


Development Server
Launch the hot-reloading development UI instance:
npm run dev

Production Compiling
Compile and optimize the build distribution for secure internal proxy hosting:

npm run build
# Preview build assets locally
npm run preview




🔒 Governance & Regulatory Alignment
SovereignDoc KSA includes automated validation maps mimicking strict administrative directives:
entities/PIIRule.jsonc: Predefined matching maps checking for Local Identification IDs, phone vectors, and confidential financial metrics.
entities/AuditLog.jsonc: Structuring tamper-evident access records tracking actions like FileUploaded, PIIMasked, or AuthFailure.







