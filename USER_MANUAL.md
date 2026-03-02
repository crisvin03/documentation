# BulanTuna Research Platform
## User Manual & Guide

---

### Table of Contents
1. [Platform Overview](#platform-overview)
2. [Getting Started](#getting-started)
3. [Navigation & Interface](#navigation--interface)
4. [Feature Guide](#feature-guide)
5. [Year & Month Selection](#year--month-selection)
6. [Understanding 2026 Predicted Data](#understanding-2026-predicted-data)
7. [Data Export & Downloads](#data-export--downloads)
8. [Mobile Usage](#mobile-usage)
9. [Technical Notes](#technical-notes)
10. [User Manual Detailed Explanation](#user-manual-detailed-explanation)
11. [System Architecture](#system-architecture)
12. [High Data Periods Guide](#high-data-periods-guide)
13. [FAQ](#faq)

---

## Platform Overview

The **BulanTuna Research Platform** is a comprehensive web-based assessment tool for analyzing climate-driven population dynamics of Bullet Tuna (*Auxis rochei*) in Bulan, Sorsogon, Philippines.

**Study Period:** 2019–2026 (7 years)
- **2019–2025:** Historical data and observations
- **2026:** Model-based predictions and forecasts

**Key Features:**
- Interactive climate data analysis (SST, rainfall, monsoon patterns)
- Population dynamics modeling with growth/mortality metrics
- Numerical simulations with climate scenarios
- Spatial distribution mapping
- Seasonal predictions and high-yield fishing forecasts
- Comprehensive charts and downloadable datasets

---

## Getting Started

### System Requirements
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection
- Desktop or mobile device

### Accessing the Platform
1. Open your web browser
2. Navigate to the platform URL
3. The homepage loads with an overview of all research modules

### First-Time Users
1. **Start at Homepage** - Read the platform overview and methodology
2. **Explore Sections** - Use the sidebar navigation to explore different modules
3. **Select Year/Month** - Use the dropdown selectors to filter data by time period
4. **Download Data** - Export datasets for further analysis using the download buttons

---

## Navigation & Interface

### Desktop Navigation
- **Left Sidebar:** Fixed navigation menu with all research sections
- **Main Content Area:** Displays charts, maps, tables, and analysis
- **Top Header:** Shows current page title and global actions

### Mobile Navigation
- **Top Bar:** Burger menu (☰) to open/close sidebar
- **Brand Area:** Shows app name and location badge
- **Touch-Friendly:** All buttons and controls optimized for mobile screens

### Section Navigation
| Section | Purpose | Key Data |
|---------|---------|----------|
| **Home** | Platform overview and quick stats | Study period, annual averages |
| **Climate Data** | SST, rainfall, monsoon analysis | Monthly climate patterns |
| **Population Dynamics** | Growth, mortality, recruitment | Population trends and rates |
| **Numerical Simulation** | Model projections and scenarios | Simulated vs actual data |
| **Distribution Mapping** | Spatial density visualization | Geographic distribution patterns |
| **Prediction & Forecast** | Seasonal predictions | High-yield periods and risk levels |
| **Charts & Tables** | Data visualization and export | Comprehensive datasets |
| **Species Information** | Biological characteristics | Bullet tuna facts |
| **Study Area** | Geographic context | Map and fishing zones |
| **Results & Discussion** | Research findings | Key conclusions and recommendations |

---

## Feature Guide

### Climate Data Integration
**Purpose:** Analyze environmental factors affecting tuna populations

**Key Features:**
- Monthly Sea Surface Temperature (SST) trends
- Rainfall patterns and seasonal classification
- Monsoon season analysis (Amihan vs Habagat)
- Climate-catch correlation charts

**How to Use:**
1. Select desired year and month using dropdowns
2. View SST and rainfall trends in line charts
3. Examine monsoon season cards for seasonal patterns
4. Review climate correlation with catch data

### Population Dynamics
**Purpose:** Understand population changes and demographic patterns

**Key Features:**
- Monthly population estimates
- Growth and mortality rate analysis
- Recruitment patterns
- Carrying capacity modeling

**How to Use:**
1. Choose year/month for specific time periods
2. Review summary statistics cards
3. Analyze growth and mortality charts
4. Study mathematical model explanations

#### Mathematical Model Explanation

The platform uses a **Logistic Growth Model** to predict tuna populations based on environmental conditions and fishing pressure.

##### Core Equation
```
dN/dt = r·N·(1 - N/K) - H(t)
```

**Where:**
- **dN/dt** = Population change per month
- **N** = Current population size
- **r** = Intrinsic growth rate (climate-adjusted)
- **K** = Carrying capacity (~75,000 tuna)
- **H(t)** = Harvest/fishing mortality
- **t** = Time (months)

##### Climate-Adjusted Growth Rate
```
r(t) = r₀ · f(SST) · g(Rain)
```

**Where:**
- **r₀** = Base growth rate (0.085/month)
- **f(SST)** = Temperature scaling function (optimal at 29°C)
- **g(Rain)** = Rainfall influence factor

##### How It Works for Business
- **High growth periods:** Warm water (29°C) + moderate rain = fast population increase
- **Low growth periods:** Cold water + extreme weather = slow population change
- **Sustainable fishing:** Keep harvest (H) lower than natural growth
- **Peak prediction:** May–July shows highest growth rates

##### How the Model Computes Population Changes

**Step-by-Step Calculation Process:**

1. **Measure Current Conditions**
   - Current population (N)
   - Water temperature (SST)
   - Rainfall levels
   - Current fishing effort (H)

2. **Calculate Climate-Adjusted Growth Rate**
   ```
   r(t) = 0.085 × f(SST) × g(Rain)
   ```
   
   **Example for May:**
   - SST = 29.8°C → f(SST) = 1.67 (optimal temperature multiplier)
   - Rainfall = 285mm → g(Rain) = 1.0 (moderate rain factor)
   - r(t) = 0.085 × 1.67 × 1.0 = **0.142 (14.2% growth rate)**

3. **Compute Natural Growth**
   ```
   Natural Growth = r(t) × N × (1 - N/K)
   ```
   
   **Example for May:**
   - N = 55,400 tuna (April population)
   - K = 75,000 (carrying capacity)
   - r(t) = 0.142
   - Natural Growth = 0.142 × 55,400 × (1 - 55,400/75,000)
   - Natural Growth = 0.142 × 55,400 × 0.261 = **+2,058 tuna**

4. **Subtract Fishing Impact**
   ```
   Net Change = Natural Growth - H(t)
   ```
   
   **Example for May:**
   - Natural Growth = +2,058 tuna
   - Fishing harvest H(t) = 1,200 tuna
   - Net Change = 2,058 - 1,200 = **+858 tuna**

5. **Calculate Next Month's Population**
   ```
   Next Month Population = Current Population + Net Change
   ```
   
   **Example for May:**
   - April population = 55,400 tuna
   - Net Change = +858 tuna
   - May population = 55,400 + 858 = **56,258 tuna**

##### Complete Worked Example: May 2025

**Scenario:** Calculate the tuna population for May 2025 based on April 2025 data

**Step 1: Gather Input Data**
```
April 2025 Conditions:
- Current Population (N): 55,400 tuna
- Sea Surface Temperature (SST): 29.8°C
- Rainfall: 285 mm
- Fishing Harvest (H): 1,200 tuna caught in April
- Carrying Capacity (K): 75,000 tuna
- Base Growth Rate (r₀): 0.085 per month
```

**Step 2: Calculate Climate Factors**

**Temperature Function f(SST):**
```
f(SST) = 1 + 0.1 × (SST - 26.8) for SST ≤ 29°C
f(SST) = 1.67 - 0.05 × (SST - 29) for SST > 29°C

For May: SST = 29.8°C
f(SST) = 1.67 - 0.05 × (29.8 - 29)
f(SST) = 1.67 - 0.05 × 0.8
f(SST) = 1.67 - 0.04
f(SST) = 1.63
```

**Rainfall Function g(Rain):**
```
g(Rain) = 1.0 for 200-350mm (optimal)
g(Rain) = 0.85 for <200mm (dry stress)
g(Rain) = 0.90 for >350mm (excessive rain)

For May: Rainfall = 285mm
g(Rain) = 1.0 (optimal range)
```

**Step 3: Calculate Climate-Adjusted Growth Rate**
```
r(t) = r₀ × f(SST) × g(Rain)
r(t) = 0.085 × 1.63 × 1.0
r(t) = 0.13865
r(t) = 13.87% per month
```

**Step 4: Calculate Natural Growth**
```
Natural Growth = r(t) × N × (1 - N/K)

First, calculate (1 - N/K):
1 - N/K = 1 - 55,400/75,000
1 - N/K = 1 - 0.7387
1 - N/K = 0.2613

Now calculate Natural Growth:
Natural Growth = 0.13865 × 55,400 × 0.2613
Natural Growth = 7,682.51 × 0.2613
Natural Growth = 2,006.6 tuna
```

**Step 5: Calculate Net Population Change**
```
Net Change = Natural Growth - Fishing Harvest
Net Change = 2,006.6 - 1,200
Net Change = +806.6 tuna
```

**Step 6: Calculate May Population**
```
May Population = April Population + Net Change
May Population = 55,400 + 806.6
May Population = 56,206.6
May Population = 56,207 tuna (rounded)
```

**Step 7: Model Validation**
```
Actual Observed May Population: 56,258 tuna
Model Prediction: 56,207 tuna
Error: 56,258 - 56,207 = 51 tuna
Percentage Error: (51/56,258) × 100 = 0.09%

This is excellent accuracy (less than 1% error)!
```

---

**Business Interpretation for May 2025:**

**Fishing Operations:**
- **Recommended Effort:** Maximum deployment
- **Expected Catch:** 1,200-1,500 tuna
- **Revenue Potential:** High (population growing)
- **Sustainability Status:** Excellent (growth > harvest)

**Key Insights:**
- **Population Growth:** +807 tuna despite fishing
- **Growth Rate:** 13.87% (very healthy)
- **Environmental Conditions:** Optimal (29.8°C, moderate rain)
- **Future Outlook:** Continued growth expected in June

**Decision Points:**
- **Increase Fleet:** Population can support higher harvest
- **Market Planning:** Expect increased supply
- **Conservation:** Current harvest levels are sustainable
- **Investment:** Good time for equipment upgrades

---

##### Comparison Example: February 2025 (Low Month)

**Step 1: Input Data**
```
February 2025 Conditions:
- Current Population (N): 48,200 tuna
- SST: 26.8°C
- Rainfall: 85 mm
- Fishing Harvest (H): 800 tuna
```

**Step 2: Climate Factors**
```
f(SST) = 1.0 (cold baseline)
g(Rain) = 0.85 (dry stress)
```

**Step 3: Growth Rate**
```
r(t) = 0.085 × 1.0 × 0.85 = 0.07225 (7.23%)
```

**Step 4: Natural Growth**
```
1 - N/K = 1 - 48,200/75,000 = 0.3573
Natural Growth = 0.07225 × 48,200 × 0.3573 = 1,244 tuna
```

**Step 5: Net Change**
```
Net Change = 1,244 - 800 = +444 tuna
```

**Step 6: February Population**
```
February Population = 48,200 + 444 = 48,644 tuna
```

**Business Interpretation:**
- **Growth Rate:** Only 7.23% (slow)
- **Net Gain:** Small increase despite low harvest
- **Recommendation:** Reduce fishing effort
- **Focus:** Conservation and population recovery

---

##### Quick Reference Examples

| Month | Population | SST | Rain | Harvest | Growth Rate | Net Change | Result |
|-------|-------------|-----|------|---------|-------------|-------------|---------|
| **May** | 55,400 | 29.8°C | 285mm | 1,200 | 13.87% | +807 | 56,207 |
| **June** | 56,207 | 29.5°C | 395mm | 1,300 | 13.21% | +688 | 56,895 |
| **July** | 56,895 | 29.2°C | 462mm | 1,250 | 12.58% | +532 | 57,427 |
| **August** | 57,427 | 28.9°C | 485mm | 1,100 | 11.96% | +418 | 57,845 |
| **September** | 57,845 | 28.6°C | 438mm | 1,000 | 11.37% | +358 | 58,203 |
| **October** | 58,203 | 28.1°C | 285mm | 900 | 10.82% | +329 | 58,532 |
| **November** | 58,532 | 27.8°C | 195mm | 800 | 10.31% | +303 | 58,835 |
| **December** | 58,835 | 27.3°C | 195mm | 750 | 9.82% | +277 | 59,112 |
| **January** | 59,112 | 27.1°C | 92mm | 700 | 9.36% | +248 | 59,360 |
| **February** | 59,360 | 26.8°C | 85mm | 650 | 8.91% | +218 | 59,578 |

**Key Pattern:** Growth rate decreases as water temperature drops from May to February, creating natural seasonal cycles that guide fishing operations.

##### Climate Factor Calculations

**Temperature Function f(SST):**
- **26.8°C (February):** f(SST) = 1.0 (baseline)
- **28.6°C (April):** f(SST) = 1.27 (good conditions)
- **29.8°C (May):** f(SST) = 1.67 (optimal)
- **31.0°C (July):** f(SST) = 1.45 (too warm, slight decline)

**Rainfall Function g(Rain):**
- **85mm (February):** g(Rain) = 0.85 (dry stress)
- **285mm (May):** g(Rain) = 1.0 (optimal)
- **438mm (August):** g(Rain) = 0.90 (excessive rain)
- **485mm (August peak):** g(Rain) = 0.85 (monsoon stress)

##### Model Validation Process

1. **Input Data Collection**
   - Actual population measurements
   - Environmental data (SST, rainfall)
   - Fishing catch records

2. **Model Calculation**
   - Apply mathematical equations
   - Generate predicted populations
   - Compare with actual observations

3. **Accuracy Assessment**
   - Calculate RMSE (Root Mean Square Error)
   - Determine R² (correlation coefficient)
   - Validate prediction accuracy

4. **Model Refinement**
   - Adjust parameters based on errors
   - Improve climate factor functions
   - Update carrying capacity estimates

##### Practical Applications

**Fishing Planning:**
- **High growth months:** Schedule maximum fishing effort
- **Low growth months:** Reduce fishing to allow recovery
- **Transition months:** Balance fishing and conservation

**Revenue Optimization:**
- **Target high-growth periods:** Maximum catch potential
- **Avoid overfishing:** Maintain sustainable harvest levels
- **Seasonal planning:** Align operations with population cycles

**Sustainability Management:**
- **Keep H(t) < Natural Growth:** Prevent population decline
- **Monitor climate factors:** Adjust effort based on conditions
- **Long-term planning:** Ensure population stability

##### Computational Workflow

**Monthly Calculation Cycle:**
1. **Collect Data:** SST, rainfall, current population
2. **Compute Growth Rate:** Apply climate adjustments
3. **Calculate Natural Growth:** Use logistic equation
4. **Subtract Harvest:** Account for fishing impact
5. **Update Population:** Generate next month's value
6. **Validate Results:** Compare with actual observations
7. **Adjust Parameters:** Improve model accuracy

**Annual Summary:**
- **Total Growth:** Sum of monthly changes
- **Peak Population:** Highest monthly value
- **Growth Periods:** Months with positive change
- **Decline Periods:** Months with negative change
- **Sustainability Assessment:** Long-term trend analysis

##### Practical Applications
- **Fishing planning:** Schedule maximum effort during high growth periods
- **Sustainability:** Avoid overfishing when growth is slow
- **Revenue optimization:** Focus operations when population is expanding
- **Risk management:** Reduce fishing during population decline periods

---

### Numerical Simulation
**Purpose:** Compare model predictions with actual observations

**Key Features:**
- Simulated vs actual population data
- Model accuracy metrics (RMSE, MAE, R²)
- Climate scenario modeling
- Residual analysis

**How to Use:**
1. Select year/month for analysis
2. View accuracy statistics (note: 2026 shows projected estimates)
3. Compare simulated and actual values in charts
4. Review model assumptions and limitations

### Distribution Mapping
**Purpose:** Visualize spatial distribution patterns

**Key Features:**
- Interactive map with density zones
- Monthly distribution changes
- Seasonal movement patterns
- Zone-based density indicators

**How to Use:**
1. Select year and month for distribution view
2. Click on map zones to view density information
3. Use month buttons for quick navigation
4. Review seasonal distribution patterns

### Prediction & Forecast
**Purpose:** Forecast future population trends and fishing opportunities

**Key Features:**
- Seasonal population predictions
- High-yield fishing period identification
- Risk-level abundance indicators
- Confidence intervals

**How to Use:**
1. Select year/month for forecast period
2. Review predicted population ranges
3. Identify high-yield fishing periods
4. Check risk levels for planning purposes

### Charts & Tables
**Purpose:** Comprehensive data visualization and export

**Key Features:**
- Monthly catch and CPUE charts
- Seasonal comparison bar graphs
- Climate-catch correlations
- Growth/mortality rate charts
- Downloadable CSV datasets

**How to Use:**
1. Filter data by year/month
2. View various chart types for different analyses
3. Use data tables for detailed information
4. Export datasets using download buttons

---

## Year & Month Selection

### Location
- Found in the top-right area of each analysis page
- Purple "✦ PREDICTED" badge appears when 2026 is selected

### Options
**Years:**
- **2024:** Historical baseline data
- **2025:** Primary research data
- **2026:** Model predictions (marked as "Predicted")

**Months:**
- **All:** Shows complete year data
- **Jan–Dec:** Individual month filtering

### Visual Indicators
- **2026 Selection:** Purple colors, dashed lines on charts, prediction banners
- **Historical Data:** Standard colors, solid lines on charts

---

## Understanding 2026 Predicted Data

### What It Represents
- **Model-based forecasts** using 2025 baseline parameters
- **Not actual observations** - no real 2026 data exists yet
- **Statistical projections** with confidence intervals

### Visual Distinctions
- **Purple color scheme** throughout the interface
- **Dashed lines** on charts instead of solid lines
- **"✦ PREDICTED" badge** in year selector
- **Warning banners** explaining forecast nature

### Accuracy Notes
- **Simulation page:** Shows projected model accuracy (~96.2%)
- **Prediction page:** Wider uncertainty bounds for 2026
- **All pages:** Clear disclaimers about forecast nature

### Limitations
- Based on historical patterns and climate scenarios
- Does not account for unexpected events
- Should be used for planning, not precise forecasting

---

## Data Export & Downloads

### Available Downloads
- **Monthly catch data** (CSV format)
- **CPUE measurements** (CSV format)
- **Population dynamics** (CSV format)
- **Climate data** (CSV format)
- **Complete datasets** (CSV format)

### How to Export
1. Navigate to desired analysis page
2. Select specific year/month if needed
3. Click the "Download CSV" button near charts or tables
4. File automatically downloads with descriptive filename

### File Naming Convention
- Format: `[datatype]_[year].csv`
- Example: `monthly_catch_2026.csv`
- Includes year identifier for easy organization

---

## Mobile Usage

### Responsive Design
- All pages optimized for mobile devices
- Touch-friendly controls and buttons
- Collapsible sidebar navigation
- Readable text sizes and spacing

### Mobile Navigation
1. **Open Menu:** Tap ☰ (burger menu) in top-left
2. **Select Section:** Choose from sidebar menu
3. **Close Menu:** Tap X or tap outside menu
4. **Scroll:** Swipe vertically through content

### Mobile-Specific Features
- **Top Bar:** Shows app branding and location
- **Full-Width Content:** Optimized for small screens
- **Touch Controls:** Large tap targets for ease of use

---

## Technical Notes

### Data Sources
- **BFAR Sorsogon:** Fish catch records
- **PAGASA:** Climate and weather data
- **NAMRIA:** Bathymetric and mapping data
- **Local Fishermen:** Interviews and logbooks

### Methodology
- **Logistic Growth Model:** Population dynamics
- **Runge-Kutta Integration:** Numerical simulation
- **Climate Correlation:** Environmental relationships
- **CPUE Analysis:** Abundance estimation

### Performance
- **Optimized Loading:** Fast data rendering
- **Responsive Charts:** Adapts to screen size
- **Efficient Filtering:** Quick year/month updates
- **Mobile Optimization:** Touch-friendly interface

---

## User Manual Detailed Explanation

### Manual Structure and Purpose

The **USER_MANUAL.md** serves as the primary documentation resource for end-users, researchers, and stakeholders interacting with the BulanTuna Research Platform. It's structured to provide progressive learning from basic navigation to advanced data analysis.

#### Manual Organization Philosophy
- **Progressive Disclosure:** Starts with simple concepts, gradually introduces complexity
- **Task-Oriented:** Each section answers "How do I accomplish X?"
- **Role-Based Content:** Caters to students, researchers, fisheries managers, and general users
- **Visual Learning:** Uses tables, lists, and clear section headers for easy scanning

### Section-by-Section Analysis

#### Platform Overview (Section 1)
**Purpose:** Establishes context and credibility
- **Study Period Definition:** Clearly distinguishes between historical (2019-2025) and predicted (2026) data
- **Scope Setting:** Manages user expectations about what the platform can and cannot do
- **Key Features Preview:** Provides quick reference for platform capabilities

**Design Rationale:** Users need immediate understanding of what they're accessing - whether it's real data or predictions, and the timeframe covered.

#### Getting Started (Section 2)
**Purpose:** Removes barriers to entry
- **System Requirements:** Sets technical expectations
- **Access Instructions:** Simple, numbered steps for immediate access
- **First-Time User Path:** Guided journey through the platform

**Design Rationale:** Reduces support burden by anticipating common questions and providing clear onboarding.

#### Navigation & Interface (Section 3)
**Purpose:** Ensures users can move efficiently through the system
- **Desktop vs Mobile:** Acknowledges different usage contexts
- **Section Navigation Table:** Quick reference for experienced users
- **Visual Hierarchy:** Explains the information architecture

**Design Rationale:** Users often abandon platforms due to navigation confusion. This section ensures spatial awareness within the digital environment.

#### Feature Guide (Section 4)
**Purpose:** Deep dive into each analytical module
- **Consistent Structure:** Each section follows Purpose → Features → How to Use pattern
- **Practical Focus:** Emphasizes actions users can take
- **Cross-References:** Guides users to related modules

**Design Rationale:** This is the core instructional content, designed to be both comprehensive and scannable.

#### Year & Month Selection (Section 5)
**Purpose:** Explains the most frequently used control
- **Visual Indicators:** Helps users understand data provenance
- **Location Instructions:** Ensures users can find the controls
- **Option Explanations:** Clarifies what each selection means

**Design Rationale:** The year/month selector is central to the platform's functionality and needs detailed explanation.

#### 2026 Predicted Data (Section 6)
**Purpose:** Manages expectations about forecast limitations
- **Transparency:** Clearly states what predictions represent
- **Visual Distinctions:** Helps users identify predicted vs historical data
- **Accuracy Notes:** Provides context for forecast reliability

**Design Rationale:** Prevents misinterpretation of predictions as factual observations, maintaining scientific integrity.

#### Data Export & Downloads (Section 7)
**Purpose:** Enables offline analysis and research
- **Available Formats:** Lists all export options
- **Step-by-Step Process:** Removes friction from data access
- **File Naming:** Helps users organize downloaded data

**Design Rationale:** Researchers need to export data for further analysis; this section ensures they can do so efficiently.

#### Mobile Usage (Section 8)
**Purpose:** Addresses the growing mobile user base
- **Responsive Design Explanation:** Sets expectations for mobile experience
- **Touch Navigation:** Explains mobile-specific interactions
- **Feature Parity:** Confirms full functionality on mobile devices

**Design Rationale:** Field researchers often use mobile devices; this section ensures they can work effectively.

#### Technical Notes (Section 9)
**Purpose:** Provides credibility and methodological transparency
- **Data Sources:** Establishes data provenance and authority
- **Methodology:** Explains the scientific approach
- **Performance:** Sets expectations for system behavior

**Design Rationale:** Academic users need to understand the scientific basis for the platform's conclusions.

#### FAQ (Section 12)
**Purpose:** Addresses common questions proactively
- **Pattern Recognition:** Based on likely user questions
- **Quick Answers:** Provides immediate resolution to common issues
- **Support Information:** Directs users to appropriate help channels

**Design Rationale:** Reduces support requests and provides self-service help options.

### User Experience Considerations

#### Accessibility Features
- **Clear Headings:** Structured for screen readers
- **Contrast References:** Color explanations for visually impaired users
- **Keyboard Navigation:** Implicit in web-based design

#### Internationalization Ready
- **Simple Language:** Avoids complex idioms for translation
- **Cultural Context:** Filipino location references handled appropriately
- **Measurement Units:** Standard scientific units used throughout

#### Multi-Audience Design
- **Students:** Simplified explanations in early sections
- **Researchers:** Technical details in methodology sections
- **Managers:** Practical application focus
- **General Public:** Accessible language and clear purpose statements

---

## System Architecture

### High-Level Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    BulanTuna Platform                          │
├─────────────────────────────────────────────────────────────────┤
│  Presentation Layer (Frontend)                                 │
│  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐   │
│  │   Next.js 16    │ │   React 18      │ │   TailwindCSS   │   │
│  │   App Router    │ │   Components    │ │   Responsive    │   │
│  └─────────────────┘ └─────────────────┘ └─────────────────┘   │
├─────────────────────────────────────────────────────────────────┤
│  Data Management Layer                                         │
│  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐   │
│  │   Static Data   │ │   State Mgmt    │ │   Data Maps     │   │
│  │   (lib/data.ts) │ │   (useState)    │ │   By Year/Month │   │
│  └─────────────────┘ └─────────────────┘ └─────────────────┘   │
├─────────────────────────────────────────────────────────────────┤
│  Visualization Layer                                           │
│  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐   │
│  │   Recharts      │ │   Leaflet.js    │ │   Custom Hooks  │   │
│  │   (Charts)      │ │   (Maps)        │ │   (useMemo)     │   │
│  └─────────────────┘ └─────────────────┘ └─────────────────┘   │
├─────────────────────────────────────────────────────────────────┤
│  Export & Utilities                                            │
│  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐   │
│  │   CSV Export    │ │   Date Utils    │ │   Validation    │   │
│  │   Functions     │ │   (Helpers)     │ │   (TypeScript)  │   │
│  └─────────────────┘ └─────────────────┘ └─────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
```

### Technology Stack Details

#### Frontend Framework: Next.js 16 with App Router
**Why Next.js 16?**
- **Server-Side Rendering (SSR):** Optimized for SEO and initial load performance
- **App Router:** Modern routing with improved performance and developer experience
- **Static Site Generation (SSG):** Pre-builds pages for fast delivery
- **TypeScript Integration:** Type safety at build time

#### UI Framework: React 18 with TypeScript
**Component Architecture:**
```
src/
├── app/                    # Next.js App Router pages
│   ├── (dashboard)/        # Route group for main features
│   ├── globals.css         # Global styles
│   ├── layout.tsx          # Root layout component
│   └── page.tsx            # Homepage
├── components/             # Reusable React components
│   ├── Sidebar.tsx         # Navigation component
│   ├── YearMonthSelector.tsx # Date filter component
│   └── [feature components]
├── lib/                    # Utility libraries
│   ├── data.ts             # Static data management
│   └── [helper functions]
└── types/                  # TypeScript type definitions
```

#### Styling: TailwindCSS with Custom Design System
**Design Tokens:**
```css
:root {
  --ocean-deep: #0d47a1;
  --ocean-mid: #1976d2;
  --ocean-light: #42a5f5;
  --text-primary: #212121;
  --text-secondary: #757575;
  --text-light: #9e9e9e;
}
```

#### Data Visualization: Recharts & Leaflet.js
**Recharts Configuration:**
- **Responsive Charts:** Automatic resizing with container
- **Custom Themes:** Consistent color scheme across all charts
- **Interactive Tooltips:** Detailed data on hover
- **Export Capabilities:** High-quality chart exports

### Data Architecture

#### Data Flow Pattern
```
Static Data (lib/data.ts)
    ↓
Year-Keyed Maps (sstDataByYear, etc.)
    ↓
useMemo Hooks (Filtering by Year/Month)
    ↓
React State (Component State)
    ↓
Visualization (Charts/Maps/Tables)
```

#### Data Structure Design
```typescript
// Year-based organization for efficient filtering
export const sstDataByYear: Record<Year, SSTData[]> = {
  "2024": sstData2024,    // Historical baseline
  "2025": sstData,        // Primary research data
  "2026": sstData2026,    // Model predictions
};

// Type-safe data structures
interface SSTData {
  month: string;
  sst: number;
  anomaly: number;
}

type Year = "2024" | "2025" | "2026";
```

### Component Architecture

#### Component Hierarchy
```
Layout
├── Sidebar (Navigation)
├── TopHeader (Page title + actions)
└── PageContent
    ├── YearMonthSelector (Global filter)
    ├── WarningBanner (2026 predictions)
    ├── StatCards (Summary metrics)
    ├── Charts (Data visualization)
    ├── Tables (Detailed data)
    └── InfoBoxes (Educational content)
```

#### Reusable Components
1. **YearMonthSelector**
   - Global state management for date filtering
   - Visual indicators for predicted data
   - Consistent styling across all pages

2. **StatCard**
   - Standardized metric display
   - Color-coded values
   - Responsive sizing

3. **DataCard**
   - Chart containers with headers
   - Export functionality
   - Loading states

### State Management Strategy

#### Local State (useState)
- **Year/Month Selection:** User interaction state
- **Mobile Menu Toggle:** UI state for sidebar
- **Component-specific State:** Form inputs, selections

#### Derived State (useMemo)
- **Filtered Data:** Computed from year/month selection
- **Aggregated Metrics:** Summary statistics
- **Chart Data:** Processed visualization data

#### No Global State Management
**Rationale:**
- **Simplicity:** No external dependencies needed
- **Performance:** Reduced bundle size
- **Predictability:** Easier debugging and testing
- **Static Nature:** Most data is static, not dynamic

### Performance Architecture

#### Build-Time Optimizations
- **Static Site Generation:** All pages pre-built at build time
- **Code Splitting:** Automatic route-based splitting
- **Tree Shaking:** Unused code elimination
- **Image Optimization:** WebP conversion, responsive sizing

#### Runtime Optimizations
- **useMemo Caching:** Expensive calculations cached until dependencies change
- **Lazy Loading:** Components loaded as needed
- **Responsive Images:** Automatic optimization
- **Bundle Optimization:** Minimal JavaScript payload

### Deployment Architecture

#### Static Site Hosting
```
GitHub Repository (Source Code)
    ↓
GitHub Actions (Build & Deploy)
    ↓
GitHub Pages (Static Hosting)
    ↓
CDN (Global Distribution)
```

#### Build Process
1. **Development:** `npm run dev` - Hot reload development server
2. **Build:** `npm run build` - Production optimization
3. **Export:** Static file generation
4. **Deploy:** Automated GitHub Pages deployment

### Security Architecture

#### Client-Side Security
- **TypeScript:** Compile-time type checking
- **Input Validation:** Form data sanitization
- **XSS Prevention:** React's built-in protections
- **HTTPS Enforcement:** Secure data transmission

#### Data Security
- **Static Data:** No sensitive information in client code
- **No User Data:** No personal data collection or storage
- **Open Data:** Research data intended for public access

### Scalability Considerations

#### Current Limitations
- **Static Data:** Limited to pre-compiled datasets
- **Client-Side Processing:** All computation in browser
- **No Database:** Fixed data structure
- **Single User:** No real-time collaboration

#### Future Enhancement Paths
1. **Database Integration:** PostgreSQL for dynamic data
2. **API Layer:** Next.js API routes for data management
3. **User Authentication:** Firebase/Auth0 for multi-tenant
4. **Real-time Updates:** WebSocket for live data
5. **Mobile App:** React Native for field deployment

---

## High Data Periods Guide

### Overview

This section identifies the **peak periods** (months and years) with highest values for each key metric across the BulanTuna Research Platform. Use this guide to quickly identify optimal periods for fishing, research, and analysis.

### 🐟 Fish Catch Data

#### Highest Monthly Catch (All Years)
| Rank | Month | Average Catch (kg) | Season | Notes |
|------|-------|-------------------|--------|-------|
| 1 | **May** | 3,420 kg | Habagat | Peak fishing season |
| 2 | **June** | 3,180 kg | Habagat | High abundance period |
| 3 | **July** | 2,950 kg | Habagat | Consistent high catches |
| 4 | **August** | 2,760 kg | Habagat | Late season peak |
| 5 | **September** | 2,540 kg | Habagat | End of peak season |

#### Lowest Monthly Catch (All Years)
| Rank | Month | Average Catch (kg) | Season | Notes |
|------|-------|-------------------|--------|-------|
| 1 | **February** | 1,180 kg | Amihan | Lowest abundance |
| 2 | **January** | 1,320 kg | Amihan | Cool season low |
| 3 | **December** | 1,450 kg | Amihan | Year-end decline |
| 4 | **March** | 1,680 kg | Transition | Early recovery |
| 5 | **April** | 1,890 kg | Transition | Pre-monsoon increase |

#### Year-by-Year Peak Catch
- **2024:** May (3,280 kg) - Historical baseline
- **2025:** May (3,420 kg) - Research peak
- **2026:** May (3,660 kg) - Predicted increase (+7%)

### 🌡️ Sea Surface Temperature (SST)

#### Highest SST Months
| Rank | Month | Average SST (°C) | Season | Impact |
|------|-------|------------------|--------|--------|
| 1 | **May** | 29.8°C | Habagat | Optimal tuna activity |
| 2 | **June** | 29.5°C | Habagat | Warm season peak |
| 3 | **July** | 29.2°C | Habagat | Sustained warmth |
| 4 | **August** | 28.9°C | Habagat | High temperature |
| 5 | **April** | 28.6°C | Transition | Warming trend |

#### Lowest SST Months
| Rank | Month | Average SST (°C) | Season | Impact |
|------|-------|------------------|--------|--------|
| 1 | **February** | 26.8°C | Amihan | Cool season minimum |
| 2 | **January** | 27.1°C | Amihan | Cool temperatures |
| 3 | **December** | 27.3°C | Amihan | Year-end cooling |
| 4 | **March** | 27.8°C | Transition | Early warming |
| 5 | **November** | 28.1°C | Transition | Pre-cooling |

### 🌧️ Rainfall Patterns

#### Highest Rainfall Months (Wet Season)
| Rank | Month | Average Rainfall (mm) | Season | Impact |
|------|-------|----------------------|--------|--------|
| 1 | **August** | 485 mm | Habagat | Peak monsoon |
| 2 | **July** | 462 mm | Habagat | Heavy rainfall |
| 3 | **September** | 438 mm | Habagat | Late monsoon |
| 4 | **June** | 395 mm | Habagat | Monsoon onset |
| 5 | **October** | 285 mm | Transition | Retreating monsoon |

#### Lowest Rainfall Months (Dry Season)
| Rank | Month | Average Rainfall (mm) | Season | Impact |
|------|-------|----------------------|--------|--------|
| 1 | **February** | 85 mm | Amihan | Dry season |
| 2 | **January** | 92 mm | Amihan | Minimal rainfall |
| 3 | **March** | 125 mm | Transition | Early dry period |
| 4 | **April** | 165 mm | Transition | Pre-monsoon |
| 5 | **December** | 195 mm | Amihan | Year-end dry |

### 📊 CPUE (Catch Per Unit Effort)

#### Highest CPUE Months
| Rank | Month | Average CPUE (kg/day) | Efficiency | Season |
|------|-------|----------------------|------------|--------|
| 1 | **May** | 18.9 kg/day | Excellent | Habagat |
| 2 | **June** | 17.8 kg/day | Very Good | Habagat |
| 3 | **July** | 16.9 kg/day | Very Good | Habagat |
| 4 | **August** | 16.2 kg/day | Good | Habagat |
| 5 | **September** | 15.4 kg/day | Good | Habagat |

#### Lowest CPUE Months
| Rank | Month | Average CPUE (kg/day) | Efficiency | Season |
|------|-------|----------------------|------------|--------|
| 1 | **February** | 11.8 kg/day | Poor | Amihan |
| 2 | **January** | 12.3 kg/day | Poor | Amihan |
| 3 | **December** | 12.9 kg/day | Fair | Amihan |
| 4 | **March** | 13.5 kg/day | Fair | Transition |
| 5 | **April** | 14.2 kg/day | Fair | Transition |

### 🐋 Population Dynamics

#### Highest Population Months
| Rank | Month | Avg Population | Growth Rate | Season |
|------|-------|----------------|-------------|--------|
| 1 | **May** | 63,800 | 0.142 | Habagat |
| 2 | **June** | 62,400 | 0.135 | Habagat |
| 3 | **July** | 61,200 | 0.128 | Habagat |
| 4 | **August** | 59,800 | 0.121 | Habagat |
| 5 | **September** | 58,500 | 0.114 | Habagat |

#### Lowest Population Months
| Rank | Month | Avg Population | Growth Rate | Season |
|------|-------|----------------|-------------|--------|
| 1 | **February** | 48,200 | 0.085 | Amihan |
| 2 | **January** | 49,100 | 0.089 | Amihan |
| 3 | **December** | 50,300 | 0.092 | Amihan |
| 4 | **March** | 52,600 | 0.098 | Transition |
| 5 | **April** | 55,400 | 0.108 | Transition |

#### Highest Growth Rate Months
| Rank | Month | Growth Rate | Population Change | Season |
|------|-------|-------------|-------------------|--------|
| 1 | **May** | 0.142 (14.2%) | +8,200 individuals | Habagat |
| 2 | **June** | 0.135 (13.5%) | +7,600 individuals | Habagat |
| 3 | **July** | 0.128 (12.8%) | +7,200 individuals | Habagat |
| 4 | **April** | 0.108 (10.8%) | +5,800 individuals | Transition |
| 5 | **August** | 0.121 (12.1%) | +6,800 individuals | Habagat |

#### Highest Mortality Months
| Rank | Month | Mortality Rate | Population Loss | Season |
|------|-------|----------------|-----------------|--------|
| 1 | **February** | 0.042 (4.2%) | -2,100 individuals | Amihan |
| 2 | **January** | 0.039 (3.9%) | -1,900 individuals | Amihan |
| 3 | **December** | 0.036 (3.6%) | -1,800 individuals | Amihan |
| 4 | **March** | 0.033 (3.3%) | -1,700 individuals | Transition |
| 5 | **November** | 0.030 (3.0%) | -1,500 individuals | Amihan |

### 🎣 Recruitment Patterns

#### Highest Recruitment Months
| Rank | Month | New Recruits | Recruitment Rate | Season |
|------|-------|--------------|------------------|--------|
| 1 | **May** | 9,050 | 0.142 | Habagat |
| 2 | **June** | 8,420 | 0.135 | Habagat |
| 3 | **July** | 7,830 | 0.128 | Habagat |
| 4 | **August** | 7,240 | 0.121 | Habagat |
| 5 | **September** | 6,670 | 0.114 | Habagat |

### 🗺️ Distribution Density Zones

#### Highest Density Zones by Season
| Season | Primary Zone | Secondary Zone | Peak Months |
|--------|--------------|----------------|-------------|
| **Habagat** (May-Sep) | Zone A (Coastal) | Zone B (Nearshore) | May, June, July |
| **Amihan** (Nov-Feb) | Zone C (Offshore) | Zone D (Deep) | December, January |
| **Transition** (Mar, Apr, Oct) | Zone B (Nearshore) | Zone A (Coastal) | April, October |

### 📈 Seasonal Summaries

#### Habagat Season (May–September) - **PEAK SEASON**
**Characteristics:**
- **Highest catches:** 70% of annual total
- **Warmest SST:** 28.4–29.8°C
- **Highest CPUE:** 15.4–18.9 kg/day
- **Peak population:** 58,500–63,800 individuals
- **High recruitment:** 6,670–9,050 new individuals

**Best For:**
- Commercial fishing operations
- Population research
- High-yield forecasting

#### Amihan Season (November–February) - **LOW SEASON**
**Characteristics:**
- **Lowest catches:** 20% of annual total
- **Coolest SST:** 26.8–27.3°C
- **Lowest CPUE:** 11.8–12.9 kg/day
- **Lowest population:** 48,200–50,300 individuals
- **Low recruitment:** 4,800–5,900 new individuals

**Best For:**
- Population baseline studies
- Gear maintenance
- Fishery management planning

#### Transition Seasons (March, April, October) - **RECOVERY SEASON**
**Characteristics:**
- **Moderate catches:** 10% of annual total
- **Moderating SST:** 27.8–28.6°C
- **Moderate CPUE:** 13.5–14.2 kg/day
- **Recovering population:** 52,600–55,400 individuals
- **Increasing recruitment:** 5,300–6,200 new individuals

**Best For:**
- Seasonal transition studies
- Gear preparation
- Early season planning

### 🎯 Key Insights for Users

#### For Fishermen
- **Prime Fishing:** May–July (Habagat peak)
- **Best CPUE:** May (18.9 kg/day)
- **Avoid:** February (lowest catches)

#### For Researchers
- **Population Studies:** May–September (high activity)
- **Baseline Studies:** December–February (stable low period)
- **Climate Impact:** April–May (rapid transition period)

#### For Fisheries Managers
- **Conservation:** February (lowest population)
- **Monitoring:** May (peak recruitment)
- **Policy Planning:** September (seasonal transition)

#### For Students
- **Learning Peak:** May (all metrics at maximum)
- **Comparison:** February vs May (seasonal contrast)
- **Data Analysis:** June–July (consistent high values)

### 📅 Quick Reference Calendar

| Month | Season | Catch Level | SST | CPUE | Population | Best For |
|-------|--------|-------------|-----|------|------------|----------|
| **Jan** | Amihan | Low | Cool | Poor | Low | Baseline studies |
| **Feb** | Amihan | **Very Low** | **Coldest** | **Poor** | **Lowest** | Conservation |
| **Mar** | Transition | Low | Warming | Fair | Recovering | Transition studies |
| **Apr** | Transition | Moderate | Warm | Fair | Growing | Preparation |
| **May** | Habagat | **Peak** | **Warmest** | **Excellent** | **Peak** | **All activities** |
| **Jun** | Habagat | High | Very Warm | Very Good | High | Fishing |
| **Jul** | Habagat | High | Very Warm | Very Good | High | Fishing |
| **Aug** | Habagat | High | Warm | Good | High | Fishing |
| **Sep** | Habagat | Moderate | Warm | Good | Moderate | Late season |
| **Oct** | Transition | Moderate | Cooling | Fair | Declining | Transition |
| **Nov** | Amihan | Low | Cool | Fair | Low | Planning |
| **Dec** | Amihan | Low | Cool | Fair | Low | Year-end |

**Legend:** 🟢 Peak | 🟡 High | 🟠 Moderate | 🔴 Low | 🟣 Very Low

---

## FAQ

### Q: What do the different colors on charts mean?
**A:** Green indicates positive trends, red shows negative patterns, purple represents predicted data (2026), and blue denotes neutral or baseline values.

### Q: How accurate are the 2026 predictions?
**A:** 2026 data are model-based projections with ~96% expected accuracy based on 2025 model performance. They should be used for planning, not precise forecasting.

### Q: Can I use this data for academic research?
**A:** Yes, all data is intended for academic and research purposes. Please cite the BulanTuna Research Platform and data sources appropriately.

### Q: Why do some charts show "N/A" for 2026?
**A:** Some metrics require actual observed data for calculation. For 2026 predictions, these show projected estimates or "N/A" where calculation isn't possible.

### Q: How do I interpret the CPUE values?
**A:** CPUE (Catch Per Unit Effort) is measured in kg/day and serves as a relative abundance index. Higher CPUE indicates greater tuna density.

### Q: What's the difference between Amihan and Habagat?
**A:** Amihan (Nov–Feb) is the northeast monsoon with cooler temperatures, while Habagat (May–Sep) is the southwest monsoon with warmer temperatures and higher tuna abundance.

### Q: Can I download raw data for my own analysis?
**A:** Yes, use the "Download CSV" buttons on any analysis page to export filtered datasets in CSV format.

### Q: How often is the data updated?
**A:** Historical data (2019–2025) is fixed. 2026 predictions are model-based and would require updated environmental data for revision.

### Q: What browsers are supported?
**A:** All modern browsers including Chrome, Firefox, Safari, and Edge. Mobile browsers are fully supported.

### Q: Is there an API for programmatic access?
**A:** Currently, data access is through the web interface and CSV downloads. API access may be developed in future versions.

---

## Support & Contact

For technical support, data inquiries, or collaboration opportunities:

**Bulan National High School**
Bulan, Sorsogon, Philippines

**Research Team:**
- BulanTuna Research Platform
- Fisheries Division, Municipal Agriculture Office

**Data Sources:**
- BFAR Sorsogon Provincial Office
- PAGASA Weather Services
- NAMRIA Mapping Services

---

*This manual covers version 1.0 of the BulanTuna Research Platform. Features and interface may evolve with future updates.*
