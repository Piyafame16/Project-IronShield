## 🛡️ Project IronShield: ระบบอัจฉริยะเพื่อการตรวจจับบัญชีม้า
ยินดีต้อนรับสู่ **Project IronShield** ภารกิจของเราคือการปกป้องระบบนิเวศทางการธนาคารจากภัยคุกคามของ APP Fraud (การหลอกให้โอนเงิน) และเครือข่ายบัญชีม้า (Mule Account Networks) ด้วยการประยุกต์ใช้การวิเคราะห์พฤติกรรมขั้นสูง (Advanced Behavioral Analytics) และกลยุทธ์การตรวจจับเชิงรุก เพื่อสร้างความปลอดภัยที่เหนือกว่าในทุกการทำธุรกรรม

## 🚀 บริบททางธุรกิจ (Bussiness Context)
ปัจจุบันปัญหา **APP Fraud (Authorized Push Payment Fraud)** ทวีความรุนแรงขึ้น โดยมิจฉาชีพใช้เครือข่าย **บัญชีม้า (Mule Accounts)** เป็นกลไกหลักในการยักย้ายถ่ายเทเงินออกนอกระบบภายในเวลาอันรวดเร็ว (มักเกิดขึ้นภายในไม่กี่นาที)

ข้อจำกัดของระบบตรวจจับรูปแบบเดิม (Legacy Rule-based) คือความล่าช้าและอัตราการตรวจจับที่ต่ำ ส่งผลให้ไม่สามารถระงับธุรกรรมได้ทันท่วงที **Project IronShield** จึงถูกพัฒนาขึ้นเพื่อประยุกต์ใช้ Behavioral Analytics และระบบตรวจจับแบบ Real-time เพื่อวิเคราะห์รูปแบบความผิดปกติของธุรกรรมและระบุพฤติกรรมที่เข้าข่ายบัญชีม้า โดยมุ่งเน้นที่การลดอัตราความเสียหาย (Fraud Loss) และรักษาสมดุลของ False Positive Rate เพื่อไม่ให้กระทบต่อผู้ใช้งานปกติ

## 🎯 วัตถุประสงค์ (Objectives)
* พัฒนา Machine Learning Model เพื่อตรวจจับและจำแนกบัญชีม้าจากพฤติกรรมธุรกรรมที่ผิดปกติ
* เพิ่มประสิทธิภาพการตรวจจับแบบ Real-time โดยเน้นการประมวลผลที่มีความหน่วงต่ำ (Low Latency)
* สร้าง Behavioral Baseline เพื่อแยกแยะระหว่างผู้ใช้งานปกติและกลุ่มพฤติกรรมเสี่ยง
* ลดมูลค่าความเสียหาย (Fraud Loss) ผ่านการระงับธุรกรรมในโซนอันตรายได้ทันท่วงที

## 🎯 SMART Objectives
* **อัตราการตรวจจับ (Recall Rate):** สามารถระบุและตรวจพบบัญชีที่เข้าข่ายบัญชีม้า (Suspected Mule Accounts) ได้มากกว่า 85%
* **การลดมูลค่าความเสียหาย (Loss Mitigation):** ลดมูลค่าความเสียหายทางการเงินที่อาจเกิดขึ้นลง 30% ภายใน 6 เดือนแรกหลังจากการเริ่มใช้งานระบบ
* **ประสิทธิภาพการปฏิบัติงาน (Efficiency):** ลดระยะเวลาที่ใช้ในการตรวจสอบโดยเจ้าหน้าที่ (Manual Investigation) ลง 40% ด้วยการใช้ระบบคัดกรองและติดสถานะ "ความเสี่ยงสูง" (High-Risk Tagging) แบบอัตโนมัติ

## 🖼️ Project Canvas
สามารถสรุปภาพรวมของโปรเจกต์ออกมาในรูปแบบ Project Canvas ได้ดังรูปนี้:

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
