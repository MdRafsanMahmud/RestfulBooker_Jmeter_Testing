# 🧪 Restful Booker - JMeter Performance & Stress Testing

This project demonstrates performance and stress testing on the [Restful Booker API](https://restful-booker.herokuapp.com) using **Apache JMeter**. It includes simulation of real-world traffic: login, create booking, and search booking, along with timed execution and report generation.

---

## ✅ What Has Been Done

* Designed a JMeter test plan (`booking.jmx`) that simulates:

  * User login
  * Booking creation with random data
  * Booking search using extracted booking ID
* Applied a **Gaussian Random Timer** (Deviation: 2000ms, Constant Delay: 500ms) for realistic traffic simulation
* Performed Load Testing in 3 steps:

  * Step 1: 5 minutes
  * Step 2: 10 minutes
  * Step 3: 20 minutes
* Performed Stress Testing by gradually increasing users until bottlenecks were observed
* Collected test results in `.jtl` format and generated:

  * 📊 HTML reports
  * 📈 Excel summary: `booking-api-test-report.xlsx`

---

## 🔧 Prerequisites

* JMeter 5.5 or later
* Java 8 or higher
* Git (for cloning the repo)

---

## 🚀 How to Run the Test

```bash
# Step 1: Clone the repo
git clone https://github.com/your-username/RestfulBooker_Jmeter_Testing.git
cd RestfulBooker_Jmeter_Testing

# Step 2: Open booking.jmx in JMeter

# Step 3: Run the test (GUI or CLI mode)
# For GUI: Open booking.jmx in JMeter and press Start
# For CLI:
jmeter -n -t booking.jmx -l booking.jtl

# Step 4: Generate HTML report
jmeter -g booking.jtl -o Reports/

# Optional: Replace old report
rm -rf Reports/ booking.jtl
```
## 📷 Screenshots

## 📈 Load Test Report
### Step1_5_Min
![image](https://github.com/user-attachments/assets/ce110271-a856-45ed-9a0b-fa1034028000)
### Step2_10_Min
![image](https://github.com/user-attachments/assets/35fdd37f-fc1b-4ef2-b1c0-cc3d64c31baa)
### Step3_20_Min
![image](https://github.com/user-attachments/assets/194cc00e-f328-4ceb-ab3c-4108d35ee45d)





## 📉 Stress Test Report (Excel)
### Iteration 2
![image](https://github.com/user-attachments/assets/ceb48546-3182-456c-89cb-942d74121adf)
### Iteration 2.1
![image](https://github.com/user-attachments/assets/0ea4b5af-a3b5-4f6c-aa1a-98d3d5fecd8c)
### Iteration 2.1.1
![image](https://github.com/user-attachments/assets/adbe6903-8a5d-4b1f-ac75-0c9ca5f5a0ce)
### Iteration 2.1.2
![image](https://github.com/user-attachments/assets/09ad6ff1-d5a9-4219-a896-991f591a0453)
### Iteration 2.1.3 (Breakdown Point)
![image](https://github.com/user-attachments/assets/485b02ea-f9f8-4fc5-833e-987f763f1431)

---





