# Airline Reservation 2

## Overview

This **Airline Reservation System** is a Visual C# application designed to manage a simple airline reservation process. It utilizes a SQLite database to store and manage flight records, customer information, and flight purchases. The application features multiple Windows Forms to search for flights, process purchases, and display receipts with detailed order information and total costs, including taxes.

## Features

- **Flight Management**: View and search for available flights, including details such as departure/destination cities, dates/times, pricing, and seat availability.
- **Customer Management**: Manage customer information including name, telephone, and address.
- **Reservation Processing**: Make flight purchases, update seat availability, and record transactions.
- **Receipt Generation**: Generate detailed receipts that include customer information, flight details, and total cost with taxes.
- **Robust Error Handling**: Implements exception handling to prevent runtime errors and ensure smooth user experience.
- **Database Integration**: Utilizes SQLite for efficient data storage and retrieval, ensuring data consistency and integrity.

## Components

### 1. **SQLite Database**

The application uses a SQLite database with the following tables:

- **Flight Records**:
  - `FlightID`: Unique identifier for each flight.
  - `DepartureCity`: City of departure.
  - `DestinationCity`: Destination city.
  - `DepartureDateTime`: Date and time of departure.
  - `ArrivalDateTime`: Date and time of arrival.
  - `Price`: Cost of the flight.
  - `SeatsAvailableFirstClass`: Number of available first-class seats.
  - `SeatsSoldFirstClass`: Number of sold first-class seats.
  - `SeatsAvailableCoach`: Number of available coach seats.
  - `SeatsSoldCoach`: Number of sold coach seats.

- **Customer Information**:
  - `CustomerID`: Unique identifier for each customer.
  - `Name`: Customer's full name.
  - `Telephone`: Customer's telephone number.
  - `Address`: Customer's address.

- **Flight Purchases**:
  - `PurchaseID`: Unique identifier for each purchase.
  - `FlightID`: Associated flight ID.
  - `CustomerID`: Associated customer ID.
  - `PurchaseDate`: Date of purchase.
  - `SeatClass`: Class of seat purchased (First-Class or Coach).
  - `Quantity`: Number of seats purchased.

### 2. **Windows Forms Applications**

- **Search Flights Form**:
  - Allows users to search for flights based on criteria such as departure/destination cities and dates.
  
- **Purchase Flights Form**:
  - Enables users to select flights and make purchases.
  - Updates the database with new purchase records and adjusts seat availability accordingly.
  
- **Receipt Display Form**:
  - Displays detailed receipts for completed purchases, including customer information, flight details, and total cost with taxes.

## Setup Instructions

### Prerequisites

- **Development Environment**:
  - Visual Studio 2019 or later with C# and .NET support.
  
- **Database**:
  - SQLite installed or use the built-in SQLite support within the application.

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/airline-reservation-system.git
   cd airline-reservation-system
