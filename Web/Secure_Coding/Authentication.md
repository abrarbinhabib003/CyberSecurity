
# 🔐 Authentication Techniques - Explained in Detail

### 🚀 Why Authentication Matters  
In today’s digital world, protecting **user accounts** is crucial. Without proper authentication, sensitive data can be accessed by malicious actors. From secure **passwords** to advanced methods like **OAuth** and **OpenID Connect**, every layer of security helps.

---

## 1️⃣ Strong Password Policies 🔑

### 📌 What It Is:
A **Password Policy** is a set of rules that ensures users create strong, hard-to-guess passwords.

### 📋 Common Rules:
- Minimum 12 characters
- Mix of uppercase 🔠 and lowercase 🔡
- Include numbers 🔢 and special characters (!@#$%)
- Change passwords every 90 days 🗓️

### 🔍 Real-life Example:
At a university portal, students are required to set passwords with at least one capital letter, one number, and one special character, and change them every semester.

### ✅ Benefits:
- First line of defense against attacks like brute-force
- Protects against easy-to-guess or reused passwords

---

## 2️⃣ Multi-Factor Authentication (MFA) 🧠📱

### 📌 What It Is:
**MFA** requires users to authenticate using **two or more independent factors**:
1. Something you **know** (password)
2. Something you **have** (phone/code)
3. Something you **are** (fingerprint/face)

### 🔍 Real-life Example:
Logging into your bank app:  
🔐 Enter password → 📲 Enter OTP sent to your phone

### ✅ Benefits:
- Protects even if your password is compromised
- Widely used in banks, Gmail, GitHub, etc.

---

## 3️⃣ OAuth (Open Authorization) 🌐🔗

### 📌 What It Is:
OAuth allows you to log into apps using **third-party accounts** (like Google, Facebook, Microsoft), without creating a new password.

### 🔍 Real-life Example:
Signing up for a fitness app → Click "Log in with Google" → You’re in! 🏋️‍♂️

### ✅ Benefits:
- Reduces the number of passwords to remember
- Prevents weak/reused passwords
- Users stay within secure ecosystems (Google, Microsoft)

---

## 4️⃣ OpenID Connect (OIDC) 🛡️🧾

### 📌 What It Is:
An identity layer **on top of OAuth**.  
Not only authorizes you but also **verifies your identity** using an ID token.

### 🔍 Real-life Example:
You log in using your Microsoft account → App receives a signed token with your name/email → App confirms: Yes, it’s you!

### ✅ Benefits:
- Prevents impersonation
- Secure identity verification without extra user steps
- Common in enterprise apps and SSO (Single Sign-On) systems

---

## 🧠 Interview Questions & Answers

### ❓ Q1: What are the essential components of a strong password policy?
**✅ A:** Minimum 12 characters, a mix of upper/lowercase, numbers, special characters, and periodic updates.

### ❓ Q2: Why is MFA more secure than just passwords?
**✅ A:** MFA adds additional independent layers of verification, making it difficult for attackers to breach even if one layer (like a password) is compromised.

### ❓ Q3: What is OAuth used for?
**✅ A:** OAuth allows third-party apps to authorize users securely via accounts from providers like Google, without handling their passwords directly.

### ❓ Q4: How is OpenID Connect different from OAuth?
**✅ A:** OAuth handles authorization only, whereas OpenID Connect adds authentication by verifying identity using ID tokens.

---

## 🧩 Summary Table

| Technique           | Focus            | Key Feature                                | Example Use-Case                        |
|---------------------|------------------|---------------------------------------------|------------------------------------------|
| Password Policy     | User-side entry  | Enforce strong, complex passwords           | Email sign-up                            |
| Multi-Factor Auth   | Extra security   | Combines multiple factors (e.g. code + pwd) | Bank login                               |
| OAuth               | Convenience      | Use existing accounts (Google, FB, etc.)    | Fitness app login                        |
| OpenID Connect      | Identity proof   | Verifies who the user is                   | Corporate SSO systems, secure platforms  |

---

## 🏁 Final Thoughts  
Authentication is not just a tech requirement — it’s a **trust-building bridge** between your app and its users. By applying a layered approach—**strong passwords**, **MFA**, **OAuth**, and **OpenID Connect**—you **enhance security** without sacrificing user experience. 🌟



# 🔑 Authentication Techniques: **Passkeys**

---

### 🧠 What Are Passkeys?

**Passkeys** are a **modern, passwordless authentication method** designed to be:
- **More secure** than traditional passwords 🔒
- **Easier to use** for end users 😌
- **Phishing-resistant** 🛡️

They replace passwords with **cryptographic key pairs** — a **public key** stored on the website and a **private key** stored securely on your device.

---

### 🔍 How Do Passkeys Work?

Think of passkeys as a **digital key** 🗝️ stored on your phone or computer.

Here's the simplified breakdown:

1. ✅ **User tries to log in** to an app or website.
2. 📲 **The website asks your device** to verify your identity using a passkey.
3. 👆 You use **biometrics (Face ID, fingerprint)** or your **device PIN** to approve.
4. 🔐 Your **private key** (on your device) signs a challenge.
5. ☁️ The app verifies this signature with the **public key** it has stored.

> ✅ You’re logged in — *without typing a password!*

---

### 🔄 Passkeys vs Passwords

| Feature               | Passwords                       | Passkeys                                |
|----------------------|----------------------------------|------------------------------------------|
| 🔐 Security           | Can be reused, weak, or stolen   | Strong cryptographic-based authentication |
| 🛡️ Phishing-Proof     | ❌ Susceptible to phishing        | ✅ Resistant to phishing attacks          |
| 🔁 Reuse Risk         | High (users repeat passwords)    | No reuse — unique key pairs              |
| 🧠 Memorization       | Requires remembering             | No need to remember anything             |
| 🔄 Device Sync        | Manual with passwords            | Auto-sync via cloud (iCloud, Google etc.)|

---

### 🔄 Syncing Passkeys Across Devices

- Platforms like **Apple iCloud**, **Google Account**, or **Windows Hello** allow syncing passkeys across all your devices.
- Lose your phone? 😱 No problem — as long as you have backup and sync enabled, you can recover your passkeys.

---

### 🧪 Real-Life Example

Imagine you’re logging into your **online banking app**:

**Before (Old Way)**  
🔑 Enter password → 😰 Hope it’s strong → 🙄 Wait for OTP → Login.

**Now (Passkey Way)**  
👆 Tap "Login with Face ID" → 😎 You're in securely — in *seconds*.

---

### 💡 Benefits of Passkeys

✅ **Stronger security** than passwords  
✅ **No phishing** risk  
✅ **Faster login experience**  
✅ **No password resets needed**  
✅ **Reduces IT overhead** for password management

---

### 🚫 Challenges or Considerations

⚠️ **User adoption** — people are still used to passwords  
⚠️ **Device compatibility** — older systems may not support passkeys  
⚠️ **Account recovery** — needs to be planned well in case of lost device  

> 🔧 Developers need to implement **WebAuthn** and **FIDO2 standards** to support passkeys.

---

### 📢 Interview Questions

1. **Q:** What is a passkey in authentication?  
   **A:** A passkey is a cryptographic login credential that replaces passwords, combining public-private key encryption with biometric/device-based verification.

2. **Q:** Why are passkeys considered more secure than passwords?  
   **A:** Because they are phishing-resistant, cannot be reused, and are device-bound, eliminating many common vulnerabilities of passwords.

3. **Q:** What tech standards support passkeys?  
   **A:** **WebAuthn** and **FIDO2**, both developed by the **FIDO Alliance**.

4. **Q:** Can passkeys be used on multiple devices?  
   **A:** Yes, if supported by a cloud sync service like **iCloud Keychain** or **Google Password Manager**.

---

### 🔐 Final Thoughts

Passkeys represent the **future of authentication**.  
They deliver the **security of biometrics + cryptography** and the **simplicity of one-touch login**, making them a game changer in the fight against cyber threats.

---

📝 **Pro Tip for Developers:**  
Start exploring **WebAuthn APIs** and integrating **passkey login** into your apps to stay ahead in the authentication game.

---

# 🔐 Authorization Techniques – Implementing RBAC (Role-Based Access Control)

### 🎯 Key Concepts:
- **RBAC (Role-Based Access Control):** Security model to restrict resource access based on user roles (e.g., `admin`, `user`).
- **JWT (JSON Web Token):** Securely stores and transmits user data (like roles) in the payload for verification.
- **Authorization Policies:** Define which role can access what—`adminOnly`, `userOnly`.
- **Middleware:** Acts as a checkpoint before reaching route handlers to validate JWTs and roles.
- **Testing RBAC:** Use Postman to simulate requests with JWTs and verify access control.

---

### ⚙️ Workflow Summary:
1. **Define roles** (admin, user).
2. **Store role in user object** (e.g., `{ username, passwordHash, role }`).
3. **Include role in JWT payload**.
4. **Use middleware** to verify token and enforce policies.
5. **Assign policies to routes** (e.g., `adminOnly` for `/admin-panel` route).
6. **Test using Postman** by sending valid/invalid JWTs.

---

### 💡 Real-Life Example:
> A hospital management app gives different dashboard access:
> - **Doctors** can access patient history and prescriptions.
> - **Admins** can manage users and records.
> - **Patients** can only view their own info.

Using RBAC, you can ensure each role sees **only** what they should.

---

## 🧠 Interview Questions & Answers

### ✅ General Questions:

**Q1: What is RBAC, and why is it important?**  
🅰️ RBAC (Role-Based Access Control) is a method of regulating user access based on roles. It improves security by giving users only the permissions necessary for their role, reducing risks of misuse.

**Q2: How does middleware help in RBAC implementation?**  
🅰️ Middleware checks JWTs before requests reach route handlers. It validates tokens, extracts roles, and enforces access policies accordingly.

**Q3: What are some best practices when implementing RBAC?**  
🅰️  
- Use clear role definitions.  
- Store roles securely (e.g., in JWT payload).  
- Apply middleware to protected routes.  
- Regularly audit role access and permissions.

---

### 🔐 Cybersecurity & MERN Stack Focused Questions:

**Q4: How does JWT help in enforcing RBAC in a MERN stack app?**  
🅰️ JWT stores role info in the payload. In a MERN stack app, the backend verifies the token using middleware, checks if the role matches the required one, and grants or denies access accordingly.

**Q5: How would you protect an admin dashboard in your MERN project?**  
🅰️  
- Define a role like `admin` in user schema.  
- Include it in the JWT on login.  
- Create middleware to verify `admin` role.  
- Use it on the `/admin-dashboard` route.

**Q6: What happens if a user without the right role tries to access a restricted route?**  
🅰️ The server responds with a **403 Forbidden** status, indicating that the user lacks permission for that route.

---

Implementing Authentication and Authorization in a Web Application \- Guided Lab Video
======================================================================================

Overview
--------

This guided lab focuses on implementing secure authentication and authorization within a sample Node.js web application. The steps entail setting up user registration and login, implementing multi-factor authentication (MFA), and establishing role-based access control (RBAC).

Contents
--------

1.  **Setting Up Infrastructure**
    *   Libraries and Environment
    *   User and OTP Management
2.  **User Registration and Login**
    *   Registration Endpoint
    *   Login Endpoint
3.  **Multi-Factor Authentication (MFA)**
    *   Sending One-Time Password (OTP)
    *   Verifying OTP
4.  **Role-Based Access Control (RBAC)**
    *   Authorizing Access
    *   Admin12702### Interactive Explanation Note on Implementing Authentication and Authorization in a Web Application

#### Introduction

In this guided lab, we will learn how to implement secure authentication and authorization in a sample Node.js web application. We'll break down the process into manageable steps, covering registration, login, multi-factor authentication, and role-based access control (RBAC).

* * *

#### Step 1: Setting Up User Registration and Login

1.  **Library Imports:**
    
    *   **Express**: Sets up the web server.
    *   **bcrypt.js**: Hashes passwords for security.
    *   **jsonwebtoken (JWT)**: Manages secure tokens.
2.  **Variables Initialization:**
    
    *   Initialize`app`using Express.
    *   Use`express.json()`for parsing JSON request bodies.
    *   Create variables for users (simulated) and OTP (One-Time Password) storage.
3.  **Register Endpoint:**
    
    *   Define a`/register`POST endpoint where a user can send their email and password.
    *   **Password Length Check**: If the password is less than 8 characters, return an error.
    *   **Password Hashing**: Use`bcrypt.hash`to hash the password to ensure it’s stored securely.
    *   Create the user, and respond with a success message.
4.  **Login Endpoint:**
    
    *   Define a`/login`POST endpoint for users to enter their credentials.
    *   Extract email and password from the request body.
    *   Use`bcrypt.compare`to authenticate the user by comparing the provided password with the stored hashed password.
    *   If authentication succeeds, use`jwt.sign`to create a token using the user's email and role.
    *   Respond with the generated token for secure access.

* * *

#### Step 2: Implementing Multi-Factor Authentication (MFA)

1.  **OTP Generation Endpoint:**
    
    *   Define an endpoint`/send-otp`for user requests for a one-time password (OTP).
    *   Use`Math.floor`to create a random six-digit OTP.
    *   Store the OTP indexed by the user’s email in a temporary storage solution.
    *   Log the OTP to the console and send a message to the user that the OTP is generated.
2.  **OTP Verification Endpoint:**
    
    *   Define an endpoint`/verify-otp`where users will submit their OTP.
    *   Compare the submitted OTP with the stored OTP.
    *   If they match, delete the stored OTP and grant access (return success).
    *   If they do not match, indicate that the OTP is invalid.

* * *

#### Step 3: Implementing Role-Based Access Control (RBAC)

1.  **Authorization Function:**
    
    *   Create a middleware function called`Authorize`that checks the user's role.
    *   Check for the presence of a token in the request's authorization header.
    *   If absent, deny access.
    *   If present, use`jwt.verify`to decode the token and validate the role against required permissions.
2.  **Admin Endpoint:**
    
    *   Define a`/admin`GET endpoint for restricted access to admin routes.
    *   Pass the`admin`role to the`Authorize`function.
    *   If authentication checks pass, send a welcome message to the admin; otherwise, respond with a 403 Forbidden status if the user lacks the necessary role.

* * *

#### Summary

This lab session detailed three core steps to implement secure authentication and authorization in a web application using Node.js:

*   **Registering and Logging In Users**: Utilizing email and password protections.
*   **Adding Multi-Factor Authentication**: Enhancing security with temporary OTPs.
*   **Implementing Role-Based Access Control**: Restricting access to sensitive areas based on user roles.

Utilizing these techniques helps secure sensitive information within your application and ensure only authorized users can access certain functionalities.

### Notes

*   Ensure to always handle errors gracefully at every step of the process.
*   In a production environment, consider implementing email functionalities for sending OTPs instead of logging to the console.
*   Regularly update libraries and maintain security practices, especially around authentication and authorization.

---



## 🚀 Lab Part 1: Setting Up Secure AuthApp with Node.js + Express

### 🎯 **Objective**
By the end of this part, you'll have:
- Created a full folder structure for `AuthApp` 🗂️  
- Set up **Node.js projects** for OAuth Server & Web App 🛠️  
- Installed all required packages 📦  
- Configured environment variables for JWT and ports 🔑  
- Verified servers with basic Express setup 🌐  

---

### 📁 Folder & File Structure

Here's what your structure should look like:

```
AuthApp/
│
├── authorization-server/
│   ├── server.js
│   └── .env
│
├── web-app/
│   ├── app.js
│   ├── .env
│   └── views/
│       ├── login.html
│       ├── register.html
│       └── protected.html
```

---

### 🛠️ Step-by-Step Setup

#### 1️⃣ Create Project Folders
Open VS Code ➜ File → Open Folder → Create a folder named `AuthApp` → Open it ✅

#### 2️⃣ Create Subfolders and Files

**Inside `authorization-server`:**
- `server.js`
- `.env`

**Inside `web-app`:**
- `app.js`
- `.env`
- `views/` folder containing:
  - `login.html`
  - `register.html`
  - `protected.html`

#### 3️⃣ Initialize Node Projects
In terminal:

```bash
# Init OAuth server
cd authorization-server
npm init -y

# Init Web App
cd ../web-app
npm init -y
```

#### 4️⃣ Install Dependencies

📌 In `authorization-server`:
```bash
npm install express jsonwebtoken dotenv body-parser cors
```

📌 In `web-app`:
```bash
npm install express bcryptjs jsonwebtoken dotenv body-parser axios cors nodemailer
```

#### 5️⃣ Set Up `.env` Files

📄 `authorization-server/.env`:
```env
PORT=4001
JWT_SECRET=your_secret_key
```

📄 `web-app/.env`:
```env
PORT=5001
JWT_SECRET=your_secret_key
```

---

### ⚙️ 6️⃣ Basic Express Servers

📌 `authorization-server/server.js`:
```js
const express = require("express");
const jwt = require("jsonwebtoken");
require("dotenv").config();

const app = express();
app.use(express.json());

const authCodes = {}; // Store auth codes temporarily

// Example route
app.get("/", (req, res) => {
  res.send("OAuth Server is running");
});

app.listen(process.env.PORT, () =>
  console.log(`OAuth Server running on port ${process.env.PORT}`)
);
```

📌 `web-app/app.js`:
```js
const express = require("express");
require("dotenv").config();

const app = express();
app.use(express.json());
app.use(express.static("views"));

app.get("/", (req, res) => res.sendFile(__dirname + "/views/login.html"));

app.listen(process.env.PORT, () =>
  console.log(`Web App running on port ${process.env.PORT}`)
);
```

---

### 🧪 7️⃣ Run and Test the App

**In one terminal:**
```bash
cd authorization-server
node server.js
```

**In another terminal:**
```bash
cd web-app
node app.js
```

➡️ Visit:  
- [http://localhost:5001](http://localhost:5001) → Login page should show  
- [http://localhost:4001](http://localhost:4001) → OAuth server basic message  

---

### ✅ You’re Ready for Part 2!

Next you'll implement:
- 🔑 **Registration & Login**  
- 🔐 **Password validation**  
- 📱 **Multi-Factor Authentication (MFA)**  
- 🌐 **OAuth Flow Simulation**

---


# 🔐 Secure Authentication Web App with MFA

## ✅ Project Overview

This project demonstrates a **basic user authentication system** using only HTML, JavaScript, and `localStorage`. It includes:

- User **registration**
- **Login** with credential verification
- **In-memory user storage**
- **Multi-Factor Authentication (MFA)** using OTP
- **Protected page** accessible only to authenticated users

---

## 🌐 Part 1: Folder Structure

```
/project-folder
├── register.html
├── login.html
└── protected.html
```

---

## 🧾 Part 2: User Registration Page

### ✅ Goal:
Create a registration page where users can input their email and password. Data is saved in localStorage.

### 🔧 Instructions:

1. Create a file named `register.html`.
2. Add a form to capture `email` and `password`.
3. Use `localStorage.setItem()` to store user data in memory.

### ✅ `register.html` Code + Explanation:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Register</title>
</head>
<body>
  <h2>User Registration</h2>
  <form id="registerForm" onsubmit="registerUser(event)">
    <input type="email" id="email" placeholder="Email" required><br><br>
    <input type="password" id="password" placeholder="Password" required><br><br>
    <button type="submit">Register</button>
  </form>

  <script>
    function registerUser(event) {
      event.preventDefault();
      const email = document.getElementById("email").value;
      const password = document.getElementById("password").value;

      let users = JSON.parse(localStorage.getItem("users")) || [];

      const existingUser = users.find(user => user.email === email);
      if (existingUser) {
        alert("User already exists!");
        return;
      }

      users.push({ email, password });
      localStorage.setItem("users", JSON.stringify(users));
      alert("Registration successful!");
      window.location.href = "login.html";
    }
  </script>
</body>
</html>
```

#### 📌 Explanation:
- Checks if a user already exists using `.find()`.
- Adds new user to the list.
- Saves user list using `localStorage.setItem("users", JSON.stringify(users))`.

---

## 🔐 Part 3: Login Page with Credential Check

### ✅ Goal:
Create a login page that verifies if a registered user exists. If valid, move on to OTP verification.

### 🔧 Instructions:

1. Create `login.html`.
2. Add a form to input `email` and `password`.
3. Match the user with stored data from localStorage.
4. Show OTP entry if credentials match.

### ✅ `login.html` Code + Explanation:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Login</title>
</head>
<body>
  <h2>User Login</h2>
  <form id="loginForm" onsubmit="loginUser(event)">
    <input type="email" id="email" placeholder="Email" required><br><br>
    <input type="password" id="password" placeholder="Password" required><br><br>
    <button type="submit">Login</button>
  </form>

  <div id="otpSection" style="display:none;">
    <h3>Enter OTP</h3>
    <input type="text" id="otpInput" placeholder="One-Time Passcode"><br><br>
    <button onclick="verifyOTP()">Verify OTP</button>
  </div>

  <script>
    let generatedOTP = null;
    let currentUser = null;

    function loginUser(event) {
      event.preventDefault();
      const email = document.getElementById("email").value;
      const password = document.getElementById("password").value;

      const users = JSON.parse(localStorage.getItem("users")) || [];
      const matchedUser = users.find(user => user.email === email && user.password === password);

      if (!matchedUser) {
        alert("Invalid credentials!");
        return;
      }

      // Save current user
      currentUser = matchedUser;

      // Generate and display OTP
      generatedOTP = Math.floor(100000 + Math.random() * 900000); // 6-digit OTP
      alert("Your OTP is: " + generatedOTP);

      document.getElementById("otpSection").style.display = "block";
    }

    function verifyOTP() {
      const enteredOTP = document.getElementById("otpInput").value;
      if (parseInt(enteredOTP) === generatedOTP) {
        localStorage.setItem("authToken", "sampleToken123"); // fake auth token
        localStorage.setItem("currentUser", JSON.stringify(currentUser));
        alert("Login successful!");
        window.location.href = "protected.html";
      } else {
        alert("Incorrect OTP!");
      }
    }
  </script>
</body>
</html>
```

#### 📌 Explanation:
- Matches input against `localStorage` user list.
- If valid, generates a 6-digit OTP.
- Stores fake `authToken` in localStorage to simulate a real token system.

---

## 🔒 Part 4: Protected Page with Token Check

### ✅ Goal:
Restrict access to authenticated users only by verifying the presence of a token in `localStorage`.

### 🔧 Instructions:

1. Create `protected.html`.
2. Check if `authToken` and `currentUser` exist in `localStorage`.
3. If not, redirect to login page.

### ✅ `protected.html` Code + Explanation:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Protected Page</title>
</head>
<body>
  <h2>Protected Page</h2>
  <div id="content"></div>

  <script>
    const token = localStorage.getItem("authToken");
    const user = JSON.parse(localStorage.getItem("currentUser"));

    if (!token || !user) {
      alert("You are not authorized. Please log in.");
      window.location.href = "login.html";
    } else {
      document.getElementById("content").innerHTML = `
        <p>Welcome, ${user.email}!</p>
        <button onclick="logout()">Logout</button>
      `;
    }

    function logout() {
      localStorage.removeItem("authToken");
      localStorage.removeItem("currentUser");
      alert("Logged out successfully.");
      window.location.href = "login.html";
    }
  </script>
</body>
</html>
```

#### 📌 Explanation:
- Uses `localStorage.getItem()` to check authentication.
- Blocks unauthorized access.
- Adds a logout button to clear session.

---

## ✅ Summary of All Steps

| Feature                     | File             | Functionality                                        |
|----------------------------|------------------|-----------------------------------------------------|
| 🔐 Registration            | `register.html`  | User enters email and password, saved to localStorage |
| 🔓 Login                   | `login.html`     | Validates credentials and shows OTP field            |
| 🔢 OTP Verification        | `login.html`     | 6-digit code generated, must be entered correctly     |
| 🔒 Protected Page          | `protected.html` | Accessible only if valid token exists in localStorage |
| 🚪 Logout                  | `protected.html` | Clears auth token and redirects to login             |

---

## 📌 Notes:
- This is a simulation and should **NOT** be used for real user data.
- For production systems, always use:
  - A backend with encrypted databases
  - Real authentication APIs
  - Secure session tokens and cookies
  - HTTPS

---

 **Part 5: Implementing Local OAuth 2.0 Authentication** — building on your existing system. This guide assumes you already have a **custom OAuth 2.0 server** running locally. We'll now:

1. Modify the **web app (`app.js`)** to handle the OAuth login and callback routes.
2. Add an **OAuth login button** in `login.html`.
3. Handle **authorization code** and **token exchange**.

---

## 🔐 Part 5: Local OAuth 2.0 Authentication System

---

### ✅ Goal:
Enhance user authentication by integrating your **custom OAuth 2.0 server** with your existing login system.

---

## 📁 Folder Structure Update

```
/web-app
├── app.js            <-- Web app Express server
├── views/
│   └── login.html    <-- Updated login page
```

---

## 1️⃣ `app.js` - Web App Configuration (Express)

### 🔧 Instructions:

- Create `/oauth-login` route → Redirect to custom OAuth server
- Create `/oauth-callback` route → Exchange code for token

### ✅ Sample `app.js` (web app):
```js
const express = require('express');
const axios = require('axios');
const path = require('path');

const app = express();
const PORT = 3000;

// Replace these with your custom OAuth server values
const OAUTH_SERVER = 'http://localhost:4000'; // Your local OAuth server
const CLIENT_ID = 'my-client-id';
const CLIENT_SECRET = 'my-client-secret';
const REDIRECT_URI = 'http://localhost:3000/oauth-callback';

app.use(express.static('views'));

// 1. Redirect user to OAuth server
app.get('/oauth-login', (req, res) => {
  const authURL = `${OAUTH_SERVER}/authorize?response_type=code&client_id=${CLIENT_ID}&redirect_uri=${REDIRECT_URI}`;
  res.redirect(authURL);
});

// 2. Handle the OAuth callback and exchange code for token
app.get('/oauth-callback', async (req, res) => {
  const code = req.query.code;
  try {
    const tokenRes = await axios.post(`${OAUTH_SERVER}/token`, {
      grant_type: 'authorization_code',
      code,
      redirect_uri: REDIRECT_URI,
      client_id: CLIENT_ID,
      client_secret: CLIENT_SECRET
    });

    const accessToken = tokenRes.data.access_token;
    const userInfoRes = await axios.get(`${OAUTH_SERVER}/userinfo`, {
      headers: { Authorization: `Bearer ${accessToken}` }
    });

    const user = userInfoRes.data;

    // Save token in localStorage using script injection
    res.send(`
      <script>
        localStorage.setItem("authToken", "${accessToken}");
        localStorage.setItem("currentUser", JSON.stringify(${JSON.stringify(user)}));
        alert("OAuth Login Successful!");
        window.location.href = "/protected.html";
      </script>
    `);
  } catch (error) {
    console.error('OAuth Error:', error);
    res.send("OAuth authentication failed. Please try again.");
  }
});

app.listen(PORT, () => {
  console.log(`Web App running at http://localhost:${PORT}`);
});
```

---

## 2️⃣ Modify `login.html` — Add OAuth Button

### 🔧 Instructions:
- Add a "Login with OAuth" button that links to `/oauth-login`.

### ✅ Updated `views/login.html`:
```html
<!-- Existing Login Form Here -->

<hr>
<h3>OR</h3>
<button onclick="window.location.href='/oauth-login'">
  Login with OAuth
</button>
```

---

## 🧪 Testing the OAuth Flow

### ✅ Pre-requisites:
- Your custom **OAuth server is running** on `http://localhost:4000`
- Your **OAuth server supports**:
  - `/authorize` route
  - `/token` route
  - `/userinfo` route

### 🔁 Flow Summary:
1. User clicks **Login with OAuth**
2. Redirected to your OAuth server’s **/authorize** page
3. After approval, redirected back to `/oauth-callback?code=...`
4. Your app exchanges the code for an **access token**
5. Access token is saved to `localStorage`
6. User is redirected to **protected.html**

---

## 📌 Security Notes:
- This simulates OAuth 2.0 locally for learning purposes.
- Use HTTPS and secure token storage (not localStorage) in production.
- Never expose `client_secret` in frontend apps — only backend!

---

## 🧾 Final Checklist

| Feature | File | Action |
|--------|------|--------|
| Redirect to OAuth server | `app.js` `/oauth-login` | ✅ |
| Handle token exchange | `app.js` `/oauth-callback` | ✅ |
| OAuth button | `views/login.html` | ✅ |
| Save token & user | JS Injection in `/oauth-callback` | ✅ |

---

 **Part 6: Implementing Role-Based Access Control (RBAC)** to your web app, including detailed instructions and code examples. This will allow different users to see or access different content depending on their roles (e.g., `admin`, `user`, `moderator`, etc.).

---

## 🛡️ Part 6: Role-Based Access Control (RBAC)

---

### ✅ Goal:
After successful login, assign a **role** to the user and **control content access** based on that role.

---

### 🔧 Folder Recap:

```
/web-app
├── app.js               <-- Web app logic
├── views/
│   ├── login.html       <-- Modified to store user role
│   ├── protected.html   <-- Modified to display role-based content
```

---

## 1️⃣ Modify `app.js` – Assign Roles After Login

### ✅ Update OAuth callback to assign a role

Modify `/oauth-callback` to:
- Check email of user
- Assign a role (e.g., based on email)
- Send role along with user data to frontend

### ✨ Sample Logic:
```js
// Inside /oauth-callback
const user = userInfoRes.data;

// Assign roles based on email (can be dynamic or database-driven)
let role = 'user';
if (user.email === 'admin@example.com') {
  role = 'admin';
} else if (user.email.endsWith('@moderator.com')) {
  role = 'moderator';
}

// Send token, user info, and role to frontend
res.send(`
  <script>
    localStorage.setItem("authToken", "${accessToken}");
    localStorage.setItem("currentUser", JSON.stringify(${JSON.stringify(user)}));
    localStorage.setItem("role", "${role}");
    alert("OAuth Login Successful! Role: ${role}");
    window.location.href = "/protected.html";
  </script>
`);
```

> 📝 You can enhance this by fetching role data from a database or role service later.

---

## 2️⃣ Modify `login.html` — Store Role After Login (for traditional login)

If you're using **email-password login (non-OAuth)** too, update your script there as well:

```html
<script>
function loginUser(event) {
  event.preventDefault();
  const email = document.getElementById("email").value;
  const password = document.getElementById("password").value;

  const users = JSON.parse(localStorage.getItem("users")) || [];
  const user = users.find(u => u.email === email && u.password === password);

  if (user) {
    // Assign role based on email
    let role = "user";
    if (user.email === "admin@example.com") {
      role = "admin";
    } else if (user.email.endsWith("@moderator.com")) {
      role = "moderator";
    }

    localStorage.setItem("authToken", "some-auth-token");
    localStorage.setItem("currentUser", JSON.stringify(user));
    localStorage.setItem("role", role);

    alert("Login Successful. Role: " + role);
    window.location.href = "protected.html";
  } else {
    alert("Invalid credentials");
  }
}
</script>
```

---

## 3️⃣ Modify `protected.html` – Show Content Based on Role

### ✅ Instructions:
- On page load, check the saved role.
- Display content conditionally.

### ✨ Example Code:
```html
<body>
  <h2>Protected Page</h2>
  <div id="content"></div>

  <script>
    const token = localStorage.getItem("authToken");
    const role = localStorage.getItem("role");

    if (!token) {
      alert("You are not authorized. Please log in.");
      window.location.href = "login.html";
    }

    const contentDiv = document.getElementById("content");

    if (role === "admin") {
      contentDiv.innerHTML = `
        <h3>Welcome Admin!</h3>
        <p>You have full access to user management and data control.</p>
      `;
    } else if (role === "moderator") {
      contentDiv.innerHTML = `
        <h3>Welcome Moderator!</h3>
        <p>You can manage posts and moderate user activity.</p>
      `;
    } else if (role === "user") {
      contentDiv.innerHTML = `
        <h3>Welcome User!</h3>
        <p>You can view and update your profile.</p>
      `;
    } else {
      contentDiv.innerHTML = `
        <h3>Welcome Guest!</h3>
        <p>Your role is unknown. Access is limited.</p>
      `;
    }
  </script>
</body>
```

---

## 🔐 Role Mapping Ideas (Optional Advanced):
| Email Pattern                | Role       |
|-----------------------------|------------|
| admin@example.com           | admin      |
| endsWith `@moderator.com`   | moderator  |
| all others                  | user       |

---

## ✅ Final Checklist

| Task | Status |
|------|--------|
| Assign roles in `/oauth-callback` or login script | ✅ |
| Store role in `localStorage` | ✅ |
| Read role in `protected.html` and display content accordingly | ✅ |
| Prevent access if no token | ✅ |

---



# 🧪 Step-by-Step Instructions for Testing Authentication, MFA, OAuth Login, and Role-Based Access Control (RBAC)

---

## 1️⃣ **Test Authentication and MFA**

#### ✅ **Step 1: Register the User**
1. **Navigate to Register Page:**
   - Open your browser and go to:  
     `http://localhost:4001/register.html`
   
2. **Register User:**
   - **Email:** `test@example.com`
   - **Password:** `password`
   - Click on **Register** button to create the account.

---

#### ✅ **Step 2: Log in with Credentials**
1. **Navigate to Login Page:**
   - Open your browser and go to:  
     `http://localhost:4001/login.html`
   
2. **Enter Credentials:**
   - **Username (Email):** `test@example.com`
   - **Password:** `password`
   - Click **Login**.

3. **Enter One-Time Password (OTP):**
   - After entering login credentials, a random OTP code will be displayed. For example, something like `123456`.
   - **Copy OTP Code** and paste it into the provided OTP field.
   - Click **Verify OTP**.

4. **Successful Login:**
   - If login is successful, you should be redirected to:  
     `protected.html`  
   - The **User Dashboard** should be displayed, confirming a successful authentication process.

---

### 2️⃣ **Test OAuth Login**

#### ✅ **Step 1: Navigate to Login Page**
1. Open your browser and go to:  
   `http://localhost:4001/login.html`

#### ✅ **Step 2: Login Using OAuth**
1. On the login page, you will find a button labeled **Login with OAuth**.
2. Click the **Login with OAuth** button to be redirected to the OAuth provider.
   - This should redirect you to the OAuth server that you have set up (e.g., your custom OAuth server).

#### ✅ **Step 3: OAuth Redirection & Callback**
1. After successful OAuth authentication, the OAuth server will redirect you back to your web app with a token and the user's details.
2. On successful OAuth login, you should be redirected to:  
   `protected.html`
3. The **User Dashboard** should be displayed, confirming that OAuth authentication worked successfully.

---

### 3️⃣ **Test Role-Based Access Control (RBAC)**

#### ✅ **Step 1: Test Admin Role Access**
1. **Navigate to Login Page:**
   - Open your browser and go to:  
     `http://localhost:4001/login.html`

2. **Enter Admin Credentials:**
   - **Username (Email):** `admin@example.com`
   - **Password:** `admin123`
   - Click **Login**.

3. **Enter One-Time Password (OTP):**
   - After entering login credentials, a random OTP code will be displayed.
   - **Copy OTP Code** and paste it into the provided OTP field.
   - Click **Verify OTP**.

4. **Successful Login:**
   - If login is successful, you should be redirected to:  
     `protected.html`  
   - The **Admin Dashboard** should be displayed, confirming that the admin role has been granted and the proper content is shown based on the role.

#### ✅ **Step 2: Test Regular User Role Access**
1. **Navigate to Login Page:**
   - Open your browser and go to:  
     `http://localhost:4001/login.html`

2. **Enter Regular User Credentials:**
   - **Username (Email):** `test@example.com`
   - **Password:** `password`
   - Click **Login**.

3. **Enter One-Time Password (OTP):**
   - After entering login credentials, a random OTP code will be displayed.
   - **Copy OTP Code** and paste it into the provided OTP field.
   - Click **Verify OTP**.

4. **Successful Login:**
   - If login is successful, you should be redirected to:  
     `protected.html`  
   - The **User Dashboard** should be displayed for the regular user role, confirming that content access is properly restricted based on the user's role.

---

### 🛠️ **What to Expect During Tests:**

1. **Authentication and MFA:**
   - **User Dashboard** should be shown only after successful login and OTP verification.

2. **OAuth Login:**
   - The **OAuth** process should redirect you back to the app with an authenticated session, showing the **User Dashboard**.

3. **Role-Based Access Control (RBAC):**
   - **Admin Dashboard** should only be shown when logged in as `admin@example.com` and after entering the OTP.
   - **User Dashboard** should be shown for other users, restricting admin-only access.

---

### 💡 **Troubleshooting Tips:**

- **Incorrect OTP or credentials:** Ensure that you’ve entered the correct email and password for each login attempt.
- **Role mismatches:** If the correct dashboard doesn’t appear (e.g., the Admin Dashboard is shown to regular users), verify that the role is correctly assigned on the backend and sent to the frontend after successful login.
- **OAuth issues:** Make sure that the OAuth callback logic is set up correctly, and that tokens are being stored and handled securely.

---


