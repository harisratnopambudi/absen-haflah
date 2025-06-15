# 🎉 Visitor Attendance Web App with Firebase

A simple and powerful QR-based attendance system built with **HTML**, **JavaScript**, and **Firebase Realtime Database**.

-----

## 📋 Features

  - ✅ **Real-time Attendance Recording**
  - 📷 **QR Code Scanner (html5-qrcode)**
  - ⚠️ **Duplicate Attendance Detection**
  - 📊 **Filter, Sort, and Export Visitor List to CSV**
  - 🔒 **Admin Authentication for Data Reset**
  - 🖨️ **QR Code Generator with PNG, ZIP, and PDF Export**
  - 🎉 **Live Welcome Screen with Real-time Visitor Display**

-----

## 🛠️ Tech Stack

  - **HTML5 & CSS3** 🎨
  - **JavaScript (ES6+)** 💻
  - **Firebase Realtime Database** ☁️
  - **Firebase Authentication** 🔐
  - **html5-qrcode** 📱
  - **FileSaver.js** 💾
  - **jsPDF & JSZip** 🗂️

-----

## 📂 Project Structure

```text
📁 project-root
├── 📄 index.html              # Main Menu
├── 📄 scanner.html            # QR Code Scanner
├── 📄 tamu.html               # Visitor List & Admin Dashboard
├── 📄 login.html              # Admin Login
├── 📄 welcome.html            # Visitor Welcome Display
├── 📄 barcode_generator.html  # QR Code Generator
└── 📄 README.md               # Project Documentation
```

-----

## ⚙️ Firebase Setup

### 1\. Create Firebase Project

Go to [Firebase Console](https://console.firebase.google.com/). Create a new project and register a Web App.

### 2\. Enable Services

#### Realtime Database:

Go to `Build > Realtime Database` and create a database.

**Recommended Security Rules:**

```json
{
  "rules": {
    "pengunjung": {
      ".read": true,
      ".write": "auth != null"
    }
  }
}
```

⚡ **For public write access (not recommended):**

```json
{
  "rules": {
    "pengunjung": {
      ".read": true,
      ".write": true
    }
  }
}
```

#### Authentication:

Enable `Email/Password` in `Build > Authentication > Sign-in Method`.

#### Create Admin Account:

Add an admin user for the data reset feature.

### 📝 Firebase Configuration

Update this in all HTML files:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID",
};
```

-----

## 🚀 How to Use

### 🖨️ Generate QR Codes

Use `barcode_generator.html` to create visitor QR codes.

### 📱 Scan Attendance

Open `scanner.html` on a smartphone to scan QR codes.

### 🎉 Welcome Visitors

Display `welcome.html` on a large screen to show real-time greetings.

### 📋 Manage Visitors

Open `tamu.html` to view, filter, sort, export, or reset visitor data. Reset data requires admin login from `login.html`.

-----

## 🔒 Security Tips

  - Public write access is **NOT safe** for production.
  - Always prefer authentication for write access.
  - For advanced security, consider using Firebase Cloud Functions.

-----

## 🎯 Pages Overview

| Page                 | Description                         |
| :------------------- | :---------------------------------- |
| `index.html`         | Main Menu                           |
| `scanner.html`       | QR Code Scanner                     |
| `tamu.html`          | Visitor List (with Admin Reset)     |
| `login.html`         | Admin Login Page                    |
| `welcome.html`       | Dynamic Welcome Display             |
| `barcode_generator.html` | QR Code Generator and Export Tool |

-----

## 📸 Screenshots (Optional)

You can add project screenshots or demo GIFs here.

-----

## 📜 License

This project is licensed under the MIT License.

-----

## 🚀 Happy Scanning\!

-----

I've formatted your README according to GitHub's Markdown. Is there anything else you'd like to add or change? For example, would you like to:

  - Add badges (like Firebase version, license, etc.)?
  - Create visual banners?
  - Generate demo GIFs?

Let me know\! 😊
