# 📊 Balanced Scorecard Dashboard Excel Project — Strategic Performance Management

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Dashboard](https://img.shields.io/badge/Dashboard-Balanced_Scorecard-blue)
![Perspectives](https://img.shields.io/badge/Perspectives-4_Quadrant_BSC-orange)
![States](https://img.shields.io/badge/Coverage-4_U.S._States-purple)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

> A production-grade **Balanced Scorecard (BSC)** analytics project measuring strategic performance across **4 U.S. states** and **4 BSC perspectives** — Finance, Customer, Operations, and Resources — tracking $56.84M in annual sales, 42,262 calls, 3,158 customers, and 75+ staff headcount through a fully dynamic, state-filterable executive dashboard.
>
>
> ![image alt](https://github.com/ParthPatilAnalyst/Balanced-Scorecard-Dashboard-Excel-Project-Strategic-Performance-Management/blob/97ea6b9aa4d29f6dfe8cc70756932612ed047e65/Screenshot%202026-05-13%20100528.png)

---

## 📋 Table of Contents

- [Situation](#-situation)
- [Task](#-task)
- [Action](#-action)
- [Result](#-result)
- [Project Structure](#-project-structure)
- [BSC Framework Applied](#-bsc-framework-applied)
- [Key Metrics Snapshot](#-key-metrics-snapshot)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Author](#-author)

---

## ⚙️ Situation

A multi-state service organization operating across **4 U.S. states** (New York, Arizona, Texas, California) was managing performance measurement through disconnected reports — financial results were tracked separately from customer outcomes, operational efficiency, and workforce data. Leadership had no integrated view of how these four dimensions connected or reinforced each other.

The core problem: **decisions were being made with partial information**:

- Finance teams could see sales figures but had no link to customer satisfaction or operational cost drivers
- Operations managers tracked call volumes but had no visibility into revenue-per-call or how staffing levels impacted service quality
- HR had headcount and absenteeism data but no connection to sales outcomes or customer retention
- There was **no single framework** tying strategy to execution — making it impossible to identify which states were performing well across all dimensions, and which were hiding underperformance behind a single strong metric

The organization needed a structured, multi-perspective performance management system that could surface trade-offs, flag early warning signals, and give leadership a coherent strategic picture.

---

## 🎯 Task

As the **lead data analyst and dashboard architect**, the objective was to:

1. **Design and implement a full Balanced Scorecard** framework — structured around the 4 BSC perspectives: Financial, Customer, Operations (Internal Process), and Resources (Learning & Growth)
2. **Integrate 6 raw data streams** — Sales, Expenses, Customer counts, Call centre operations, Staff headcount, and Casual/absenteeism data — into a single unified model
3. **Build a dynamic Calculations engine** that powered Actual vs. Plan vs. Prior Year (PY) comparisons across all 4 states and 12 months simultaneously
4. **Deliver a state-filterable executive dashboard** that allowed leadership to drill into any state (AZ, NY, TX, CA, or Total) and see their complete strategic scorecard in one view
5. **Surface cross-perspective insights** — linking financial outcomes to customer behaviour, operational efficiency, and workforce capacity

---

## 🔧 Action

### Phase 1 — Data Architecture (7-Sheet Model)

Designed a purpose-built, **7-sheet workbook** with strict separation of data, logic, and presentation:

| Sheet | Role | Contents |
|---|---|---|
| `Lists` | Configuration | State list with filter link cells — drives dashboard interactivity |
| `Resources` | Raw Data | Staff headcount (PY / Actual / Plan), casual staff ratios, 4 states × 12 months |
| `Operations` | Raw Data | Calls volume, average handling time, revenue per call, cost per call — PY / Act / Plan |
| `Customer` | Raw Data | Customer counts, repeat customers, satisfaction %, 4 states × 12 months |
| `Finance` | Raw Data | Sales, expenses, P&L, no. of sales — PY / Act / Plan by state |
| `Calculations` | Logic Layer | All KPI derivations, chart data, state-level aggregations — feeds the dashboard |
| `Dashboard` | Presentation | Interactive executive BSC view — filtered by state via `Lists` link cell |

### Phase 2 — Financial Perspective
Tracked the complete financial picture across all 4 states:
- **Sales**: Actual vs. Plan vs. Prior Year — monthly and annualised
- **Expenses**: Actual vs. Plan with margin analysis
- **P&L**: State-level profitability with variance flags
- **Debtor Days**: Cash collection efficiency per state (e.g. NY at 81.6 days vs. plan of 62.8 — a critical flag)
- **Audit Risks**: Risk exposure count tracked per state

Key finding: Sales beat plan by **+6.8%** ($56.84M vs. $53.21M) but expenses also exceeded plan — requiring margin discipline analysis at state level.

### Phase 3 — Customer Perspective
Built a full customer health model covering:
- **Total Customers**: Actual (3,158) vs. Plan (3,042) vs. PY (2,946) — +7.2% YoY growth
- **Repeat Customers**: 812 actual vs. 770 plan — tracking loyalty and retention
- **Repeat Rate**: 25.7% — identifying which states drove the highest loyalty
- **Satisfaction %**: State-level scores ranging from **70.8% (NY) to 92.6% (CA)** — exposing a major satisfaction gap between states
- **Conversion Rate & Customer Profitability**: Linked customer volume to financial outcomes per state

### Phase 4 — Operations Perspective
Engineered the call centre efficiency layer:
- **42,262 total calls** handled across 4 states — tracked against a plan of 43,189
- **Average Handling Time**: 8.4 minutes actual vs. 7.0 minutes plan — identifying efficiency gaps by state
- **Revenue per Call**: $1,356.93 average — with state-level variance revealing NY at $1,697 vs. TX at $1,113
- **Cost per Call**: $9.15 average — enabling cost-efficiency scoring per state
- **Net Promoter Score**: Tracked per state to link operational quality to customer loyalty

### Phase 5 — Resources (Learning & Growth) Perspective
Tracked the workforce layer that underpins all other perspectives:
- **Staff Headcount**: Avg 30.2 actual vs. 31.5 plan across all states — identifying under/overstaffing by state
- **Casual Staff Ratio**: 17.8% average — tracking reliance on non-permanent workforce
- **Absenteeism Days**: Tracked monthly per state — NY significantly below PY (157.7 vs. 246.0 days)
- **Overtime Hours**: Monitored against plan (NY: 15,668 actual vs. 14,555 plan — flagging workforce pressure)
- **Excess Leave Days**: Tracked to identify capacity risk (NY: 2,304 actual vs. 1,850 plan)

### Phase 6 — Calculations Engine
Built a dedicated `Calculations` sheet that acts as the model's central nervous system:
- Aggregated all 4 BSC perspectives into state-level summary KPI tables (Finance / Customer / Operations / Resources)
- Generated monthly trend chart data for Sales, No. of Sales, and Customers — feeding 12-month sparklines and trend visuals
- Applied PY / Actual / Plan triple-comparison logic across every metric
- All dashboard elements reference `Calculations` exclusively — raw data sheets are read-only and never touched by the dashboard

### Phase 7 — Executive Dashboard
Built a single-pane **interactive BSC dashboard** driven by the state selector in `Lists`:
- Select any state (NY / AZ / TX / CA / Total) and all 4 quadrants refresh instantly
- Each quadrant displays its core KPIs with Actual, Plan, and PY columns + variance indicators
- Embedded trend charts for Sales, Customer counts, and No. of Sales — month-by-month for the selected state
- Color-coded variance indicators for at-a-glance strategic health assessment

---

## 📊 Result

### Performance Summary

| Perspective | Key Metric | Actual | Plan | vs Plan |
|---|---|---|---|---|
| **Finance** | Total Sales | $56.84M | $53.21M | **+6.8%** ✅ |
| **Finance** | Total Expenses | $51.12M | $47.89M | **+6.7%** ⚠️ |
| **Finance** | P&L | $5.72M | — | **10.1% margin** |
| **Customer** | Total Customers | 3,158 | 3,042 | **+3.8%** ✅ |
| **Customer** | Repeat Customers | 812 | 770 | **+5.5%** ✅ |
| **Customer** | Avg Satisfaction | 82.5% | — | Range: 70.8–92.6% |
| **Operations** | Total Calls | 42,262 | 43,189 | **-2.1%** |
| **Operations** | Revenue per Call | $1,356.93 | — | NY: $1,697 vs TX: $1,113 |
| **Operations** | Avg Handling Time | 8.4 mins | 7.0 mins | **+20% ⚠️** |
| **Resources** | Avg Staff | 30.2 | 31.5 | **-4.1%** |
| **Resources** | Casual Staff Ratio | 17.8% | — | Within acceptable range |

### State-Level P&L Breakdown

| State | Sales | Expenses | P&L |
|---|---|---|---|
| **NY** | $9.79M | $8.80M | $1.00M |
| **AZ** | $8.10M | $7.29M | $0.81M |
| **CA** | $5.59M | $5.03M | $0.56M |
| **TX** | $4.94M | $4.44M | $0.49M |

### Top Strategic Insights Delivered

| # | Insight | Perspective | Action Triggered |
|---|---------|-------------|-----------------|
| 1 | Sales exceeded plan by +6.8% but expenses rose proportionally — margin held at 10.1% | Finance | Expense discipline review initiated |
| 2 | NY debtor days at 81.6 vs. plan of 62.8 — a **30% cash collection lag** | Finance | Collections process review for NY |
| 3 | CA satisfaction at 92.6% vs. NY at 70.8% — **22-point gap** between best and worst state | Customer | NY customer experience improvement programme |
| 4 | Avg handling time +20% above plan — driving higher cost per call | Operations | Process efficiency review across all states |
| 5 | NY overtime 7.7% above plan while absenteeism dropped 36% vs. PY | Resources | Workforce capacity rebalancing for NY |
| 6 | Repeat customer rate at 25.7% — CA and AZ driving the highest loyalty | Customer | Loyalty programme replicated from CA/AZ to NY/TX |

---

## 📁 Project Structure

```
balanced-scorecard-dashboard/
│
├── BalancedScorecard_FINAL.xlsx       # Master workbook
│   ├── Lists                          # State selector — drives dashboard filter
│   ├── Resources                      # Staff headcount, casual ratio, absenteeism, OT
│   ├── Operations                     # Calls, AHT, revenue/cost per call, NPS
│   ├── Customer                       # Customers, repeat rate, satisfaction %
│   ├── Finance                        # Sales, expenses, P&L, debtor days, audit risk
│   ├── Calculations                   # Dynamic KPI engine — all aggregations & chart data
│   └── Dashboard                      # Executive BSC — 4-quadrant interactive view
│
└── README.md
```

---

## 🗂️ BSC Framework Applied

```
┌─────────────────────────────────────────────────────────┐
│                   VISION & STRATEGY                     │
└──────────────┬──────────────────────────────┬───────────┘
               │                              │
   ┌───────────▼───────────┐    ┌─────────────▼─────────────┐
   │   FINANCIAL           │    │   CUSTOMER                │
   │                       │    │                           │
   │ • Sales vs Plan/PY    │    │ • Customer count          │
   │ • Expenses & P&L      │    │ • Repeat customers        │
   │ • Debtor Days         │    │ • Satisfaction %          │
   │ • Audit Risk          │    │ • Conversion Rate         │
   └───────────┬───────────┘    └─────────────┬─────────────┘
               │                              │
   ┌───────────▼───────────┐    ┌─────────────▼─────────────┐
   │   OPERATIONS          │    │   RESOURCES               │
   │   (Internal Process)  │    │   (Learning & Growth)     │
   │                       │    │                           │
   │ • No. of Calls        │    │ • Staff headcount         │
   │ • Avg Handling Time   │    │ • Casual staff ratio      │
   │ • Revenue per Call    │    │ • Absenteeism days        │
   │ • Cost per Call       │    │ • Overtime hours          │
   │ • Net Promoter Score  │    │ • Excess leave days       │
   └───────────────────────┘    └───────────────────────────┘

  All 4 perspectives tracked: Actual vs Plan vs Prior Year
  Filterable by state: AZ | NY | TX | CA | Total
```

---

## 🔢 Key Metrics Snapshot

```
Financial Performance
──────────────────────────────────────────────────
  Total Sales (Actual)  : $56.84M  (+6.8% vs Plan)
  Total Expenses        : $51.12M  (+6.7% vs Plan)
  P&L                   : $5.72M   (10.1% margin)
  Best State (P&L)      : NY — $1.00M
  NY Debtor Days        : 81.6 days ⚠️  (Plan: 62.8)

Customer Health
──────────────────────────────────────────────────
  Total Customers       : 3,158   (+7.2% vs PY)
  Repeat Customers      : 812     (25.7% repeat rate)
  Best Satisfaction     : CA — 92.6%
  Lowest Satisfaction   : NY — 70.8%  ⚠️

Operations Efficiency
──────────────────────────────────────────────────
  Total Calls           : 42,262  (-2.1% vs Plan)
  Avg Handling Time     : 8.4 mins  (Plan: 7.0) ⚠️
  Revenue per Call      : $1,356.93
  Cost per Call         : $9.15
  Highest Rev/Call      : NY — $1,697.63

Workforce (Resources)
──────────────────────────────────────────────────
  Avg Staff (Actual)    : 30.2    (Plan: 31.5)
  Casual Staff Ratio    : 17.8%
  NY Overtime           : 15,668 hrs (Plan: 14,555) ⚠️
  NY Absenteeism        : 157.7 days (PY: 246.0) ✅
```

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| **Microsoft Excel** | Full BSC data model, calculation engine, interactive dashboard |
| **Structured Data Modelling** | 7-sheet architecture — raw data / logic / presentation separation |
| **Dynamic Formulas** | PY / Actual / Plan triple-comparison across 4 states × 12 months |
| **BSC Framework** | Kaplan & Norton 4-perspective balanced scorecard methodology |
| **Dashboard Design** | State-filtered KPI quadrants, trend charts, variance indicators |

---

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/balanced-scorecard-dashboard.git
cd balanced-scorecard-dashboard
```

### 2. Open the workbook
```
Open BalancedScorecard_FINAL.xlsx in Microsoft Excel (2016 or later)
```

### 3. Use the dashboard
```
1. Navigate to the Dashboard sheet
2. Use the state selector (linked to Lists sheet) to filter by:
   AZ (Arizona) | NY (New York) | TX (Texas) | CA (California) | Total
3. All 4 BSC quadrants refresh instantly for the selected state
4. Review Actual vs Plan vs PY across all perspectives
```

### 4. Update data
```
Edit raw data in: Resources / Operations / Customer / Finance sheets only
Calculations and Dashboard refresh automatically
Never edit the Calculations sheet formulas directly
```

---


## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

*If this project helped you, consider giving it a ⭐ on GitHub!*
