# CORE_SYSTEM_FILES.md

## Overview
This document defines the **essential markdown files** required to run the funding assistant effectively. These files form the core intelligence layer that powers qualification, matching, offer generation, and conversion.

---

## 🧠 1. AGENTS.md
Defines the assistant’s internal roles and responsibilities.

### Purpose:
- Breaks the assistant into functional roles:
  - Qualifier (collects user data)
  - Matcher (aligns user with lenders)
  - Advisor (improves approval odds)
  - Closer (drives CTA + application)

### Key Contents:
- Role definitions
- When each role activates
- Transition logic between roles

---

## ⚙️ 2. SYSTEM_CONFIG.md
Global rules and behavioral guardrails.

### Purpose:
- Controls how the assistant interacts with users
- Enforces structure and consistency

### Key Contents:
- One-question rule
- Qualification flow order
- CTA rules (anchor text only)
- Offer readiness requirements
- Response style guidelines

---

## 🧩 3. SKILLS.md
Defines what the assistant is capable of doing.

### Purpose:
- Expands assistant capabilities beyond basic Q&A

### Key Contents:
- Qualification
- Offer matching
- Credit coaching
- Scenario simulation
- Document guidance
- Follow-up generation

---

## 🎯 4. ACTIONS.md
Defines executable actions the assistant can take.

### Purpose:
- Creates a clear action framework for decision-making

### Core Actions:
- qualify_user
- match_offers
- improve_profile
- simulate_scenarios
- generate_followup
- push_to_api

---

## 💰 5. UNDERWRITING_RULES.md
Core approval and eligibility logic.

### Purpose:
- Determines which users qualify for which products

### Key Contents:
- Revenue thresholds
- Time in business minimums
- Credit score tiers
- Industry restrictions
- Risk flags

---

## 🤝 6. LENDER_CRITERIA.md
Detailed breakdown of each funding partner.

### Purpose:
- Enables precise matching

### Key Contents:
- Lender name
- Min requirements
- Preferred profiles
- Deal breakers
- Product types offered

---

## 📊 7. OFFER_TEMPLATES.md
Standardized offer output structure.

### Purpose:
- Ensures consistent, high-quality presentation

### Key Contents:
- Amount
- Term
- Rate (APR or factor)
- Payment structure
- Fees
- Lender name
- CTA formatting rules

---

## 🧾 8. INTAKE_FLOW.md
Controls how user data is collected.

### Purpose:
- Optimizes conversion and reduces friction

### Key Contents:
- Question sequence
- One-question enforcement
- Conditional branching logic
- When to move to next stage

---

## 🔗 9. API_PAYLOADS.md
Defines how applications are submitted.

### Purpose:
- Standardizes integration with funding APIs

### Key Contents:
- Finta payload structure
- Lendflow payload structure
- Required vs optional fields

---

## 🧠 10. DATA_SCHEMA.md
Defines all required data fields.

### Purpose:
- Ensures consistency across qualification + API

### Key Fields:
- business_name
- entity_type
- time_in_business
- monthly_revenue
- annual_revenue
- credit_score_range
- funding_amount
- use_of_funds

---

## 🚫 11. DECLINE_REASONS.md
Tracks why deals fail.

### Purpose:
- Improves assistant recommendations

### Key Contents:
- Low revenue
- Short time in business
- Poor credit
- Risky industry
- Negative banking behavior

---

## 🔐 12. COMPLIANCE.md
Legal and regulatory safeguards.

### Purpose:
- Protects user and system

### Key Contents:
- Lending disclaimers
- Data usage policies
- Limitations of offers

---

## 🔁 13. DEMO_OFFERS.md
Fallback offers when APIs are unavailable.

### Purpose:
- Ensures uninterrupted user experience

### Key Contents:
- 2–3 mock lenders
- Realistic ranges
- Tier-based offer examples

---

## 📁 Recommended Folder Structure

/core
  ├── AGENTS.md
  ├── SYSTEM_CONFIG.md
  ├── SKILLS.md
  ├── ACTIONS.md

/funding
  ├── UNDERWRITING_RULES.md
  ├── LENDER_CRITERIA.md

/offers
  ├── OFFER_TEMPLATES.md
  ├── DEMO_OFFERS.md

/intake
  ├── INTAKE_FLOW.md
  ├── DATA_SCHEMA.md

/api
  ├── API_PAYLOADS.md

/risk
  ├── DECLINE_REASONS.md

/compliance
  ├── COMPLIANCE.md

---

## ✅ Implementation Notes

- Start with the **Core 5**:
  - AGENTS.md
  - SYSTEM_CONFIG.md
  - UNDERWRITING_RULES.md
  - INTAKE_FLOW.md
  - OFFER_TEMPLATES.md

- Add remaining files incrementally
- Keep formatting clean and structured for retrieval
- Use consistent naming conventions across all files

---

## 🎯 Outcome

With these files in place, the assistant will:
- Qualify users faster
- Match more accurately
- Generate realistic offers
- Convert more users into applications
