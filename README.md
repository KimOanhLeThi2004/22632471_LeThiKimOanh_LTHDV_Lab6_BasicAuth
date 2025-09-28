# Lab 1 - Basic Authentication & Cookie Authentication

This repository is part of LAB 6 - Security in NodeJS. It demonstrates two parts: (a) Basic Authentication using hardcoded credentials and (b) Cookie Authentication with MongoDB to store and validate cookie tokens.

## How to Run

### (a) BasicAuth
Install dependencies with `npm install`. Run the server using `node basic_auth.js`. The server will start at `http://localhost:3000`.

### (b) CookieAuth
Install dependencies with `npm install`. Run the server using `node cookie_auth.js`. The server will start at `http://localhost:3001`.

## Routes

### (a) BasicAuth
Available routes are:
- `GET /` → public route
- `GET /public` → public route
- `GET /secure` → protected route requiring Basic Auth

Default credentials are:
- Username: `admin`
- Password: `12345`

### (b) CookieAuth
Available routes are:
- `POST /login` → login with username and password, set cookie `auth_cookie_token`, and save it in MongoDB
- `GET /profile` → protected route, requires valid cookie
- `POST /logout` → logout, delete cookie from DB and client

## Testing with Postman

### (a) BasicAuth
1. Test `GET http://localhost:3000/` and `GET http://localhost:3000/public` → both return success without authentication.  
2. Test `GET http://localhost:3000/secure` → requires Basic Auth. In Postman, go to Authorization tab, select Basic Auth, enter username `admin` and password `12345`.

### (b) CookieAuth
1. Login with `POST http://localhost:3001/login`, body JSON:
```json
{ "username": "admin", "password": "12345" }
