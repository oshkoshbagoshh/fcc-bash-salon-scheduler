# Salon Appointment Scheduler

This project is a simple bash script that interacts with a PostgreSQL database to manage salon appointments. It allows users to select a service, enter their phone number, and schedule an appointment.

## Features

- Display a list of available services
- Prompt users to select a service
- Check if the user is an existing customer by phone number
- Add new customers to the database
- Schedule appointments for customers

## Database Schema

The database consists of three tables:

1. **customers**
   - `customer_id` (SERIAL PRIMARY KEY)
   - `name` (VARCHAR NOT NULL)
   - `phone` (VARCHAR UNIQUE NOT NULL)

2. **services**
   - `service_id` (SERIAL PRIMARY KEY)
   - `name` (VARCHAR NOT NULL)

3. **appointments**
   - `appointment_id` (SERIAL PRIMARY KEY)
   - `customer_id` (INT REFERENCES customers(customer_id))
   - `service_id` (INT REFERENCES services(service_id))
   - `time` (VARCHAR NOT NULL)



