# IRCTC Railway Management System

## Features
- Secure JWT authentication
- Train availability & seat booking
- Admin controls: add trains, update seats
- Role-based access (user/admin)

## Setup
### Prerequisites
- Install [Node.js](https://nodejs.org/) (v14+)
- Install [MySQL](https://www.mysql.com/)
- Install [Postman](https://www.postman.com/) for testing

### Installation
1. Clone the repo & install dependencies:
   ```bash
   git clone https://github.com/ujjawalkumar131/IRCTC_API_WorkIndia.git
   cd irctc-railway-management
   npm install
   ```
2. Set up MySQL database:
   ```sql
   CREATE DATABASE irctc_db;
   USE irctc_db;
   ```
3. Configure `.env` file:
   ```bash
   PORT=3000
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=yourpassword
   DB_NAME=irctc_db
   JWT_SECRET=your_jwt_secret
   API_KEY=your_admin_api_key
   ```
4. Start the server:
   ```bash
   npm start
   ```
   API runs at `http://localhost:3000`

## API Endpoints
### User
- **Register:** `POST /user/register`
- **Login:** `POST /user/login`
- **Check Trains:** `GET /user/availability?source=Ranchi&destination=Delhi`
- **Book Seats:** `POST /user/book`
- **View Bookings:** `GET /user/getAllbookings`

### Admin
- **Add Train:** `POST /admin/addTrain` (Requires API Key)
- **Update Seats:** `PUT /admin/update-seats/:id` (Requires API Key)

## Testing
Use Postman to test API endpoints.

## Tech Stack
- **Node.js & Express.js**: Backend
- **MySQL**: Database
- **JWT & bcrypt**: Security
- **dotenv**: Config management

