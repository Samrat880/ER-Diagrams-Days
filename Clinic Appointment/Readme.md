# Clinic Appointment Management Ecosystem - ER Diagram

<img width="2498" height="1476" alt="diagram-export-8-4-2026-7_41_50-pm" src="https://github.com/user-attachments/assets/05dd3681-542e-4a6a-bbbc-933a577fae4b" />


## Overview
This ER diagram models a clinic appointment system where patients book doctors, receive consultations, get prescriptions and diagnostics, and complete billing with invoices and payments.

It is not just a booking system. It is a full clinical and billing workflow.

## My Approach
I designed the schema in layers so the model stays clean and scalable:

1. Identity: users, patient_profiles, doctor_profiles, specialties
2. Availability: doctor_schedules
3. Care Flow: appointments, consultations, prescriptions, prescription_items
4. Diagnostics: diagnostic_catalog, test_reports
5. Billing: invoices, invoice_line_items, payments

## Key Design Decisions
- Separated authentication data in users from doctor and patient profiles for better normalization.
- Added specialties and doctor_schedules to support practical doctor discovery and availability mapping.
- Kept consultations separate from appointments so medical data starts only when care actually happens.
- Split prescriptions into header and line items for flexible medicine-level instructions.
- Designed diagnostics with a test catalog plus test reports to support reusable test definitions.
- Used invoices, line items, and payments to represent realistic clinic billing and partial payment flows.

## Relationship Summary
- One user can map to one patient profile or one doctor profile based on role.
- One specialty can have many doctors.
- One doctor can have many schedule slots and many appointments.
- One patient can have many appointments and many invoices over time.
- One appointment can produce one consultation and one invoice.
- One consultation can produce one prescription and many diagnostic test reports.
- One prescription can have many prescribed medicine items.
- One invoice can have many line items and many payments.

## Files
- eraser.txt (Eraser schema source)
- Clinic Appointment.png (exported ER diagram)

## Conclusion
The goal was to keep the model practical, healthcare-oriented, and easy to extend for future needs like receptionist operations, insurance workflows, and reporting.
