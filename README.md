# WebIn Project Documentation

## Overview
WebIn is a full-stack web application built using FastAPI for the backend, React and Tailwind CSS for the frontend, and PostgreSQL as the database. This document provides comprehensive details about the project structure, technology stack, and setup instructions.

## Technology Stack
- **Backend:** FastAPI
- **Frontend:** React, Tailwind CSS
- **Database:** PostgreSQL

## Project Structure
### Backend (FastAPI)
- **app/**: Contains the main application code.
  - **api/**: All the API endpoints are defined here.
  - **models/**: Contains the database models that correspond to the PostgreSQL tables.
  - **schemas/**: Pydantic schemas for data validation and serialization.
  - **database.py**: Database connection and configuration settings.
  
### Frontend (React + Tailwind)
- **src/**: The source code for the React application.
  - **components/**: Reusable components for the application UI.
  - **pages/**: Page components for various routes.
  - **styles/**: Tailwind configuration and custom styles.
  - **App.js**: Main application component that brings everything together.

### Database (PostgreSQL)
- **Schemas:**
  - **Users**: Table to store user information.
  - **Posts**: Table to manage posts submitted by users.
  - **Comments**: Table to handle comments on posts.

## Setup Instructions
### Backend Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/MeetUp2026/WebIn.git
   cd WebIn
   ```
2. Install the necessary Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up the PostgreSQL database and update the `database.py` with your connection details.
4. Start the FastAPI server:
   ```bash
   uvicorn app.main:app --reload
   ```

### Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install the required npm packages:
   ```bash
   npm install
   ```
3. Start the React development server:
   ```bash
   npm start
   ```

## Notes
- Make sure to set up environment variables as needed for the application.
- For production deployment, consider using Docker or cloud services.

## Conclusion
WebIn aims to provide a seamless experience for users to interact and share their thoughts. Please refer to the respective sections for detailed information on each component and its setup.