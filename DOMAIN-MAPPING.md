# Domain Mapping - Student Hostel Management System

## 1. Student & Accommodation Management

### Responsibility
Manages students, hostels, rooms, beds, bookings, allocations, check-ins, and check-outs.

### Entities
- Student
- Student Account
- Hostel
- Room
- Bed
- Booking
- Room Allocation
- Check-In
- Check-Out

### Relationships
- A Student can make multiple Bookings.
- A Hostel contains multiple Rooms.
- A Room contains one or more Beds.
- A Booking is associated with a Student and a Room.
- A Room Allocation assigns a Student to a Room.
- A Student can have a Check-In and Check-Out record.

---

## 2. Billing & Payments

### Responsibility
Manages hostel fees, invoices, payments, receipts, balances, and refunds.

### Entities
- Hostel Fee
- Invoice
- Payment
- Payment Receipt
- Outstanding Balance
- Refund

### Relationships
- A Student can have multiple Payments.
- An Invoice represents an amount owed by a Student.
- A Payment is linked to an Invoice.
- A successful Payment generates a Payment Receipt.
- An unpaid Invoice creates an Outstanding Balance.

---

## 3. Maintenance Management

### Responsibility
Manages maintenance complaints, work orders, repairs, assignments, and maintenance status.

### Entities
- Maintenance Request
- Maintenance Staff
- Work Order
- Repair
- Maintenance Status

### Relationships
- A Student can submit multiple Maintenance Requests.
- A Maintenance Request is associated with a Room.
- A Maintenance Request can create a Work Order.
- A Work Order can be assigned to Maintenance Staff.
- A Maintenance Request has a Maintenance Status.

---

## 4. Security & Visitor Management

### Responsibility
Manages visitors, visitor passes, entry and exit records, and security incidents.

### Entities
- Visitor
- Visitor Pass
- Security Officer
- Entry Record
- Exit Record
- Incident Report

### Relationships
- A Student can register multiple Visitors.
- A Visitor can have a Visitor Pass.
- A Security Officer verifies visitors.
- Entry and Exit Records track visitor movements.
- Security incidents can generate Incident Reports.

---

## 5. Communication & Notifications

### Responsibility
Manages announcements, complaints, messages, and system notifications.

### Entities
- Notification
- Announcement
- Message
- Complaint
- Complaint Status

### Relationships
- A Student can receive multiple Notifications.
- An Administrator can create Announcements.
- A Student can submit Complaints.
- A Complaint has a Complaint Status.
- System events can generate Notifications.

---

## 6. Hostel Administration & Reporting

### Responsibility
Provides administrative management, monitoring, reporting, and oversight.

### Entities
- Hostel Administrator
- Accommodation Officer
- Finance Officer
- Report
- Occupancy Record
- Student Record

### Relationships
- Administrators manage hostel records.
- Accommodation Officers manage room allocations.
- Finance Officers manage payment records.
- Reports use information from different system contexts.
- Occupancy Records are based on room allocation and check-in information.

---

# Cross-Domain Relationships

## Student → Booking → Room → Hostel

A student submits a booking for an available room within a hostel.

## Student → Invoice → Payment

A student's accommodation generates an invoice, which can then be paid.

## Student → Maintenance Request → Room → Maintenance Staff

A student reports a problem affecting their room. The request can then be assigned to maintenance staff.

## Student → Visitor → Security Officer

A student registers a visitor, and security officers verify and record the visitor's entry and exit.

## Student → Complaint → Administrator

A student submits a complaint which can be reviewed and managed by hostel administration.

## System Event → Notification → Student

Important events such as booking approval, payment confirmation, or maintenance updates generate notifications for students.

## All Contexts → Reporting

Accommodation, payment, maintenance, and security information can be used to generate administrative reports.
