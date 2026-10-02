# Trampei — Conectando talentos e oportunidades

A Brazilian web platform designed to seamlessly connect individuals and businesses looking for freelance services with skilled local professionals.

## 🚀 Key Features

*   **Authentication & Security:** Secure signup, login, JWT handling (cookies + headers), password recovery, Helmet, and rate limiting.
*   **Professional Profiles:** Dedicated portfolios, custom skill tags, real-time availability tracking, and past project showcases.
*   **Service Feed:** Advanced categorization, filtering, and an infinite scroll feed that automatically removes completed jobs.
*   **Unified Search:** Smart search engine equipped with dynamic queries and instant suggestions.
*   **Real-Time Communication:** Integrated live chat powered by Socket.io along with direct WhatsApp click-to-chat links (`wa.me`).
*   **Reviews & Ratings:** Mutual feedback and evaluation system after job completion.
*   **Modern UI/UX:** Interactive dashboard, location and tag-based recommendations, dark mode toggle, skeleton loaders, and responsive notifications.

## 🛠️ Tech Stack

### Frontend
*   React 19 & Next.js 16 (App Router)
*   Tailwind CSS 4 & Framer Motion
*   Axios & Socket.io-client
*   React-hot-toast & Next-themes

### Backend
*   Node.js & Express 5
*   MongoDB & Mongoose
*   JWT & Bcryptjs
*   Socket.io & Cloudinary
*   Helmet & Express Rate Limit

## 📁 Project Structure

```text
trampei/
├── client/              # Next.js Frontend (App Router)
│   ├── app/             # Pages and routing
│   ├── components/      # UI Elements
│   ├── context/         # Global state management
│   └── lib/             # Helper utilities
└── server/              # REST API + WebSocket Backend
    └── src/
        ├── config/      # Database & third-party configs
        ├── controllers/ # Request handlers
        ├── middlewares/ # Security & validation filters
        ├── models/      # MongoDB Schemas
        ├── routes/      # API Endpoints
        └── sockets/     # Real-time events
```

## ⚙️ Prerequisites

*   **Node.js** 20+
*   **MongoDB** Atlas account (or a local MongoDB instance)
*   **Cloudinary** account for profile and portfolio image uploads *(Optional)*
*   **SMTP Service** for password recovery emails *(Optional)*

## 🔧 Environment Configuration

1. Navigate to the backend directory: `cd server`
2. Duplicate the environment template: `cp .env.example .env`
3. Populate your `.env` file with the required credentials:

```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_strong_production_secret
CLIENT_URL=http://localhost:3000
CLOUDINARY_URL=your_cloudinary_credentials
SMTP_HOST=your_smtp_host
```

## 💻 Getting Started

### Development Mode
Open two separate terminals and execute the following commands:

**Terminal 1 (Backend):**
```bash
cd server
npm run dev
```

**Terminal 2 (Frontend):**
```bash
cd client
npm run dev
```

### Production Build
To build and run the application for a production environment:

**Frontend:**
```bash
cd client
npm run build
npm start
```

**Backend:**
```bash
cd server
npm start
```
