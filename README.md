# Appointment Scheduling System

The **Appointment Scheduling System** enables customers to book, reschedule, and cancel appointments with doctors. It ensures data integrity through relational constraints and Python logic, providing a structured workflow for managing appointments.

## Features

- **Customer Management**: Register and manage customer details.
- **Doctor Management**: Maintain doctor records with specialization and availability.
- **Appointment Booking**: Schedule, reschedule, and cancel appointments.
- **Data Integrity**: Triggers prevent double booking, and constraints ensure valid references.
- **Statistical Reporting**: Plan for future integration of reports on appointments and cancellations.

## Database Schema

The system uses a relational database with the following tables:

### Customers Table

Stores customer details:
- **id** (Primary Key)
- **name** (Customer name)
- **email** (Customer email)
- **phone** (Customer phone number)

### Doctors Table

Stores doctor details:
- **id** (Primary Key)
- **name** (Doctor name)
- **specialization** (Doctor specialization)
- **availability** (Availability for appointments, e.g., "9:00 AM - 5:00 PM")

### Appointments Table

Tracks appointments with customers and doctors:
- **id** (Primary Key)
- **customer_id** (Foreign Key: Customer)
- **doctor_id** (Foreign Key: Doctor)
- **appointment_date** (Appointment date)
- **appointment_time** (Appointment time)
- **status** (Appointment status, e.g., "Scheduled", "Canceled")

## Setup and Usage

### 1. Prerequisites

Before running the application, make sure you have the following installed:
- **Python 3.x**
- **Flask**
- **Flask-SQLAlchemy**
- **SQLite** (or another database if preferred)

### 2. Install Dependencies

Create a virtual environment and install the required Python packages using the following commands:

```bash
# Create a virtual environment (optional)
python -m venv venv

# Activate the virtual environment
# For Windows:
venv\Scripts\activate
# For macOS/Linux:
source venv/bin/activate

# Install required dependencies
pip install Flask Flask-SQLAlchemy
