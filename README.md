# whythisprice


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