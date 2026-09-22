# Domain Mapping

## 1. Student & Accommodation Management

### Responsibility

Manages student registration, hostel applications, room availability, bookings, room allocation, check-in, and check-out.

### Main Entities

- Student
- Student Account
- Hostel
- Room
- Bed
- Booking
- Room Allocation
- Check-In
- Check-Out

---

## 2. Billing & Payments

### Responsibility

Manages hostel fees, invoices, payments, receipts, outstanding balances, and refunds.

### Main Entities

- Hostel Fee
- Invoice
- Payment
- Payment Receipt
- Outstanding Balance
- Refund

---

## 3. Maintenance Management

### Responsibility

Manages maintenance complaints, repair requests, work orders, maintenance staff assignments, and repair status.

### Main Entities

- Maintenance Request
- Maintenance Staff
- Work Order
- Repair
- Maintenance Status

---

## 4. Security & Visitor Management

### Responsibility

Manages visitors, visitor registration, entry and exit records, security incidents, and hostel access.

### Main Entities

- Visitor
- Visitor Pass
- Security Officer
- Entry Record
- Exit Record
- Incident Report

---

## 5. Communication & Notifications

### Responsibility

Manages announcements, student complaints, messages, and notifications relating to hostel activities.

### Main Entities

- Notification
- Announcement
- Message
- Complaint
- Complaint Status

---

## 6. Hostel Administration & Reporting

### Responsibility

Provides hostel administrators and staff with tools for managing records, monitoring occupancy, generating reports, and overseeing hostel operations.

### Main Entities

- Hostel Administrator
- Accommodation Officer
- Finance Officer
- Report
- Occupancy Record
- Student Record

# Context Relationships

## Student & Accommodation Management ↔ Billing & Payments

Accommodation information is shared with the billing context so that hostel fees can be generated and payment status can be associated with room bookings.

## Student & Accommodation Management ↔ Maintenance Management

Student and room information is used when maintenance requests are submitted and assigned.

## Student & Accommodation Management ↔ Security & Visitor Management

Resident information is used to identify students and associate visitors with the appropriate residents.

## Student & Accommodation Management ↔ Communication & Notifications

Booking, room allocation, check-in, and check-out events can trigger notifications to students.

## Billing & Payments ↔ Communication & Notifications

Payment confirmations, outstanding balances, and payment reminders can generate notifications.

## Maintenance Management ↔ Communication & Notifications

Maintenance request updates can generate notifications for students and administrators.

## Hostel Administration & Reporting ↔ All Contexts

Administrative reporting uses accommodation, payment, maintenance, and security information to support hostel management and decision-making.
