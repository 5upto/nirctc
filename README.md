# NIRCTC Railway Reservation System

## Overview

NIRCTC is a mini-mock railway reservation system, as part of an Object-Oriented System Design project. This project aims at demonstrating the simplified functionality of a railway reservation system.

## Table of Contents

- [Functional Requirements](#functional-requirements)
- [Non-Functional Requirements](#non-functional-requirements)
- [System Architecture](#system-architecture)
- [Setup Instructions](#setup-instructions)
- [Technologies Used](#technologies-used)
- [Database Structure](#database-structure)
- [Live Demo](#live-demo)
- [How It Works](#how-it-works)
  - [User Registration and Authentication](#user-registration-and-authentication)
  - [Ticket Booking](#ticket-booking)
  - [Ticket Cancellation](#ticket-cancellation)
- [Conclusion](#conclusion)

## Functional Requirements

1. **User Registration and Authentication:**

   - Users can register with a valid username and password.
   - Authentication is required for accessing the system.

2. **Ticket Booking:**

   - Users can search for available trains based on source, destination, and date.
   - The system displays a list of available trains matching the search criteria.

3. **Ticket Cancellation:**
   - Users can cancel their booked tickets based on the PNR number.

## Non-Functional Requirements

1. **Performance Requirements:**

   - Responses to user requests should be within a reasonable amount of time.

2. **Reliability Requirements:**

   - The system must be highly reliable, avoiding crashes or data loss.
   - High availability is crucial, ensuring continuous operation for extended periods.

3. **Security Requirements:**

   - User data must be protected from unauthorized access, modification, or disclosure.

4. **Usability Requirements:**

   - The system has an intuitive and user-friendly interface suitable for users of all technical backgrounds.
   - Clear instructions and prompts guide users through various tasks.

5. **Maintainability Requirements:**

   - The system is well-structured and documented for easy understanding and modification.
   - Adherence to standard coding practices and modular design principles.

## System Architecture

NIRCTC utilizes a server-client architecture. The entire project is implemented in Python, leveraging the customtkinter framework for handling client-side logic. SQLite3 is used as the database for storing user information, train schedules, and bookings.

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/5upto/nirctc
   ```

2. Navigate to the project directory:

   ```bash
   cd nirctc
   ```

3. Create a virtual environment and activate it.

   ```bash
   python -m venv <your-environment-name>
   <your-environment-name>\Scripts\activate
   ```

4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Run the application:
   ```bash
   python .
   ```

## Technologies Used

- **Backend:** Python 3.12
- **Database:** SQLite3
- **GUI Library:** Tkinter, customtkinter
- **Other Libraries:** tkcalendar, time, os

## Database Structure

The SQLite3 database includes tables for storing user information, list of trains, and bookings.

```
Database: NIRCTC

Table: User
    username TEXT
    password TEXT

Table: Booking
    pnr_no TEXT PRIMARY KEY
    user_name TEXT
    full_name TEXT
    age INT
    date_of_journey DATE
    Class TEXT
    from_station TEXT
    to_station TEXT

Table: Train
    name TEXT
    from_station TEXT
    to_station TEXT
    no_of_seats INT
```

## Live Demo

https://github.com/5upto/nirctc/assets/84736189/7ccc49b1-489c-413b-8efd-88230e360167

## How It Works

### User Registration and Authentication

Users can register with a username and password. Authentication is required to access the system, ensuring secure user interactions.

### Ticket Booking

Users can search for available trains based on source, destination, and date.

### Ticket Cancellation

Users can cancel their booked tickets with appropriate confirmation, providing a seamless cancellation process.

## Conclusion

The NIRCTC is a simple user-centric application designed with a focus on performance, security, and scalability. This mini project was an insightful dive into how the architecture of a reservation system works as well as how many of the real-world projects follow a similar architecture to perform the specified tasks.

Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/5upto/).
