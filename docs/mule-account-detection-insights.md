# Analysis Findings: Fraud Detection and Mule Account Patterns

### 1. Pass-Through Pattern as the Primary Behavioral Signal
Mule accounts exhibit a clear **"Pass-Through"** behavior, receiving and transferring out funds within an average of **6 hours**. In contrast, normal accounts typically hold funds for over **30 hours**. Notably, some high-risk accounts move funds within **60 minutes**, significantly outpacing current system detection speeds.
<img width="1903" height="1143" alt="Screenshot 2026-05-11 232244" src="https://github.com/user-attachments/assets/b7d971b1-d255-4ae5-a2ff-8430d0e4625f" />

### 2. Transaction Amount Overlap
The median fraud transaction value is **155 times higher** than normal transactions. However, there is a significant overlap as legitimate customers also perform high-value transfers (e.g., real estate purchases or investments). Consequently, **transaction volume alone is an insufficient predictor** for fraud detection.
<img width="1908" height="1147" alt="Screenshot 2026-05-11 232352" src="https://github.com/user-attachments/assets/984872bb-59ab-4107-8f19-2b6766ef9144" />

### 3. High-Risk Channels: Transfer and QR Code
Bank transfers and QR payments are the highest-risk channels, with fraud rates of **7.6%** and **5.0%** respectively. This is markedly higher than Bill Payments or Top-ups, aligning with criminal preferences for channels that offer instantaneous liquidity and are harder to trace.
<img width="1906" height="1149" alt="Screenshot 2026-05-11 232447" src="https://github.com/user-attachments/assets/663ac31d-f061-4773-826f-b67346f51882" />


