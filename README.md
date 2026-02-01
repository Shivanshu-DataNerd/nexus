# Nexus  
### A Causal Attribution Engine for Explaining *Why* Things Happen

---

## The Problem

Modern analytics and monitoring systems are excellent at telling us **what happened** — revenue drops, latency spikes, error surges, SLA breaches.  
What they *don’t* answer is the most critical question:

> **Why did this happen?**

Most monitoring and ML systems rely on **correlation**, leaving engineers to manually piece together root causes across metrics, logs, deployments, and upstream systems.

---

## The Solution

**Nexus** is a **causal attribution engine** that goes beyond anomaly detection and focuses on **explainable system-level reasoning**.

Nexus:
- Detects anomalies in metrics and events
- Infers causal relationships across signals
- Attributes downstream impact to upstream causes
- Generates structured, human-readable causal reports

> **Nexus doesn’t just detect incidents — it explains them.**

---

## Architecture Overview

Data Ingestion → Anomaly Detection → Causal Reasoning → Causal Attribution Report (JSON)

---

## Repository Structure

.  
├── ingestion.ipynb  
├── anomaly_detection.ipynb   
├── causal_report_engine.ipynb   
├── causal_report.json   
├── Data pipeline/  
└── README.md  


---

## Causal Report Output (Example)

```json
{
  "event": "Revenue Drop",
  "timestamp": "2025-01-12T10:00:00Z",
  "anomaly_score": 0.91,
  "root_causes": [
    {
      "factor": "Checkout latency increase",
      "service": "Payment API",
      "causal_strength": 0.78,
      "confidence": 0.82
    }
  ],
  "upstream_changes": [
    "Deployment v2.3.1",
    "Database index removal"
  ],
  "recommended_actions": [
    "Rollback deployment v2.3.1",
    "Restore removed database index"
  ]
}
```
## Use Cases
- Incident root cause analysis (RCA)
- Revenue and KPI drop attribution
- SLA/SLO breach explanation
- Operational intelligence and observability
- Automated postmortems

## Why Causality

- Correlation shows what moved together.
- Causality explains what caused the movement.

>Nexus introduces a reasoning layer that modern data platforms are missing.

## Vision

- Production-grade causal reasoning engine
- Explicit causal graph modeling
- Azure Data Explorer (Kusto) and Microsoft Fabric integration
- LLM-assisted explanations
- Real-time incident intelligence

## Author
Shivanshu Pal  
Data Engineer  
E-mail: contactshiva7@gmail.com

## License
For research, learning, and demonstration purposes.
