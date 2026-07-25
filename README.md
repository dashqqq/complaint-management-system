# Complaint Management System

A modern, real-time Complaint Management System built using Firebase and vanilla JavaScript. The application is designed for small teams, IT departments, NOCs, and internal support teams to efficiently log, assign, track, and resolve complaints.

The system provides role-based access for administrators and operators, real-time synchronization using Firebase Firestore, and a clean, responsive user interface that works across desktop and mobile devices.

---

## Features

* Firebase Authentication (Email & Password)
* Real-time Firestore synchronization
* Role-based access control (Admin & Operator)
* Complaint creation and management
* Complaint assignment to operators
* Self-assignment for operators
* Priority-based complaint tracking
* Complaint lifecycle management
* Resolution notes and history tracking
* Export complaints as CSV files (Excel compatible)
* Responsive and modern user interface
* Firebase Hosting support
* Lightweight single-page application

---

## Complaint Workflow

```
Complaint Logged
        ↓
     Pending
        ↓
     Assigned
        ↓
   In Progress
        ↓
     Resolved
        ↓
      Closed
```

---

## User Roles

### Administrator

Administrators can:

* Create new complaints.
* View all complaints in real time.
* Assign complaints to operators.
* View complaint statistics.
* Export complaint reports.
* Close resolved complaints.
* Delete complaints.
* View complete complaint details and history.

### Operator

Operators can:

* View their assigned complaints.
* Self-assign available complaints.
* Start working on complaints.
* Mark complaints as resolved.
* Add resolution notes.
* View complaint details.

---

## Technologies Used

* HTML5
* CSS3
* Vanilla JavaScript
* Firebase Authentication
* Firebase Firestore
* Firebase Hosting

---

## Project Structure

```
Complaint-Management-System/

├── index.html
├── firebase.json
├── .firebaserc
├── .gitignore
└── README.md
```

---

## Firebase Setup

### Step 1 - Create a Firebase Project

Create a new Firebase project from the Firebase Console.

### Step 2 - Enable Authentication

Enable:

* Email/Password Authentication

Create the administrator account that will be used to manage complaints.

---

### Step 3 - Enable Firestore Database

Create a Firestore database for storing:

* Users
* Complaints

The application automatically creates operator records when users log in for the first time.

---

### Step 4 - Configure Firebase Credentials

Replace the placeholder Firebase configuration inside `index.html` with your own Firebase project's credentials.

Example:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
};
```

---

### Step 5 - Configure Administrator Accounts

Replace the administrator email list with your own.

Example:

```javascript
const adminEmails = [
    "admin@example.com"
];
```

Only users listed here will have administrator privileges.

---

## Running the Application

You can run the application locally by opening:

```
index.html
```

or by using Firebase Hosting's local server.

```bash
firebase serve
```

---

## Deployment

### Install Firebase CLI

```bash
npm install -g firebase-tools
```

### Login to Firebase

```bash
firebase login
```

### Initialize Firebase

```bash
firebase init
```

### Deploy the Application

```bash
firebase deploy
```

---

## Complaint Management Features

The application includes:

* Complaint logging
* Real-time updates
* Complaint assignment
* Operator workflow management
* Complaint resolution notes
* Status tracking
* Search functionality
* Filtering by complaint status
* Complaint statistics dashboard
* CSV report export
* Toast notifications
* Loading indicators
* Responsive design

---

## Status Types

| Status      | Description                               |
| ----------- | ----------------------------------------- |
| Pending     | Newly created complaint                   |
| Assigned    | Assigned to an operator                   |
| In Progress | Work has started                          |
| Resolved    | Issue has been resolved                   |
| Closed      | Complaint has been completed and archived |

---

## Priority Levels

| Priority | Description         |
| -------- | ------------------- |
| Low      | Minor issues        |
| Medium   | Standard complaints |
| High     | Important issues    |
| Urgent   | Critical complaints |

---

## Future Improvements

Some possible enhancements include:

* Email notifications
* File attachment support
* Dashboard analytics and charts
* SLA tracking
* Multi-department management
* Dark mode support
* Audit logs
* Advanced reporting and search capabilities
* Push notifications

---

## Security Notes

Before publishing this project publicly, it is recommended that you:

* Remove your actual Firebase credentials.
* Replace administrator email addresses with placeholders.
* Configure appropriate Firestore security rules.
* Avoid committing sensitive or environment-specific information to GitHub.

---

## License

This project is released under the MIT License. Feel free to use, modify, and distribute it in accordance with the license terms.
