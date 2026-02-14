# whythisprice

- START HERE

## What You're Building

A **transparent, explainable AI system** that analyzes Indian stocks by:

1. **Running 3 independent agents** (Fundamentals, Technicals, Sentiment)
2. **Correlating their insights** across multiple dimensions
3. **Producing clear narratives** that explain: CAUSE → EFFECT → PRICE
4. **Creating full audit trails** so investors understand every decision

**Key Principle:** NOT prediction. EXPLANATION. Complete transparency.

---

## Part 1: The Multi-Agent Architecture

### 1.1 Core Agent System

Your system will have **4 Primary Agents** + **3 Supporting Agents**:

#### Primary Analysis Agents

```
┌─────────────────────────────────────────────────────────────┐
│                      User Query                              │
│        "Analyze TCS for Feb 2025 investment decision"        │
└──────────────────┬──────────────────────────────────────────┘
                   │
        ┌──────────┼──────────┐
        ↓          ↓          ↓
   ┌─────────┐ ┌─────────┐ ┌──────────┐
   │Fundamental│Technical │ News/      │
   │Agent     │Agent     │ Sentiment  │
   │          │          │ Agent      │
   └────┬────┘ └────┬────┘ └─────┬────┘
        │           │            │
        └───────────┼────────────┘
                    │
            ┌───────▼────────┐
            │ Correlation    │
            │ Engine         │
            └────────┬───────┘
                     │
            ┌────────▼────────┐
            │ Narrative       │
            │ Generator       │
            └────────┬───────┘
                     │
            ┌────────▼────────┐
            │ Auditor         │
            │ (Trace + Log)   │
            └────────┬───────┘
                     │
            ┌────────▼────────┐
            │ Output          │
            │ Report          │
            └─────────────────┘
```

---

# Architecture Diagrams: Multi-Agent Stock Analysis System

## System Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                       USER QUERY                                │
│              "Analyze TCS for investment"                        │
└─────────────────────────────┬───────────────────────────────────┘
                              │
                              ↓
                    ┌─────────────────────┐
                    │  Data Broker        │
                    │ (Fetch NSE/BSE)     │
                    └────┬────────┬───┬───┘
          ┌─────────────┘ │       │   └──────────────┐
          │               │       │                  │
    Financial         Price      News             Analyst
    Statements        History    Articles         Views
          │               │       │                  │
          └───────────────┼───────┼──────────────────┘
                          │       │
          ┌───────────────┴───┬───┴──────────────────┐
          │                   │                      │
          ↓                   ↓                      ↓
    ┌──────────────┐   ┌──────────────┐   ┌──────────────────┐
    │ Fundamental  │   │  Technical   │   │ Sentiment &      │
    │ Agent        │   │  Agent       │   │ Catalyst Agent   │
    │              │   │              │   │                  │
    │ • P/E, ROE   │   │ • Trends     │   │ • News sentiment │
    │ • Growth     │   │ • Support/R  │   │ • Analyst views  │
    │ • Margins    │   │ • Indicators │   │ • Catalysts      │
    │ • Debt       │   │ • Volume     │   │ • Events         │
    │              │   │              │   │                  │
    │ Score: 0-10  │   │ Score: 0-10  │   │ Score: 0-10      │
    └───────┬──────┘   └───────┬──────┘   └────────┬─────────┘
            │                  │                   │
            └──────────────────┼───────────────────┘
                               │
                       ┌───────▼────────┐
                       │ Correlation    │
                       │ Engine         │
                       │                │
                       │ • Alignment    │
                       │ • Weighting    │
                       │ • Confidence   │
                       │                │
                       │ Consensus: 6.7 │
                       │ Confidence:78% │
                       └───────┬────────┘
                               │
                       ┌───────▼──────────┐
                       │ Narrative        │
                       │ Generator        │
                       │                  │
                       │ CAUSE → EFFECT   │
                       │ → PRICE          │
                       │                  │
                       │ "Given...        │
                       │  fundamentals    │
                       │  strong, chart   │
                       │  bullish,        │
                       │  sentiment       │
                       │  positive, we    │
                       │  expect 4200"    │
                       └───────┬──────────┘
                               │
                       ┌───────▼──────────┐
                       │ Auditor          │
                       │ (Full Trace)     │
                       │                  │
                       │ JSON audit log   │
                       │ with every calc  │
                       └───────┬──────────┘
                               │
                       ┌───────▼──────────┐
                       │  OUTPUT REPORT   │
                       │  • Recommendation│
                       │  • Target Price  │
                       │  • Stop-Loss     │
                       │  • Narrative     │
                       │  • Audit Trail   │
                       └──────────────────┘
```

---

---

## Summary

This architecture enables:

✅ **Parallel Processing** - All agents run simultaneously (5-30s)
✅ **Resilience** - Fallback data sources if primary fails
✅ **Transparency** - Every score has visible formula
✅ **Scalability** - Run 1000 stocks/day on cloud
✅ **Learning** - Track accuracy, optimize weights
✅ **Auditability** - Full JSON trail of every decision

The system is built for **explanation, not prediction**.
Every recommendation is **traceable to its source formula**.