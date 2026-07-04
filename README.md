# Mini CRM – Client Lead Management System.

A production-grade, full-stack **Customer Relationship Management (CRM)** platform built to manage sales leads, track conversion workflows, and provide real-time analytics. This is a complete business tool designed with modern development practices.

---

## 🎯 Features

### 🔐 **Authentication & Security**
- JWT-based secure admin login system
- Password hashing with bcryptjs
- Protected routes with authentication middleware
- Automatic token injection in API requests

### 📊 **Lead Management (Full CRUD)**
- **Create**: Add new leads with email validation
- **Read**: Display all leads with real-time filtering
- **Update**: Edit lead details and status instantly
- **Delete**: Remove leads with confirmation

### 🔄 **Workflow Management**
- **Status Lifecycle**: New → Contacted → Converted
- Real-time status updates with dropdown selector
- Color-coded status indicators for quick visual reference
- Automatic timestamp tracking on all operations

### 📝 **Notes & Follow-up System**
- Add unlimited follow-up notes to each lead
- Chronological note history display
- Track communication and next steps
- Persistent storage in MongoDB

### 🔍 **Search & Filtering**
- Real-time search across name, email, and phone fields
- Case-insensitive regex matching
- Sorted by most recent leads first

### 📈 **Analytics Dashboard**
- **Total Leads Counter** - Track pipeline size
- **Status Breakdown** - New, Contacted, Converted counts
- **Conversion Rate %** - Real-time conversion percentage
- **Live Updates** - Analytics refresh as status changes

### 🎨 **Professional UI/UX**
- Clean, modern dashboard layout
- Responsive design with proper touch support
- Color-coded visual system for quick scanning
- Intuitive form validation and error handling
- Smooth transitions and professional styling

---

## 🛠️ Tech Stack

### **Frontend**
- **React.js 18** – Modern UI library with hooks
- **React Router v6** – Client-side routing
- **Axios** – HTTP client with request interceptors
- **CSS-in-JS** – Styled components for responsive design

### **Backend**
- **Node.js & Express.js** – REST API server
- **MongoDB & Mongoose** – NoSQL database with schema validation
- **JWT (jsonwebtoken)** – Secure authentication tokens
- **bcryptjs** – Password hashing and verification
- **CORS & Morgan** – Cross-origin support and logging
- **dotenv** – Environment variable management

---

## 📋 Prerequisites

Before you begin, ensure you have installed:
- **Node.js** (v14 or higher)
- **npm** (comes with Node.js)
- **MongoDB** (local or MongoDB Atlas account)

---

## ⚙️ Installation & Setup

### **1. Clone the Repository**
```bash
git clone https://github.com/Nisarga-Nisha08/mini-crm.git
cd mini-crm
```

### **2. Backend Setup**

Navigate to the backend folder:
```bash
cd backend
```

Install dependencies:
```bash
npm install
```

Create a `.env` file in the `backend/` directory:
```env
MONGO_URI=mongodb://localhost:27017/mini_crm
PORT=5001
JWT_SECRET=your_super_secret_key_here_change_in_production
```

Start the backend server:
```bash
node server.js
```

You should see:
```
Server running on port 5001
MongoDB connected
```

### **3. Frontend Setup**

In a new terminal, navigate to the frontend folder:
```bash
cd frontend
```

Install dependencies:
```bash
npm install
```

Start the development server:
```bash
npm start
```

The app will open at `http://localhost:3000`

---

## 🚀 How to Use

### **1. Login**
Register a new admin using /api/auth/register
Then login using your created credentials.

### **2. Create a Lead**
Fill in the "Add New Lead" form and click "Create Lead"

### **3. Manage Lead Status**
Click the status dropdown and select: `New` → `Contacted` → `Converted`

### **4. Add Notes**
Type a follow-up note and click "Add" to track communication

### **5. Search Leads**
Use the search bar to filter by name, email, or phone

### **6. Track Analytics**
Watch real-time metrics update as you manage leads

---

## 📁 Project Structure
mini-crm/
├── backend/
│   ├── models/
│   │   ├── Admin.js
│   │   └── Lead.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   └── leadRoutes.js
│   ├── middleware/
│   │   └── authMiddleware.js
│   ├── config/
│   │   └── db.js
│   ├── .env
│   ├── server.js
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── LeadForm.js
│   │   │   └── LeadTable.js
│   │   ├── pages/
│   │   │   ├── Login.js
│   │   │   └── Dashboard.js
│   │   ├── services/
│   │   │   └── api.js
│   │   ├── App.js
│   │   └── index.js
│   ├── public/
│   │   └── index.html
│   └── package.json
├── screenshots/
│   ├── login.png
│   ├── dashboard.png
│   ├── leads.png
│   ├── add-lead.png
│   └── analytics.png
└── README.md


---

## 🔌 API Endpoints

All endpoints require JWT authentication.

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new admin |
| POST | `/api/auth/login` | Login and get JWT token |
| GET | `/api/leads` | Get all leads (searchable) |
| POST | `/api/leads` | Create a new lead |
| PUT | `/api/leads/:id` | Update lead status, notes, etc. |
| DELETE | `/api/leads/:id` | Delete a lead |

---

## 🔒 Security Features

✅ JWT token-based authentication  
✅ Password hashing with bcryptjs  
✅ Protected API routes with middleware  
✅ CORS enabled for frontend  
✅ Environment variables for sensitive data  
✅ Input validation with Mongoose schemas  

---

## 🚀 Deployment

### **Backend to Render**
Deploy your Node.js backend for free with environment variables support

### **Frontend to Vercel**
Deploy your React app with automatic builds from GitHub

---

## 📄 License

MIT License - Feel free to use this project!

---

## 👨‍💻 Author

Built as a full-stack demonstration project showcasing:
- Modern React patterns
- RESTful API design
- JWT authentication
- MongoDB database design
- Professional code architecture

**Made with 💻 and ☕**
