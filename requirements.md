# Airbnb Clone – Backend Requirements Specification

This document outlines the technical and functional requirements for key backend features of the Airbnb Clone system.

---

## 1. User Authentication System

### 🔹 Feature Overview
Handles user registration, login, and session management using JWT authentication. Supports both Guests and Hosts.

### 🔹 API Endpoints
| Method | Endpoint | Description |
|--------|-----------|-------------|
| POST | `/api/v1/auth/register` | Register a new user (guest or host) |
| POST | `/api/v1/auth/login` | Authenticate user and return JWT token |
| GET | `/api/v1/auth/profile` | Retrieve logged-in user profile (protected) |
| PUT | `/api/v1/auth/profile` | Update user profile information |

### 🔹 Input / Output Specification
**Register Input:**
```json
{
  "name": "Rekik Tamrat",
  "email": "rekik@example.com",
  "password": "Password123",
  "role": "host"
}



{
  "message": "User registered successfully",
  "userId": "u123",
  "token": "jwt_token_here"
}



{
  "title": "Modern Apartment in Addis Ababa",
  "description": "Cozy 2-bedroom apartment near city center",
  "price": 80,
  "location": "Addis Ababa, Ethiopia",
  "amenities": ["Wi-Fi", "Kitchen", "Washer"]
}


{
  "message": "Property created successfully",
  "propertyId": "p101"
}


{
  "userId": "u123",
  "propertyId": "p101",
  "checkIn": "2025-11-01",
  "checkOut": "2025-11-05",
  "paymentMethod": "stripe"
}


{
  "message": "Booking confirmed",
  "bookingId": "b456",
  "status": "confirmed"
}
