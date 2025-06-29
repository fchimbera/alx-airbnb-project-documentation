# Airbnb System Backend Feature Documentation

This README.md file documents the technical and functional requirements for three core backend features of the Airbnb system based on the use case diagram. It includes API endpoints, input/output specs, validation rules, and performance criteria.

###📌 Features Covered

**User Authentication**

**Property Management**

**Booking System**

## 🔐 1. User Authentication

### 📝 Description

Handles account creation, login, and authentication of users (guests, hosts, and admins).

### 📡 API Endpoints

POST /api/register — Register a new user

POST /api/login — Log in an existing user

GET /api/logout — Log out a user (token/session-based)

GET /api/user — Get authenticated user details

### 📥 Input / 📤 Output

POST /api/register

Input:
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "strongpassword123"
}

Output (201 Created):
{
  "message": "User registered successfully",
  "user_id": "1234abcd"
}

POST /api/login

Input:
{
  "email": "john@example.com",
  "password": "strongpassword123"
}

Output (200 OK):
{
  "token": "jwt_token_here",
  "user": {
    "username": "john_doe",
    "role": "guest"
  }
}

### ✅ Validation Rules

Email must be valid and unique

Password must be at least 8 characters long

### ⚙️ Performance Criteria

Token expires after 15 minutes of inactivity

Authentication response time: < 500ms

## 🏠 2. Property Management

### 📝 Description

Allows hosts to list, update, and manage properties available for booking.

### 📡 API Endpoints

POST /api/properties — List a new property

GET /api/properties — Get all properties (with filters)

GET /api/properties/{id} — Get property by ID

PUT /api/properties/{id} — Update a property

DELETE /api/properties/{id} — Delete a property

### 📥 Input / 📤 Output

POST /api/properties

Input:
{
  "title": "Modern Apartment in City Center",
  "description": "2 bedroom apartment with Wi-Fi and AC",
  "price_per_night": 50,
  "location": "Harare, Zimbabwe",
  "amenities": ["WiFi", "AC"]
}

Output (201 Created):
{
  "message": "Property listed successfully",
  "property_id": "5678efgh"
}

### ✅ Validation Rules

Title: 5–100 characters

Price: Must be a positive number

Location: Required

### ⚙️ Performance Criteria

Scales up to 10,000 properties

Search and filter response time: < 800ms

## 📆 3. Booking System

### 📝 Description

Facilitates the process of booking a property and making payments through an external payment gateway.

### 📡 API Endpoints

POST /api/bookings — Make a booking

GET /api/bookings — List user bookings

GET /api/bookings/{id} — Get booking details

DELETE /api/bookings/{id} — Cancel a booking

### 📥 Input / 📤 Output

POST /api/bookings

Input:
{
  "property_id": "5678efgh",
  "start_date": "2025-07-15",
  "end_date": "2025-07-20",
  "guests": 2,
  "payment_method": "card"
}

Output (201 Created):
{
  "message": "Booking confirmed",
  "booking_id": "abcd1234",
  "payment_status": "pending"
}

### ✅ Validation Rules

No overlapping bookings allowed

start_date must be in the future

guests must be a positive integer

### ⚙️ Performance Criteria

Booking confirmation within 1 second

Supports transaction-safe operations to avoid double bookings

## 📌 Notes

All endpoints require user authentication, except registration/login.

Admin-specific actions (e.g., manage users, moderate listings) follow a similar pattern with role-based access control (RBAC).SSS