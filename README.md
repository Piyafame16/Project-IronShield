## 🛡️ Project IronShield: Intelligent System for Mule Account Detection
Welcome to **Project IronShield**. Our mission is to safeguard the banking ecosystem against the threats of APP Fraud (Authorized Push Payment Fraud) and Mule Account Networks by applying Advanced Behavioral Analytics and proactive detection strategies, ensuring superior security across all transactions.

## 🚀 Business Context
The issue of **APP Fraud (Authorized Push Payment Fraud)** has become increasingly severe. Fraudsters exploit **Mule Accounts** as the primary mechanism to rapidly move funds out of the system—often within just a few minutes.

Traditional **rule-based detection systems** face limitations such as delays and low detection rates, making them ineffective in stopping fraudulent transactions in time. **Project IronShield** was developed to leverage **Behavioral Analytics** and **Real-time Detection** to identify abnormal transaction patterns and flag mule-like behaviors. The focus is on reducing **fraud losses** while maintaining a balanced **false positive** rate to avoid disrupting legitimate users.

## 🎯Objectives
* Develop a Machine Learning Model to detect and classify mule accounts based on abnormal transaction behaviors.
* Enhance real-time detection efficiency with low latency processing.
* Establish a Behavioral Baseline to distinguish normal users from high-risk behavioral groups.
* Minimize fraud losses by promptly blocking transactions in high-risk zones.

## 🎯 SMART Objectives
* **Detection Rate (Recall Rate):** Identify suspected mule accounts with accuracy above 85%.
* **Loss Mitigation:** Reduce potential financial losses by 30% within the first six months of system deployment.
* **Operational Efficiency:** Cut manual investigation time by 40% through automated screening and High-Risk Tagging.

## 🖼️ Project Canvas
The overall project can be summarized in a Project Canvas as illustrated below.

![Project Canvas]("Project-IronShield/ProjectCanvas.jpg")

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

### 4. Introduce Dynamic Friction for High-Risk Transactions
Apply "Strategic Friction" to high-stakes scenarios. For transactions where the Risk Score is high and the amount exceeds **500,000 Baht**, the system will implement a **30-minute delay** combined with a mandatory **outbound verification call** from staff.

### 5. Real-world Validation & Model Governance
As the current findings are based on **Synthetic Data**, the derived thresholds must be validated against actual bank production data. Furthermore, a retraining pipeline will be established to adapt to evolving fraud patterns.

## 📂 Repository Structure
* `/data`
* `/dashboard`
* `/documents`
