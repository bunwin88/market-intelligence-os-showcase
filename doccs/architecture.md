# Architecture Notes

Market Intelligence OS is organized around modular workflow layers.

## Conceptual Architecture

```text
Data Sources
    ↓
Ingestion Layer
    ↓
Processing / Feature Layer
    ↓
Research and Scenario Layer
    ↓
Dashboard / GUI Layer
    ↓
Logging and Review Layer
```

---

## Layer 1: Data Sources

Potential data sources explored include:

* Live market data files
* Watchlist symbols
* Options-chain snapshots
* Portfolio visibility concepts
* Regime and macro indicators
* CSV/JSON research files
* Model-output files
* Diagnostic logs

---

## Layer 2: Ingestion Layer

The ingestion layer is responsible for receiving, copying, normalizing, and organizing incoming data.

Concepts explored:

* File watching
* Safe temp-copy reads
* Multi-symbol tick parsing
* Time-series sorting
* CSV/JSON normalization
* Data-quality checks
* Source-status diagnostics

---

## Layer 3: Processing and Feature Layer

The processing layer converts raw inputs into structured research-ready data.

Concepts explored:

* Tick-to-minute transformation
* OHLCV construction
* Technical indicator calculation
* Custom feature generation
* Scenario-ready datasets
* Research logs and audit trails

---

## Layer 4: Research and Scenario Layer

The research layer evaluates candidate ideas, model outputs, and scenario results.

Concepts explored:

* Scenario comparison
* Candidate scoring
* Paper-test signal generation
* Model-status visibility
* Cost sensitivity review
* Drawdown and win-rate review
* Exit-reason diagnostics

---

## Layer 5: Dashboard and GUI Layer

The dashboard layer gives the user operational visibility into the system.

Concepts explored:

* Main dashboard layout
* Market data status
* Model output panels
* Candidate review panels
* Diagnostic logs
* Latest signal display
* Research workflow controls

---

## Layer 6: Logging and Review Layer

The logging layer preserves system behavior for later review.

Concepts explored:

* Inference logs
* Event logs
* Candidate review logs
* Paper-test trade logs
* System-status logs
* Latest-signal JSON/CSV outputs
* Summary files

---

## Design Principle

```text
Research Signal ≠ Trade Execution
```

The system is intentionally designed so that research outputs, candidate scores, paper-test signals, and dashboards can be reviewed before any execution workflow is considered.
