# Hospital-Revenue-Leakage-and-Operations-Analysis
SQL analysis of hospital revenue leakage and appointment throughput using complex aggregations, window functions, and multi-table joins

---

## Dataset
- **Source:**  https://www.kaggle.com/datasets/kanakbaghel/hospital-management-dataset (kaggle)
- **Size:**  Row count : patients - 50, billing - 200, appointments - 200, doctors - 10, treatments - 200.
- **Time period:** Multi-year patient transaction and visit logs
- **Key columns:** patients: patient_id (PK), date_of_birth, insurance_provider
doctors: doctor_id (PK), specialty, hospital_branch
appointments: appointment_id (PK), patient_id (FK), doctor_id (FK), status
treatments: treatment_id (PK), appointment_id (FK), treatment_type, cost
billing : bill_id (PK), patient_id (FK), treatment_id (FK), total_amount, payment_method, payment_status.

---

## Tools Used
- SQL (MySQL)

---

## Key Findings
- **Insurance Claims Drive Revenue Leakage:** Unpaid and pending billing is heavily tied to insurance workflows making insurance claim delays the primary source of cash flow bottlenecks.
- **Capacity Loss from Cancellations:** Analyzing completion vs. cancellation/no-show rates per doctor highlights operational inefficiencies, showing where clinical capacity and doctor time are going underutilized.
- **Demographic & Service Concentration:** Revenue leakage and treatment demand are concentrated within specific age segments and high-cost treatment categories, indicating clear targets for preventive packages and billing interventions.

---

## Recommendations
- **Check Insurance Before Treatment:** Verify every patient's insurance at the front desk before they see the doctor. Catching coverage issues early prevents claims from being rejected later.
- **Send Automatic Text Reminders:** Send SMS or WhatsApp reminders 24 to 48 hours before appointments. This helps patients remember their visits, reduces last-minute cancellations, and keeps doctors' schedules full.
- **Offer Simple Payment Plans for Large Bills:** Create bundled health packages and flexible payment options for expensive treatments. Making bills easier to pay helps the hospital collect money faster and avoids unpaid debt.

---

## Files in This Repository
- `Hospital-Revenue-Leakage-and-Operations-Analysis.sql` - all queries with comments

---

## How to Run
- 1.Download Hospital-Revenue-Leakage-and-Operations-Analysis.sql from the repository
- 2.Load the script into MySQL Workbench or your preferred SQL tool
- 3.Run queries in order — each block is annotated with its business question
