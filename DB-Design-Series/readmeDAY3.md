Clinic Management System – ER Diagram README

Workflow
Patient Registration – Stores personal details.
Appointments – Patients schedule meetings with doctors; can have multiple appointments.
Consultations – Actual visits linked to appointments (or walk-ins); doctors record notes.
Diagnostic Tests – Prescribed during consultations; many-to-many relationship via Consultation_Test.
Reports – Generated for each test and linked to the consultation.
Payments – Linked to consultations and patients; multiple payments possible.

Key Entities
Patient – Patient details.
Doctor – Doctor details linked to Specialty.
Specialty – Medical specialty.
Appointment – Scheduled patient-doctor meetings.
Consultation – Actual visits with notes.
DiagnosticTest – Catalog of tests.
Consultation_Test – Junction table linking consultations and tests.
Report – Test results for consultations.
Payment – Records linked to consultations and patients.

Relationships
Patient → Appointment: 1:N
Doctor → Appointment: 1:N
Appointment → Consultation: 0..1:1
Consultation → Tests: M:N via Consultation_Test
Consultation → Report: 1:N
Consultation → Payment: 1:1 or 1:N
Patient → Payment: 1:N

Notes
Appointments != consultations; walk-ins allowed.
Tests and reports are linked to consultations, not just patients.
Design supports scalability, multiple visits, multiple tests per consultation, and realistic payment handling.

![DAY 3 DB Design PNG Image](Day3.png)
