# Pediatric Therapy Clinic Database System

A relational database schema and transactional dataset designed to manage logistics, employee specializations, and departmental structures for a multi-facility pediatric therapy clinic network.

## Core Architecture & ERD

The system is designed around strict healthcare data integrity rules, handling health systems, individual clinic locations, multi-tier employee rosters, and clinical certifications.

### Database Entities & Key Relationships

* **HealthSystem & Clinic:** A **One-to-Many** relationship (`HealthSystemId`) mapping parent healthcare corporate structures to individual clinic facilities.
* **Clinic & ClinicDepartment:** Houses internal operational divisions (e.g., Physical Therapy, Occupational Therapy, Speech-Language Pathology).
* **Employee & ClinicDepartment:** Maps organizational hierarchy and department management via foreign keys linking staff accounts.
* **CertifiedTherapist & ClinicSpecialty:** A bridging architecture utilizing composite keys (`ClinicSpecialtyId`, `EmployeeId`) to enforce, track, and validate professional licensing, certification dates, and renewal tracking.

---

## Getting Started / Deployment

To deploy this database locally and populate it with baseline transactional and configuration data:

1. Open **SQL Server Management Studio (SSMS)**.
2. Connect to your local or remote SQL Server Instance.
3. Create a new blank database:
   ```sql
   CREATE DATABASE PediatricTherapyClinic;
4. Open the `script.sql` file from this repository in a new query window (`File` ➔ `Open` ➔ `File...`).
5. Ensure your target database dropdown in the top toolbar is set to `PediatricTherapyClinic`, then click **Execute (F5)** to build the schema and seed the data.
