# Schema Design for Smart Clinic Management System

---

## MySQL Database Design

### Table: patients
- id: INT, Primary Key, AUTO_INCREMENT
- full_name: VARCHAR(100), NOT NULL
- email: VARCHAR(100), NOT NULL, UNIQUE
- phone: VARCHAR(15), NOT NULL
- gender: VARCHAR(10)
- date_of_birth: DATE
- created_at: TIMESTAMP DEFAULT CURRENT_TIMESTAMP

### Table: doctors
- id: INT, Primary Key, AUTO_INCREMENT
- full_name: VARCHAR(100), NOT NULL
- email: VARCHAR(100), NOT NULL, UNIQUE
- specialization: VARCHAR(100), NOT NULL
- phone: VARCHAR(15), NOT NULL
- profile_summary: TEXT
- is_active: BOOLEAN DEFAULT TRUE
- created_at: TIMESTAMP DEFAULT CURRENT_TIMESTAMP

### Table: appointments
- id: INT, Primary Key, AUTO_INCREMENT
- patient_id: INT, Foreign Key → patients(id), NOT NULL
- doctor_id: INT, Foreign Key → doctors(id), NOT NULL
- appointment_time: DATETIME, NOT NULL
- status: INT DEFAULT 0  -- (0=Scheduled, 1=Completed, 2=Cancelled)
- created_at: TIMESTAMP DEFAULT CURRENT_TIMESTAMP

### Table: admin
- id: INT, Primary Key, AUTO_INCREMENT
- username: VARCHAR(50), NOT NULL, UNIQUE
- password_hash: VARCHAR(255), NOT NULL
- role: VARCHAR(20) DEFAULT 'admin'
- last_login: DATETIME

### Table: doctor_availability
- id: INT, Primary Key, AUTO_INCREMENT
- doctor_id: INT, Foreign Key → doctors(id), NOT NULL
- available_date: DATE, NOT NULL
- start_time: TIME, NOT NULL
- end_time: TIME, NOT NULL

---

## MongoDB Collection Design

### Collection: prescriptions

```json
{
  "_id": "ObjectId('665dfe123abc456')",
  "appointmentId": 102,
  "patientId": 45,
  "doctorId": 7,
  "prescribedOn": "2025-06-20T10:30:00Z",
  "medications": [
    {
      "name": "Paracetamol",
      "dosage": "500mg",
      "frequency": "3 times a day",
      "duration": "5 days"
    },
    {
      "name": "Cough Syrup",
      "dosage": "10ml",
      "frequency": "2 times a day",
      "duration": "7 days"
    }
  ],
  "doctorNotes": "Avoid cold drinks and take complete rest.",
  "pharmacy": {
    "name": "Wellness Pharmacy",
    "address": "123 Main St, Springfield"
  },
  "refillInfo": {
    "allowed": true,
    "refillCount": 2
  }
}
