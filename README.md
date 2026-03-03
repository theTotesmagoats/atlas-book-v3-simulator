# ATLAS: THE BOOK v3.0 - Financial Advisor Simulator

## Overview

This is a single-file HTML/JS simulation of a financial advisor practice management system. It features:

- **Three-phase quarter execution**: Prepare → Alert Resolution → Finalize
- **Behavioral friction**: Client satisfaction, anxiety, and trust mechanics
- **Human capital management**: Staff hiring (Admins, Partners) with diminishing returns
- **Compliance state machine**: Field supervision alerts with meaningful tradeoffs

## Key Features

### 1. Time Allocation System
- Prospecting → Pipeline building
- Closing → Net New Assets (NNA)
- Servicing → Reduces client anxiety

### 2. Product Mix Strategy
- **Commission-based products**: High upfront NNA, higher churn, no trailing income
- **Fee-based planning**: Lower per-client NNA, recurring 1% trail, lower churn

### 3. Alert System
| Alert ID | Trigger | Options |
|----------|---------|---------|
| #1 | High churn after high-volume sales | Review closes (20hrs) vs. Ignore (churn risk) |
| #4 | Regulatory review requested | Pause closes vs. Submit later (fine risk) |
| #5 | Staffing shortfall | Hire admin ($15k) vs. Redistribute time |
| #6 | Sustainability warning | Force 10% insurance max vs. Accept risk |

### 4. Human Capital
- **Administrator**: $12k/quarter, reduces anxiety by 25 hrs
- **Junior Partner**: $30k/quarter + 20% equity split, closing multiplier with diminishing returns

## How to Use

1. Open `index.html` in any modern web browser
2. Allocate your 80 hours/quarter between prospecting, closing, and servicing
3. Manage your product mix slider (Commission vs. Fee-based)
4. Respond to Field Supervision alerts strategically
5. Build your practice toward Level 8+ unlocks

## Game States

- **Level Progression**: Based on cumulative NNA targets
- **Cash Reserves**: Must stay positive or face bankruptcy
- **Staff Satisfaction**: Impacts partner performance and alert severity
- **Trust Score**: Affects fine probabilities and alert handling flexibility

## Technical Notes

- State machine uses `state.temp` for quarter-local calculations with explicit reset to prevent leaks
- All slider values normalized from [0,100] to [0,1] before mathematical operations
- No division-by-zero or negative square root vectors exist in current implementation

## License

MIT License - Feel free to modify and redistribute.
