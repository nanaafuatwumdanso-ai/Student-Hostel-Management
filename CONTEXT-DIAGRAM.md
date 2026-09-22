# Student Hostel Management System Context Diagram

## System Context

The Student Hostel Management System consists of several interconnected domains that work together to manage student accommodation and hostel operations.

```mermaid
flowchart LR

    Student[Student]

    Accommodation[Student & Accommodation Management]
    Billing[Billing & Payments]
    Maintenance[Maintenance Management]
    Security[Security & Visitor Management]
    Communication[Communication & Notifications]
    Administration[Hostel Administration & Reporting]

    MaintenanceStaff[Maintenance Staff]
    SecurityOfficer[Security Officer]
    FinanceOfficer[Finance Officer]
    AccommodationOfficer[Accommodation Officer]
    HostelAdmin[Hostel Administrator]

    Student -->|Registration / Booking| Accommodation
    Accommodation -->|Payment Request| Billing
    Billing -->|Payment Status| Accommodation

    Student -->|Maintenance Complaint| Maintenance
    Maintenance -->|Maintenance Updates| Student

    Student -->|Visitor Registration| Security
    Security -->|Visitor Information| Student

    Accommodation -->|Booking / Room Updates| Communication
    Billing -->|Payment Updates| Communication
    Maintenance -->|Maintenance Updates| Communication
    Security -->|Security Updates| Communication

    Communication -->|Notifications| Student

    MaintenanceStaff -->|Repair Updates| Maintenance
    SecurityOfficer -->|Security Records| Security
    FinanceOfficer -->|Payment Records| Billing
    AccommodationOfficer -->|Room Allocation| Accommodation

    HostelAdmin -->|Manage| Accommodation
    HostelAdmin -->|Manage| Billing
    HostelAdmin -->|Manage| Maintenance
    HostelAdmin -->|Manage| Security
    HostelAdmin -->|Monitor| Administration

    Accommodation -->|Accommodation Data| Administration
    Billing -->|Financial Data| Administration
    Maintenance -->|Maintenance Data| Administration
    Security -->|Security Data| Administration
