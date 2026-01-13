# School Result Management System (Frontend)

This is the **frontend** of a School Result Management System built with **React** and **Tailwind CSS**. It allows schools to manage student results for JSS1–JSS3 classes, including student registration, attendance, result entry, and generation of student reports and class broadsheets. This frontend is designed to work with a separate backend API for persistent storage using MongoDB Atlas.

---

## Features

- Register students per class with auto-generated Student ID
- Enter student attendance (present / absent)
- Enter scores for 17 subjects per student (1st CA, 2nd CA, Exam)
- Automatic calculation of:
  - Subject Total
  - Grade & Remark per subject
  - Class Average per subject
  - Subject Position per student
  - Total Score per student
  - Average Score per student
  - Overall Class Position
- Session and Term selection, displayed on result and broadsheet
- Teacher and Principal remarks input
- Excel-style result entry table
- Fully integrated with backend API for MongoDB Atlas storage
- Supports persistent storage for student records, results, sessions, and classes

---

## Tech Stack

### Frontend
- React (Frontend framework)
- Tailwind CSS (Styling)
- jsPDF / html2canvas (for PDF export of results and broadsheets)
- Axios (for API requests to backend)

### Backend (Separate Repository)
- Node.js + Express (Server)
- MongoDB Atlas (Database)
- Mongoose (ODM for MongoDB)
- dotenv (Environment variables)
- CORS (Cross-Origin Resource Sharing)

### Storage
- MongoDB Atlas (cloud database for persistent storage)
  - Students collection
  - Results collection
  - Classes collection
  - Sessions collection

---



## Setup Instructions

### Frontend
1. Clone the repository:
```bash
git clone <frontend-repo-url>
cd frontend
```
2. Install dependencies:
```bash
npm install
```
3. Run the development server:
```bash
npm run dev
```
4. Open your browser at `http://localhost:5173`

### Backend (Separate)
1. Create backend folder and initialize Node project
```bash
mkdir backend
cd backend
npm init -y
```
2. Install dependencies
```bash
npm install express mongoose cors dotenv
npm install -D nodemon
```
3. Setup MongoDB Atlas and create `.env`
```env
MONGO_URI=<your-mongodb-atlas-uri>
PORT=5000
```
4. Connect backend to MongoDB using Mongoose, create routes for students, results, classes, and sessions.

---

## Notes

- All frontend calculations (totals, averages, positions, grades) are automatically done in React before sending to backend.
- Backend will handle persistent storage in MongoDB Atlas for all students, results, and class data.
- System supports session- and term-based result entry.
- Designed to generate PDFs for individual results and class broadsheets.

---

## Future Enhancements

- User authentication (login for teachers/admin)
- Export results in multiple formats (PDF, Excel)
- Analytics dashboard for class performance
- Multi-school support

---

**Portfolio Note:**
This project demonstrates a full-stack approach to building a scalable and professional school result management system using React, Tailwind, Node.js, and MongoDB Atlas. It showcases modular component design, API integration, database storage, and readiness for PDF report generation.
