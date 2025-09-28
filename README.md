# Lab 1 - Basic Authentication

This repository is part of **LAB 6 - Security in NodeJS**.  
It demonstrates **Basic Authentication** using hardcoded credentials.

---

## How to Run
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the server:
   ```bash
   node basic_auth.js
   ```
3. Server will run at:
   ```
   http://localhost:3000
   ```

---

## Routes
- `GET /` → Public route  
- `GET /public` → Public route  
- `GET /secure` → Protected route (requires Basic Auth)

---

## Default Credentials
- Username: `admin`  
- Password: `12345`

---

## Test with Postman
1. Public:
   - GET `http://localhost:3000/`  
   - GET `http://localhost:3000/public`
2. Secure:
   - GET `http://localhost:3000/secure`  
   - In Postman → tab **Authorization** → Basic Auth → enter username/password.

---
