# Secure Safe

**Secure Safe** is a secure file-sharing application that allows users to transfer files safely between devices using end-to-end encryption. The app focuses on privacy, fast real-time communication, and secure authentication to ensure that files remain protected during transfer.

It is designed for local network communication, making it useful for classrooms, offices, laboratories, or personal device-to-device sharing. Files are encrypted before transmission, meaning even the server cannot access the original file contents.

---

## Features

* Secure encrypted file transfer between devices
* Real-time device connection using Socket.IO
* User registration and login system
* Device-to-device file sharing
* Accept or decline incoming files
* AES-256-CBC encryption for files
* RSA-2048 encryption for secure key exchange
* JWT authentication and bcrypt password hashing
* Simple and responsive user interface

---

# Setup

In the terminal, run:

```bash
npm install
node app.js
```

Then open this in your browser:

```bash
http://localhost:3000
```

---

# How to Use

### 1. Create an Account

Register a new account and log in to the application.

### 2. Connect Another Device

On another device connected to the same network, open:

```bash
http://<your-ip>:3000
```

Replace `<your-ip>` with your computer’s local IP address.

### 3. Send a File

* Choose an online device from the sidebar
* Select a file
* Click **Send Encrypted**

### 4. Receive a File

The receiving user can:

* Accept the file
* Decline the file transfer

If accepted, the file is securely decrypted on the receiver’s device.

---

# Technologies Used

* **Node.js + Express** → Backend server and API handling
* **Socket.IO** → Real-time communication between devices
* **AES-256-CBC + RSA-2048** → File encryption and secure key exchange
* **JWT + bcrypt** → Secure authentication and password protection
* **HTML / CSS / JavaScript** → Frontend interface and client-side functionality

---

# Security Details

* Files are encrypted before transmission
* The server cannot read the original file contents
* Passwords are hashed using bcrypt
* Authentication tokens are protected using JWT
* RSA is used to securely exchange encryption keys
* Real-time connections are handled securely through Socket.IO

---

# Important Notes

* User data is currently stored temporarily (no database integration yet)
* The application is intended mainly for local/private network use
* Before deploying online, configure:

  * HTTPS
  * A strong `JWT_SECRET`
  * Secure environment variables
  * Database storage and validation
  * Additional security protections (rate limiting, CSRF protection, etc.)

---

ort
* Two-factor authentication (2FA)
