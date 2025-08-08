# RideMate – Smart Ride Sharing Platform

**RideMate** is a ride-sharing web application inspired by platforms like BlaBlaCar, with a strong focus on **women’s safety** and the option to share **bike rides**. It allows users to offer or find rides based on preferences like location, date, seat availability, and gender safety.

This full-stack platform is built with the **MERN** stack and integrates **Mapbox API** for smart location suggestions, along with **DigiLocker** for gender verification and **Nodemailer** for real-time booking notifications.

---

## Features

- User Authentication (Register/Login with JWT)
- Offer a Ride (Pickup, Drop, Date, Seats, and "Women Only" option)
- Find a Ride (Search by location, date, seat count, and women-safety preference)
- Book a Ride (Real-time booking with confirmation)
- Mapbox API Integration for city/location autocomplete
- Aadhaar-based gender verification via DigiLocker API
- Email Notifications using Nodemailer to inform ride providers with booking details
- MongoDB Atlas for cloud-based data storage
- RESTful API architecture with modular structure

---

## Tech Stack

### Frontend

- HTML, CSS, JavaScript
- Global CSS for consistent styling

### Backend

- Node.js, Express.js
- MongoDB Atlas (Cloud Database)
- JWT for secure user authentication
- Nodemailer for sending booking emails
- DigiLocker API for Aadhaar-based gender verification

---

## Project Structure
```bash
RideMate/
├── backend/
│   ├── controllers/          # Handles business logic
│   ├── models/               # Mongoose models
│   ├── routes/               # API routes
│   ├── validators/           # Input validators
│   ├── middleware/           # JWT auth middleware, etc.
│   ├── utils/                # DigiLocker & Nodemailer helpers
│   └── server.js             # Main backend entry point
│
├── frontend/
│   ├── index.html            # Home page
│   ├── offer-ride.html       # Offer a ride page
│   ├── find-ride.html        # Find a ride page
│   ├── available-rides.html  # Show matching rides
│   ├── no-rides.html         # No rides found page
│   └── css/
│       └── styles.css        # Global styling
```

## How to Run Locally

### Backend Setup

1. Clone the repository:

```bash
git clone https://github.com/your-username/ridemate.git
cd ridemate/backend
Install backend dependencies:

npm install
Create a .env file and add the following:

init
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_app_password

Start the backend server:
node server.js

Frontend Setup:
Navigate to the frontend directory:
cd ../frontend
Open index.html in your browser directly or use a live server extension for a better experience.

Gender Verification (DigiLocker Integration):
Only verified female users can offer "Women Only" rides.
Gender verification is handled via DigiLocker Aadhaar authentication.
This ensures trust and safety for female passengers and ride providers.

Booking Confirmation (Email Notification):
After successful booking, the ride provider receives an automated email containing the passenger’s:
Name
Contact details
Ride information
Emails are sent using Nodemailer with the credentials provided in the .env file.

Contribution:
Contributions are welcome.
Fork the repository
Create a new branch
Commit your changes
Open a pull request
For major changes, please open an issue first to discuss what you'd like to change.


Inspired by BlaBlaCar
Developed by Atharv Apugade
