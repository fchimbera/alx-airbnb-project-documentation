# 🏡 Airbnb Clone Backend Features & Functionalities

This directory contains a visual representation of the core backend components required to build the **Airbnb Clone** project. The diagram was created using **Draw.io** and outlines the major modules and features the backend must support.

## 📌 Diagram Overview

The PNG file included here represents the high-level architecture and feature breakdown of the Airbnb Clone backend. It includes:

### 🔐 User Management
- User Registration (Guests and Hosts)
- Login (Email & Password, OAuth)
- JWT-based Authentication
- Profile Management
- Role-Based Access Control (RBAC)

### 🏠 Property Listings
- Create/Edit/Delete Property Listings
- Manage amenities, availability, and pricing
- Upload and store property images

### 🔍 Search & Filtering
- Search by location, price, guest capacity
- Filter by amenities
- Pagination for large result sets

### 📅 Booking Management
- Create bookings with date validation
- Cancel bookings
- Manage booking statuses (Pending, Confirmed, Canceled, Completed)

### 💳 Payments
- Guest payments via secure gateways (e.g., Stripe, PayPal)
- Host payouts
- Multi-currency support

### ⭐ Reviews & Ratings
- Guests leave reviews after bookings
- Star ratings and optional feedback
- Hosts can respond to reviews

### 🔔 Notifications
- Email notifications (SendGrid or Mailgun)
- In-app notifications for booking and payment events

### 🛠️ Admin Dashboard
- Manage users, properties, bookings, reviews, and payments

---

## 📂 Files Included

| File | Description |
|------|-------------|
| `airbnb-backend-features.png` | Draw.io-generated PNG diagram of backend features |
| `README.md` | This documentation file |

---

## 🧰 How to Edit or Extend the Diagram

To edit or enhance the diagram:

1. Go to [https://draw.io](https://draw.io)
2. Import the `.drawio` or `.xml` source file (if available)
3. Edit the diagram and re-export as PNG if needed