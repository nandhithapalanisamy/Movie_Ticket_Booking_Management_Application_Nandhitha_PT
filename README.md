# Movie Ticket Booking Management Application

## Project Overview

The Movie Ticket Booking Management Application is a Pega-based application designed to manage the complete movie ticket booking process. It allows customers to submit movie ticket requests, check show availability, review booking details, confirm or cancel bookings, and complete the ticket booking process.

The application uses Pega Case Management, Data Objects, Data Transforms, conditional routing, SLA configuration, and correspondence to manage the booking lifecycle.

---

## Application Details

- **Project:** Movie Ticket Booking
- **Application Name:** Movie_Ticket_Booking_Management_Application_Nandhitha_PT
- **Case Type:** Ticketing Management
- **Operator:** Nandhitha_PT
- **Platform:** Pega Platform

---

## Case Lifecycle

The case follows these stages in order:

1. Request Details
2. Availability
3. Approval
4. Booking Execution

---

## Application Workflow

### 1. Request Details

The customer submits the movie ticket request by providing:

- Movie Name
- Show Date
- Show Time
- Number of Tickets

The required information is validated before the request proceeds.

### 2. Availability

The application checks whether the requested show has sufficient seats available.

The following information is maintained:

- Seat Availability Status
- Available Seats Count

The booking proceeds only when sufficient seats are available.

### 3. Approval

The customer reviews the booking details before confirmation.

The customer can select:

- Confirmed
- Cancelled

If the booking is confirmed, the case proceeds to Booking Execution. If it is cancelled, the booking is stopped appropriately.

### 4. Booking Execution

The application processes the confirmed booking and maintains:

- Seat Numbers
- Ticket ID
- Booking Confirmation Status
- Booking Status

The booking is then routed according to the Show Type and a confirmation notification is sent to the customer.

---

## Data Objects

The application uses reusable Movie and Show data objects to maintain movie and show-related information.

### Movie

Properties include:

- Movie Name
- Genre

### Show

Properties include:

- Movie Name
- Show Date
- Show Time
- Show Type
- Seat Capacity
- Ticket Price

These reusable data objects support consistency across multiple movie ticket booking requests.

---

## Booking Cost Calculation

The application automatically calculates the total booking cost.

### Formula

```text
Total Cost = Ticket Price × Number of Tickets
