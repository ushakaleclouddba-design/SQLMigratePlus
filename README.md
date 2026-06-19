# ⚡ SQLMigratePlus

> AI-powered SQL Server to Azure migration agent — the only migration tool with an automated Handoff stage that generates connection strings and migration receipts for app teams.

🌐 **Live at [sqlmigrateplus.com](https://sqlmigrateplus.com)**

---

## 🚀 What is SQLMigratePlus?

SQLMigratePlus is an end-to-end AI agent that automates SQL Server to Azure database migrations across 5 stages — from initial assessment through Day-2 operations. Built on the Claude API with a PowerShell ReAct loop, it eliminates tribal knowledge from the migration process and produces auditable, compliance-ready outputs at every stage.

**The problem it solves:** Enterprise database migrations fail because teams rely on manual scripts and tribal knowledge. The next DBA starts from scratch every time. SQLMigratePlus automates the full chain — assessment to Day-2 — so nothing is lost.

---

## 🏗️ 5-Stage Workflow

```
┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│   ASSESS    │ →  │   DECIDE    │ →  │   MIGRATE   │ →  │   HANDOFF   │ →  │  DAY-2 OPS  │
│             │    │             │    │             │    │             │    │             │
│ Discovery   │    │ Multi-cloud │    │ Migration   │    │ Connection  │    │ Runbook     │
│ Inventory   │    │ TCO report  │    │ execution   │    │ strings     │    │ Monitoring  │
│ Risk scan   │    │ Path select │    │ Validation  │    │ Receipts    │    │ Alerts      │
└─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘
```

---

## ⚙️ How It Works

SQLMigratePlus runs a **PowerShell ReAct loop** powered by the Claude API:

```
User Input → Claude API (tool-use agent)
                    ↓
            Select tool from 5 typed tools:
            ├── assess_server      → Discovery, inventory, risk scan
            ├── calculate_tco      → Multi-cloud cost comparison (Azure/AWS/GCP)
            ├── execute_migration  → Run migration with validation
            ├── generate_handoff   → Connection strings + migration receipts
            └── day2_operations    → Runbook, monitoring, alert setup
                    ↓
            Human-in-the-loop approval gate
                    ↓
            Append-only JSON audit log
```

---

## 🌟 Key Features

| Feature | Description |
|---------|-------------|
| **AI-powered assessment** | Claude API analyses server inventory, flags risks, recommends migration path |
| **Multi-cloud TCO** | 11-sheet Excel report comparing Azure, AWS, and GCP costs |
| **Anti-hallucination grounding** | Agent grounded with real server data — no fabricated outputs |
| **Human-in-the-loop gates** | Approval required before destructive operations |
| **Automated Handoff stage** | Auto-generates connection strings and migration receipts for app teams |
| **Day-2 runbook** | Post-migration operational runbook generated automatically |
| **Append-only audit log** | JSON audit trail for SOX/PCI compliance |
| **Version v0.9.1** | Packaged, versioned, production-ready |

---

## 🏦 Built for Banking & Financial Services

SQLMigratePlus was designed with banking compliance requirements in mind:

- **SOX** — append-only audit log, every action timestamped
- **PCI DSS** — no credentials stored in plain text, Key Vault integration
- **FFIEC** — risk assessment output documents regulatory posture
- **Change management** — human approval gates before execution

---

## 🗺️ Roadmap

SQLMigratePlus is designed to expand beyond SQL Server:

- ✅ SQL Server → Azure SQL Managed Instance
- ✅ SQL Server → Azure SQL Database
- 🔜 Oracle → Azure Database
- 🔜 MySQL → Azure Database for MySQL
- 🔜 PostgreSQL → Azure Database for PostgreSQL
- 🔜 Multi-cloud: AWS RDS, GCP Cloud SQL paths

---

## 🛠️ Tech Stack

- **AI Engine** — Anthropic Claude API (tool-use agent)
- **Orchestration** — PowerShell ReAct loop
- **Assessment output** — Excel (11 sheets, multi-cloud TCO)
- **Audit trail** — Append-only JSON log
- **Infrastructure** — Terraform IaC provisioning
- **Secrets** — Azure Key Vault integration
- **Site** — GitHub Pages at sqlmigrateplus.com

---

## 📁 Repository Structure

```
SQLMigratePlus/
│
├── index.html          # Portfolio site — sqlmigrateplus.com
├── CNAME               # Custom domain configuration
└── README.md
```

> The SQLMigratePlus agent source code lives in the main portfolio repo:
> [Azure-Data-Engineering-Portfolio/10-AIAgents/SQLMigratePlus](https://github.com/ushakaleclouddba-design/Azure-Data-Engineering-Portfolio/tree/main/10-AIAgents/SQLMigratePlus)

---

## 📚 Related Repositories

| Repo | Description |
|------|-------------|
| [Azure-Data-Engineering-Portfolio](https://github.com/ushakaleclouddba-design/Azure-Data-Engineering-Portfolio) | 12 Azure migration POCs — DMS, LRS, TDE, Always On AG, ADF |
| [Banking-Lakehouse-Databricks](https://github.com/ushakaleclouddba-design/Banking-Lakehouse-Databricks) | 2.26M loan records, Bronze/Silver/Gold, Claude API risk narratives |

---

## 👤 Author

**Usha Kale**
Azure Data Engineer & Senior Cloud DBA | 15+ years in Banking & Financial Services

- 🌐 [sqlmigrateplus.com](https://sqlmigrateplus.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/usha-kale-56a336a)
- 🐙 [GitHub](https://github.com/ushakaleclouddba-design)

---

## 📜 License

MIT License. See `LICENSE` for details.
