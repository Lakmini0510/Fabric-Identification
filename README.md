#  Fabric Monitoring & Decision Support Platform
**Automated Apparel Fabric Differentiation System (AIMS)**  
**Group:** J26-IT-377  
**Module Owner:** Member 4 (IT23362512 — Wasana Lakmini)  
**Deliverable:** Frontend Monitoring & Decision Support Platform (Frontend Only)
**UI/UX Inspiration:** [Google Stitch](https://stitch.withgoogle.com/) — AI-Native Design & Canvas Architecture

---

## 1. Overview & System Design

This platform has been recreated following the design principles of **Google Stitch** (`https://stitch.withgoogle.com/`), featuring:
- **Google Stitch AI Canvas Aesthetic:** Clean floating toolbars, frosted glass cards, subtle dot grid canvas, Google AI glow aura, and interactive prompt bar.
- **Dark & Light Mode:** Seamless toggle between Stitch dark canvas and crisp daylight porcelain mode with persistent theme preference in `localStorage`.
- **Modern Typography:** Geometric, high-legibility Google Fonts (`Outfit`, `Plus Jakarta Sans`, and `JetBrains Mono`).
- **Dedicated Home & Login Pages:**
  - **Home Page (`HomeView.tsx`):** Interactive prompt canvas bar, live KPI counters, flax linen scientific differentiation overview, and featured linen batch previews.
  - **Login Page (`LoginView.tsx`):** Google Stitch authentication modal with 1-click fast role switching for Viva evaluators (Wasana Lakmini QC Lead, Floor Inspector, Supervisor).
- **100% Pure Linen Fabric Focus:** All non-related fabrics and images removed. The entire catalog and AI classification pipeline exclusively inspects genuine linen fabric varieties and slub weaves.

---

## 2. Technology Stack

- **Framework:** React 18 + TypeScript
- **Bundler & Dev Server:** Vite 6
- **Typography:** `Outfit` (Primary), `Plus Jakarta Sans`, `JetBrains Mono`
- **Theme:** Dual-Mode (Stitch Dark / Light Canvas) via Tailwind `darkMode: 'class'`
- **Styling:** Vanilla CSS + Tailwind CSS
- **Icons:** Lucide React

---

## 3. Project Structure

```
├── src/
│   ├── components/
│   │   ├── auth/
│   │   │   └── LoginView.tsx               # Stitch QC portal login & 1-click viva evaluator access
│   │   ├── common/
│   │   │   └── BrandLogo.tsx               # FabricSense AI vector logo & system identity
│   │   ├── home/
│   │   │   └── HomeLandingPage.tsx         # Full landscape responsive landing page with Contact Us
│   │   ├── history/
│   │   │   └── HistoryView.tsx             # Linen history table, batch analytics & CSV export
│   │   ├── inspection/
│   │   │   └── FabricInspectionView.tsx    # Linen weave canvas, lighting simulation & sensors
│   │   ├── layout/
│   │   │   ├── Sidebar.tsx                 # Fixed non-scrollable collapsible sidebar with hamburger toggle
│   │   │   └── TopHeader.tsx               # Top bar with hamburger toggle, brand logo, and clock
│   │   ├── overview/
│   │   │   ├── CircularGauge.tsx           # Quality yield & classification gauges
│   │   │   ├── FabricTypeDistribution.tsx  # Linen material subtype donut chart
│   │   │   ├── OverviewView.tsx            # Operational quality dashboard
│   │   │   └── RecentInspectionsTable.tsx  # Recent linen inspection records table
│   ├── data/
│   │   └── fabricData.ts                   # 100% Pure linen fabric dataset records

│   ├── services/
│   │   └── dataService.ts                  # Query, filtering, and metric calculation engine
│   ├── styles/
│   │   └── index.css                       # Tailwind directives, industrial scrollbars, and grid background
│   ├── types/
│   │   └── inspection.ts                   # Strict TypeScript contracts for sensors & AI outputs
│   ├── App.tsx                             # Main workspace container & tab navigation
│   └── main.tsx                            # React DOM entry point
├── package.json
├── tailwind.config.js
├── tsconfig.json
└── vite.config.ts
```

---

## 5. How to Run the Project

### Prerequisites
- Node.js (v18+ or v24+)
- npm

### Installation & Development
```bash
# 1. Install dependencies
npm install

# 2. Start local Vite development server
npm run dev
```
Open `http://localhost:5173` in your browser.

### Production Build
```bash
# Build optimized production bundle
npm run build

# Preview production build locally
npm run preview
```

---

## 6. Verification & Test Checklist (60% Viva Readiness)

- [x] **Calculations from records:** Totals dynamically update from `src/data/fabricData.ts`.
- [x] **No Demo Banner:** Header displays clean industrial system status without demo alerts.
- [x] **Ambient Sensor Labeling:** DHT11 explicitly labeled as ambient chamber temp/hum.
- [x] **Multi-Sensor Telemetry:** TCS3200 (R, G, B, Clear), FDC1004 (pF capacitance), DHT11 displayed.
- [x] **Defect Bounding Box Overlays:** Visual toggle for anomaly bounding boxes with confidence scores.
- [x] **Lighting Modes:** Standard, Top Light, and Infrared simulated view modes.
- [x] **Search & Filters:** Search by Sample ID, Batch, Status, and Fabric Type.
- [x] **Export CSV:** Instant client-side download of inspection history records.
- [x] **Responsive Industrial UI:** Tested across desktop and mobile viewport breakpoints.
