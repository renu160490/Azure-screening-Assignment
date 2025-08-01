# Azure-screening-Assignment
# Azure Cosmos DB Cost Optimization Solution – Assignment

##  Submitted by: Renu Singh

##  Objective

Optimize costs for a **read-heavy Azure Cosmos DB** workload where:
- Records older than 3 months are rarely accessed
- There should be **no data loss, no downtime**, and
- **No changes to existing API contracts**

---

##  Proposed Solution

### Hybrid Data Tiering Strategy

- **Hot Tier**: Keep recent data (last 3 months) in Azure Cosmos DB
- **Cold Tier**: Move older data to Azure Blob Storage

This approach enables:
- ✅ Cost savings on Cosmos DB storage and throughput
- ✅ Continued access to all data with acceptable latency
- ✅ Seamless fallback for archived data

---

##  Cost Comparison

| Item | Cosmos DB | Blob Storage |
|------|-----------|--------------|
| Storage (per GB) | ₹20–₹25      | ₹1.5–₹2     |
| RU/s for reads   | Charged      | None (on-demand) |
| Potential RU/s savings | Up to 60–80% | — |

If 80% of your data is older than 3 months, this approach can cut Cosmos DB costs by **over 50%**.






