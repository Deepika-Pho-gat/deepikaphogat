# Hi, I'm Deepika Phogat 👋

<div align="center">

### Senior Data Analyst · Analytics Lead · BI Strategist
**Hyderabad, India** · Open to Senior Analyst / Assistant Manager / Analytics PM roles

[![LinkedIn](https://img.shields.io/badge/LinkedIn-deepikaphogat-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/deepikaphogat)
[![Email](https://img.shields.io/badge/Email-dphogat4121997@gmail.com-EA4335?style=flat&logo=gmail)](mailto:dphogat4121997@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-View%20My%20Work-00C9A7?style=flat)](https://deepikaphogat.github.io)

</div>

---

## 💥 Impact at a Glance

| Metric | Value | Where |
|--------|-------|--------|
| 💰 Incremental Collections | **$15M / year** | Tech Mahindra |
| 📦 Open Order Reduction | **37%** | Solenis |
| 📈 RPC Rate Increase | **30% in 2 months** | Tech Mahindra |
| ⚡ Reporting Automation | **40% effort saved** | Solenis |
| 💼 RPC Framework Impact | **$4M / year** | Tech Mahindra |
| 👥 Agents Forecasted | **300+** | Tech Mahindra |

---

## 🛠 Tech Stack

**Query & Programming**
```
SQL (Advanced)   ████████████████████  95%
Python / pandas  ████████████████░░░░  78%
SAS              ████████████████░░░░  82%
```

**BI & Visualization**
```
Tableau          ██████████████████░░  92%
Power BI         █████████████████░░░  88%
Advanced Excel   ████████████████████  94%
```

**Analytics & AI**
```
ETL Pipelines    ██████████████████░░  90%
Predictive Model ████████████████░░░░  80%
AI Tools (GPT/Copilot) █████████████████░░  85%
```

**Platforms:** `SAP` `Salesforce` `Microsoft 365` `JIRA`

---

## 🚀 Featured Projects

### 1. [$15M Collections Strategy Engine](./projects/collections-strategy)
> **Tech Mahindra · Python · SAS · SQL · Power BI · Decision Trees**

End-to-end analytics redesign of consumer collections operations. Built propensity scoring, behavioral segmentation, and dialing strategy optimization. Generated $15M in incremental annual collections across 300+ agents.

```python
# Decision tree segmentation — high-level approach
from sklearn.tree import DecisionTreeClassifier
import pandas as pd

# Features: days_delinquent, balance, prior_rpc, payment_history, channel_pref
model = DecisionTreeClassifier(max_depth=5, min_samples_leaf=50)
model.fit(X_train, y_train)  # y = 1 if payment collected

# Segment into High / Mid / Low propensity buckets
segments = pd.cut(model.predict_proba(X)[:,1], bins=[0,.4,.7,1], labels=['Low','Mid','High'])
```

**Impact:** $15M annual collections · 30% RPC rate increase · Division-wide adoption

---

### 2. [RPC Analytics Framework](./projects/rpc-framework)
> **Python · SAS · SQL · Behavioral Analytics**

Architected the Right Party Contact analytics framework from scratch — the first of its kind in the division. Combined contact timing optimization, channel propensity scoring, and willingness-to-pay modeling.

```sql
-- RPC scoring query (simplified)
SELECT
    account_id,
    customer_segment,
    best_contact_hour,
    channel_preference,
    propensity_score,
    RANK() OVER (PARTITION BY agent_id ORDER BY propensity_score DESC) AS priority_rank
FROM customer_scoring_model
WHERE propensity_score > 0.65
  AND last_rpc_attempt < CURRENT_DATE - 3
ORDER BY priority_rank;
```

**Impact:** $4M annual incremental collections · Adopted across multiple geographies

---

### 3. [SAP Order Backlog Elimination](./projects/sap-backlog)
> **SQL · SAP · Tableau · ETL Pipelines**

Built SQL ETL pipelines integrating SAP sales + inventory data into Tableau executive dashboards at Solenis. Identified bottlenecks eliminating 37% of open order backlog.

```sql
-- ETL pipeline: SAP order backlog KPI
WITH order_aging AS (
  SELECT
    order_id, customer_id, order_date,
    DATEDIFF(CURRENT_DATE, promised_delivery_date) AS days_overdue,
    order_value,
    CASE
      WHEN DATEDIFF(CURRENT_DATE, promised_delivery_date) > 30 THEN 'Critical'
      WHEN DATEDIFF(CURRENT_DATE, promised_delivery_date) > 14 THEN 'At Risk'
      ELSE 'On Track'
    END AS status
  FROM sap_orders
  WHERE status = 'OPEN'
)
SELECT status, COUNT(*) as orders, SUM(order_value) as value
FROM order_aging
GROUP BY status;
```

**Impact:** 37% open order reduction · 40% less manual reporting · Real-time KPI visibility

---

### 4. [AI-Augmented Analytics Workflow](./projects/ai-analytics)
> **Copilot · ChatGPT · Python · Tableau**

Piloted AI-assisted reporting at Solenis — using Copilot for automated KPI commentary and ChatGPT for natural language exception summaries on executive dashboards. Reduced time-to-insight by 25%.

```python
# AI-assisted commentary generation (Copilot-style pattern)
import openai

def generate_kpi_commentary(kpi_name, current_val, prev_val, benchmark):
    pct_change = ((current_val - prev_val) / prev_val) * 100
    prompt = f"""
    KPI: {kpi_name}
    Current: {current_val} | Previous: {prev_val} | Benchmark: {benchmark}
    Change: {pct_change:.1f}%
    Write a 2-sentence executive summary of this KPI trend.
    """
    response = openai.chat.completions.create(
        model="gpt-4", messages=[{"role":"user","content":prompt}]
    )
    return response.choices[0].message.content
```

---

## 📂 Repository Structure

```
deepikaphogat/
├── 📁 projects/
│   ├── collections-strategy/     # $15M impact model docs & approach
│   ├── rpc-framework/            # RPC scoring methodology
│   ├── sap-backlog/              # ETL pipeline architecture
│   └── ai-analytics/             # AI-augmented workflow examples
├── 📁 sql-snippets/              # Reusable SQL patterns (ETL, KPI, window functions)
├── 📁 python-notebooks/          # Data analysis notebooks
├── 📁 tableau-templates/         # Dashboard design patterns
└── README.md
```

---

## 🏆 Awards & Recognition

- 🥇 **Bravo Award ×3** — Process optimization & operational improvement (Tech Mahindra)
- 🏅 **Best Performer Q2** — Automated dashboards, 40% reporting efficiency gain
- 📊 **Analytics Innovation Contributor** — RPC framework adopted division-wide

---

## 📚 What I'm Learning

- `dbt` (data build tool) for analytics engineering
- `Apache Airflow` for ETL pipeline orchestration
- `LangChain` for AI-augmented analytics applications
- `PL-300` (Power BI Data Analyst certification)

---

## 💬 Let's Talk Data

I'm active on LinkedIn and open to:
- Senior Data Analyst / Analytics Lead opportunities
- Assistant Manager or Analytics PM roles
- Guest posts, webinars, or mentoring conversations about data analytics

📧 **dphogat4121997@gmail.com** · 🔗 **[linkedin.com/in/deepikaphogat](https://linkedin.com/in/deepikaphogat)**

---

<div align="center">
<i>"I don't just analyze data — I build analytics capabilities that outlast my individual contribution."</i>
</div>
