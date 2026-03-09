<div align="center">

# <img src="public/icons/graduation.png" width="45"> Teachers Database Management System <img src="public/icons/to-do-list.png" width="45">

[![Website](https://img.shields.io/badge/Website-Live-FF6B6B?logo=google-chrome&logoColor=white)](https://wonderful-emerald-pepper.glitch.me)
[![Node.js](https://img.shields.io/badge/Node.js-Runtime-339933?logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-Web%20Framework-404D59?logo=express&logoColor=white)](https://expressjs.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-Backend-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Pug](https://img.shields.io/badge/Pug-Template%20Engine-A86454?logo=pug&logoColor=white)](https://pugjs.org/)
[![JSON](https://img.shields.io/badge/Data-JSON-000000?logo=json&logoColor=white)](https://www.json.org/)
[![Nodemon](https://img.shields.io/badge/Nodemon-Dev%20Server-76D04B?logo=nodemon&logoColor=white)](https://nodemon.io/)
[![Glitch](https://img.shields.io/badge/Hosting-Glitch-3333FF?logo=glitch&logoColor=white)](https://glitch.com/)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

**🌟 A comprehensive web-based teachers database management system built with Node.js, Express.js, and Pug templating! 🌟**

Built with **modern server-side technologies** for efficient data management and seamless user experience.

[🚀 Live Demo](#-live-demo) • [✨ Features](#-features) • [📋 API Documentation](#-api-documentation)

---

</div>

## 🎯 Overview

A robust **Teachers Database Management System** that provides a complete solution for managing teacher records with **full CRUD operations**. Built with **Node.js** and **Express.js** backend, featuring a clean **Pug.js** templating system and **JSON-based data storage** for optimal performance and simplicity.

### 📂 **What's Inside This System?**
- **👥 Teacher Management** - Complete teacher profile management
- **📝 CRUD Operations** - Create, Read, Update, Delete functionality  
- **🎨 Modern UI/UX** - Clean, professional interface with Pug templates
- **📊 JSON Database** - Lightweight file-based data storage
- **🔧 RESTful API** - Clean API endpoints for data access
- **⚡ Fast Performance** - Optimized Express.js server architecture

---

## ✨ Features

### 🔧 **Core Functionality**

| Operation | Description | Implementation |
|-----------|-------------|----------------|
| **Create** | Add new teacher records | POST `/add` |
| **Read** | View all teachers & individual profiles | GET `/staff`, `/staff/:id` |
| **Update** | Edit existing teacher information | POST `/:id/edit` |
| **Delete** | Remove teacher records | GET `/:id/delete` |
| **API Access** | JSON API for external access | GET `/api/v1/staff` |

### 📊 **Teacher Data Fields**

#### **Complete Teacher Profile**
- **👤 Personal Information**
  - First Name & Last Name
  - Age
  - Email Address
- **🎓 Academic Details**
  - Major/Specialization
  - Unique ID Generation
- **🔄 Dynamic Updates**
  - Real-time form validation
  - Success/Error feedback
  - Data persistence

### 🎨 **User Interface Features**

#### **Responsive Web Interface**
- **🏠 Home Page** - Welcome dashboard with quick navigation
- **➕ Add Teacher** - Comprehensive form for new teacher registration
- **👥 All Staff** - Complete teacher directory with management options
- **📝 Edit Profile** - Individual teacher profile editing interface
- **✅ Feedback System** - Success/error notifications for all operations

#### **Form Validation & UX**
- **📋 Required Field Validation** - Prevents empty submissions
- **✨ Success Messages** - Confirmation for successful operations
- **⚠️ Error Handling** - Clear error messages for failed operations
- **🔄 Real-time Updates** - Dynamic content updates without page reload

---

## 🏗️ System Architecture

### **🔧 Technology Stack**

| Technology | Version | Purpose |
|------------|---------|---------|
| **Node.js** | Latest | Server runtime environment |
| **Express.js** | Latest | Web application framework |
| **Pug.js** | Latest | Template engine |
| **JSON** | Native | Data storage |
| **CSS3** | Latest | Styling and responsive design |

### **📁 Project Structure**
```
📦 Teachers-Database-Project/
├── 🏠 index.js                     # Main server file
├── 📁 views/                       # Pug templates
│   ├── 🎨 layout.pug              # Base template layout
│   ├── 🏠 home.pug                # Home page template
│   ├── ➕ create.pug              # Add teacher form
│   ├── 👥 staff.pug               # All teachers list
│   └── 📝 detail.pug              # Edit teacher form
├── 📁 data/                        # Data storage
│   └── 📊 staff.json              # Teacher records database
├── 📁 public/                      # Static assets
│   └── 📁 styles/                 # CSS stylesheets
│       └── 🎨 style.css           # Main stylesheet
├── 📦 package.json                # Project dependencies
└── 📖 README.md                   # Project documentation
```

### **⚡ Server Configuration**
```javascript
// Core Server Setup
const express = require("express")
const app = new express()
const fs = require('fs')

// Template Engine Configuration
app.set('view engine', 'pug')

// Middleware Setup
app.use('/static', express.static('public'))
app.use(express.urlencoded({ extended: false }))

// Port Configuration
const PORT = process.env.PORT || 3000
```

---

## 📋 API Documentation

### **🔗 Available Endpoints**

#### **📄 Web Routes**
```http
GET  /                    # Home page
GET  /add                 # Add teacher form
POST /add                 # Create new teacher
GET  /staff               # View all teachers
GET  /staff/:id           # View specific teacher
POST /:id/edit            # Update teacher information
GET  /:id/delete          # Delete teacher record
```

#### **🔌 API Endpoints**
```http
GET  /api/v1/staff        # JSON API - Get all teachers
```

### **📝 Request/Response Examples**

#### **Create Teacher (POST /add)**
```javascript
// Request Body
{
  firstname: "John",
  secondname: "Doe", 
  age: "35",
  emailaddress: "john.doe@email.com",
  major: "claw"  // Commercial law
}

// Response: Redirect to success page
```

#### **API Response (GET /api/v1/staff)**
```json
[
  {
    "id": "_abc123def",
    "firstname": "John",
    "secondname": "Doe",
    "age": "35", 
    "emailaddress": "john.doe@email.com",
    "major": "claw"
  }
]
```

### **🎓 Available Majors**
| Code | Description |
|------|-------------|
| `claw` | Commercial Law |
| `ecofin` | Economics with Finance |
| `fin` | Finance |
| `busmag` | Business Management |
| `bis` | Business Information System |

---

## 🚀 Installation & Setup

### **1. Prerequisites**
```bash
# Required Software
- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher)
- Git (for cloning)
```

### **2. Clone Repository**
```bash
git clone https://github.com/GhostKX/Teachers-Database-Project.git
cd Teachers-Database-Project
```

### **3. Install Dependencies**
```bash
npm install
```

### **4. Project Dependencies**
```json
{
  "dependencies": {
    "express": "^4.18.x",
    "pug": "^3.0.x"
  }
}
```

### **5. Run Application**
```bash
# Development Mode
node index.js

# Alternative with nodemon (if installed)
npm install -g nodemon
nodemon index.js
```

### **6. Access Application**
```
🌐 Local Server: http://localhost:3000
🚀 Live Demo: https://wonderful-emerald-pepper.glitch.me
```

---

## 🚀 Live Demo

### **🌐 Hosted Application**
**Live Website:** [Teachers Database System](https://teachers-database-project.onrender.com/)
- ***Note*** - May take some time to load the website

### **🔧 Deployment Platform**
- **Glitch Hosting** - Professional cloud hosting
- **Automatic Deployment** - Updates from GitHub repository
- **24/7 Availability** - Reliable uptime and performance

### **📱 Device Compatibility**
The system works perfectly on:
- **💻 Desktop Browsers** - Chrome, Firefox, Safari, Edge
- **📱 Mobile Devices** - iOS Safari, Android Chrome
- **📟 Tablets** - iPad and Android tablet support

---

## 💾 Data Management

### **📊 JSON Database Structure**
```json
[
  {
    "id": "_unique_generated_id",
    "firstname": "Teacher First Name",
    "secondname": "Teacher Last Name", 
    "age": "Age in years",
    "emailaddress": "email@example.com",
    "major": "subject_code"
  }
]
```

### **🔧 Data Operations**

#### **Unique ID Generation**
```javascript
function id() {
  return '_' + Math.random().toString(36).substr(2, 9);
}
```

#### **File-Based Storage**
- **Location:** `./data/staff.json`
- **Format:** JSON array of teacher objects
- **Operations:** Read/Write using Node.js `fs` module
- **Persistence:** Data survives server restarts

---

## 🛠️ Development Guide

### **📝 Adding New Features**

#### **1. New Route Example**
```javascript
app.get('/teachers/search', (req, res) => {
  // Search functionality
  const query = req.query.q
  // Implementation logic
  res.render('search', { query: query })
})
```

#### **2. New Template Example**
```pug
// views/search.pug
extends layout.pug

block content
  .container
    h2 Search Results
    // Template content
```

#### **3. Form Validation Enhancement**
```javascript
// Enhanced validation
if (!firstname || !secondname || !age || !emailaddress) {
  return res.render('create', { 
    error: true, 
    message: 'All fields are required' 
  })
}
```

### **🔧 Customization Options**

#### **Styling Modifications**
- Edit `public/styles/style.css` for visual changes
- Modify Pug templates for structure changes
- Add new CSS classes for enhanced styling

#### **Database Expansion**
- Add new fields to teacher schema
- Update forms and validation logic
- Modify JSON structure accordingly

---

## 📊 Performance & Features

### **⚡ Performance Optimizations**
- **Lightweight Framework** - Express.js minimal overhead
- **File-Based Storage** - No database setup required
- **Template Caching** - Pug template compilation optimization
- **Static Asset Serving** - Efficient CSS and asset delivery

### **🔒 Data Integrity**
- **Form Validation** - Client and server-side validation
- **Error Handling** - Comprehensive error management
- **Data Backup** - JSON file-based persistence
- **Unique IDs** - Collision-resistant ID generation

### **🎨 User Experience**
- **Intuitive Navigation** - Clear menu structure
- **Responsive Design** - Works on all device sizes
- **Real-time Feedback** - Immediate success/error messages
- **Clean Interface** - Professional and user-friendly design

---

## 🎓 Learning Outcomes

### **Skills Demonstrated**
- **Node.js Development** - Server-side JavaScript programming
- **Express.js Framework** - Web application development
- **Template Engines** - Pug.js templating system
- **CRUD Operations** - Complete data management cycle
- **File System Operations** - JSON data persistence
- **RESTful Design** - Clean API endpoint structure
- **Form Handling** - User input processing and validation

### **Best Practices Applied**
- **MVC Architecture** - Separation of concerns
- **Error Handling** - Robust error management
- **Code Organization** - Clean and maintainable structure
- **Data Validation** - Input sanitization and validation
- **RESTful Routes** - Standard HTTP method usage

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

## 👨‍💻 Author

**Teachers Database Management System** - Developed by **GhostKX**

[![GitHub](https://img.shields.io/badge/GitHub-@GhostKX-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/GhostKX)

---

</div>