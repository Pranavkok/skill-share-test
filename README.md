# Skill Share Platform

A web-based application that connects users who need help with users who have the skills to provide it.

## What the project does

This platform allows users to submit prompts or questions about a specific topic. The application then uses AI to identify the relevant skill required and notifies other users who have listed that skill on their profile. Users can then connect in a chat or video room to share their knowledge. The platform also includes an in-app currency system ("coins") to facilitate transactions between users.

## Key Features

- **User Authentication:** Secure user registration and login.
- **Skill-Based Matching:** AI-powered tagging of user prompts to match them with users who have the relevant skills.
- **Real-time Notifications:** A notification system to alert users of new help requests.
- **Chat and Video Rooms:** Integrated chat and video conferencing (using Jitsi) to enable real-time collaboration.
- **In-app Currency:** A "coin" system for users to exchange for services.
- **User Profiles:** Users can manage their profiles, including their list of skills.

## Tech Stack

### Backend

- **Framework:** Node.js, Express.js
- **Database:** MongoDB with Mongoose
- **Authentication:** JWT, bcryptjs
- **Messaging Queue:** RabbitMQ
- **AI:** Google Generative AI
- **Other:** Helmet, Morgan, CORS, dotenv

### Frontend

- **Framework:** React, Vite
- **Styling:** Tailwind CSS
- **Routing:** React Router
- **HTTP Client:** Axios
- **Video Conferencing:** Jitsi
- **UI/UX:** Framer Motion, Lucide React

## How to get started

### Prerequisites

- Node.js (v18 or higher)
- npm
- MongoDB instance
- RabbitMQ instance

### Backend Setup

1.  Navigate to the `backend` directory:
    ```bash
    cd backend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `backend` directory and add the following environment variables:
    ```
    PORT=3001
    FRONTEND_URL=http://localhost:5173
    MONGODB_URI=<your_mongodb_uri>
    JWT_SECRET=<your_jwt_secret>
    RABBITMQ_URL=<your_rabbitmq_url>
    GOOGLE_API_KEY=<your_google_api_key>
    ```
4.  Start the development server:
    ```bash
    npm run dev
    ```
5.  Start the workers:
    ```bash
    npm run worker:a
    npm run worker:b
    ```

### Frontend Setup

1.  Navigate to the `frontend` directory:
    ```bash
    cd frontend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env` file in the `frontend` directory and add the following environment variable:
    ```
    VITE_API_URL=http://localhost:3001
    ```
4.  Start the development server:
    ```bash
    npm run dev
    ```

The application should now be running at `http://localhost:5173`.

## Where to get help

This is a sample project. For any issues or questions, please open an issue in the GitHub repository.

## Who maintains and contributes

This project is maintained by the Gemini team. We welcome contributions from the community. Please feel free to fork the repository, make your changes, and submit a pull request.
