# 🛡️ Project IronShield: Mule Account Detection Intelligence

Welcome to **Project IronShield**. Our mission is to protect the banking ecosystem from APP Fraud and Mule Account networks through advanced behavioral analytics and proactive detection strategies.

## 🚀 Business Context
APP Fraud (Voluntary Transfer) has become a critical threat. **IronShield** analyzes "Voluntary" transaction patterns to distinguish between legitimate users and mule accounts, providing a balance between high-level security and seamless customer experience.

## 🎯 SMART Objectives
* **Recall Rate:** Identify > 85% of suspected mule accounts.
* **Loss Mitigation:** Reduce potential financial loss by 30% within the first 6 months of implementation.
* **Efficiency:** Reduce manual investigation time by 40% through automated "High-Risk" tagging.

## 🛠️ Project Architecture (Our Solution)
To address the challenges of real-time data, Project IronShield proposes a **Hybrid Detection Pipeline**:
1. **Tier 1 (Streaming):** Utilizing **Apache Kafka** to ingest real-time transaction data.
2. **Tier 2 (Filtering):** Applying **Rule-based Thresholds** (e.g., Median-based Outliers) for low-latency filtering.
3. **Tier 3 (Analytics):** High-fidelity AI Model processing for complex behavioral patterns.

## 📂 Repository Structure
* `/data`
* `/dashboard`
* `/documents`
