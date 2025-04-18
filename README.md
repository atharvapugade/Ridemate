# RideMate
RideMate is a ride-sharing platform inspired by apps like BlaBlaCar, with an added focus on **women's safety** and the option to share **bike rides**. Users can offer and find rides based on their preferences, and the platform supports authentication, booking management, and smart location suggestions using **Mapbox API**.

## Features

- **User Authentication** (Register/Login)
- **Offer a Ride** (Add ride details including women-only option)
- **Find a Ride** (Search by pickup, drop location, date, seats, and gender safety preference)
- **Book a Ride** (Real-time booking with confirmation)
- **MongoDB Atlas** for cloud data storage
- **Mapbox API Integration** for location autocomplete
- **Booking Confirmation Notification** to ride providers
- **Separate Frontend & Backend Folders** for organized development

## Tech Stack

### Frontend
- HTML, CSS, JavaScript
- Global CSS for consistent styling

### Backend
- Node.js & Express.js
- MongoDB Atlas (Cloud DB)
- JWT for secure user authentication
- REST API architecture

## Project Structure

```
RideMate/
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── validators/
│   ├── middleware/
│   └── server.js
│
├── frontend/
│   ├── index.html
│   ├── offer-ride.html
│   ├── find-ride.html
│   ├── available-rides.html
│   ├── no-rides.html
│   └── css/
│       └── styles.css
```

## How to Run Locally

### Backend Setup

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/ridemate.git
   cd ridemate/backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file and add:
   ```
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   ```

4. Start the server:
   ```bash
   node server.js
   ```

### Frontend Setup

1. Navigate to the `frontend` folder:
   ```bash
   cd ../frontend
   ```

2. Open `index.html` in your browser or run a live server.

## Notes

- "Women Only" rides can only be offered by verified female users (DigiLocker Aadhaar integration in progress).
- Rides and bookings are stored and fetched from MongoDB Atlas.
- Separate routes and controllers ensure maintainability.

## Contributions

Feel free to fork and contribute! Raise issues or suggestions to improve RideMate.

---
