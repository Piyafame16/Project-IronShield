# 🛡️ Project IronShield: Mule Account Detection Intelligence

Welcome to **Project IronShield**. Our mission is to protect the banking ecosystem from APP Fraud and Mule Account networks through advanced behavioral analytics and proactive detection strategies.

## 🚀 Business Context
APP Fraud (Voluntary Transfer) has become a critical threat. **IronShield** analyzes "Voluntary" transaction patterns to distinguish between legitimate users and mule accounts, providing a balance between high-level security and seamless customer experience.

## 🎯 SMART Objectives
* **Recall Rate:** Identify > 85% of suspected mule accounts.
* **Loss Mitigation:** Reduce potential financial loss by 30% within the first 6 months of implementation.
* **Efficiency:** Reduce manual investigation time by 40% through automated "High-Risk" tagging.

## 🚀 Next Steps & Recommendations

### 1. Develop a Composite Risk Scoring Model
Transition from a binary static flag to a **Composite Risk Score**. By integrating multiple features—such as *Time Gap, Transaction Amount, Channel,* and *Transaction Type*—the system can more accurately distinguish between legitimate high-value users and fraudulent activity.

### 2. Implement Micro-structuring Detection
Implement automated alerts for **"Smurfing" or Micro-structuring patterns**. This involves detecting multiple small-value transfers sent to the same destination account within a short timeframe to bypass fixed transaction thresholds.

### 3. Architect a Real-time Detection Pipeline
To combat the 60-minute "Pass-Through" window, a real-time infrastructure is required:
* **Ingestion:** Kafka to capture real-time transaction events.
* **Processing:** Stream processors to calculate features on the fly.
* **Inference:** A scoring model to evaluate risk and trigger an **Auto-block or Hold** status within a **<100ms** latency window.

![System Architecture](images/system_architecture.png)
*Figure 3: Proposed Real-time Fraud Detection Pipeline.*

### 4. Introduce Dynamic Friction for High-Risk Transactions
Apply "Strategic Friction" to high-stakes scenarios. For transactions where the Risk Score is high and the amount exceeds **500,000 Baht**, the system will implement a **30-minute delay** combined with a mandatory **outbound verification call** from staff.

### 5. Real-world Validation & Model Governance
As the current findings are based on **Synthetic Data**, the derived thresholds must be validated against actual bank production data. Furthermore, a retraining pipeline will be established to adapt to evolving fraud patterns.

## 📂 Repository Structure
* `/data`
* `/dashboard`
* `/documents`
