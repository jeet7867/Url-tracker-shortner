# Url-tracker-shortner
you can short url and track url click
# 🔗 URL Shortener & Click Tracker

A full-stack **URL Shortener Web Application** built with **React, Node.js, and MongoDB**.
It allows users to create short links and track detailed analytics such as **click count, referrer, and timestamps**.

---

## ✨ Features

* 🔗 **Shorten Long URLs** into clean, shareable links
* 📊 **Click Tracking** – record the number of times a link is visited
* ⏰ **Analytics Dashboard** – view time-based usage stats
* 🌍 **Referrer Logging** – track source websites or apps
* 📱 **Responsive UI** built with React + Tailwind (optional)
* ⚡ **REST API** to integrate URL shortening into other applications

---

## 🖥️ Tech Stack

* **Frontend:** React, Axios, TailwindCSS (or plain CSS)
* **Backend:** Node.js, Express.js
* **Database:** MongoDB (Mongoose ODM)
* **Other Tools:**

  * bcrypt / JWT for authentication (if user accounts enabled)
  * nanoid / shortid for generating short URLs

---

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/url-shortener-tracker.git
cd url-shortener-tracker
```

### 2. Backend Setup (Node + Express)

```bash
cd backend
npm install
```

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
BASE_URL=http://localhost:5000
```

Start backend server:

```bash
npm run dev
```

### 3. Frontend Setup (React)

```bash
cd frontend
npm install
npm start
```

---

## 📊 API Endpoints

### ➤ Shorten URL

`POST /api/shorten`

```json
{
  "originalUrl": "https://example.com/some/very/long/link"
}
```

**Response:**

```json
{
  "shortUrl": "http://localhost:5000/abc123",
  "clicks": 0
}
```

---

### ➤ Redirect to Original URL

`GET /:shortCode`

* Redirects user to original URL
* Increments click count

---

### ➤ Get Stats

`GET /api/stats/:shortCode`
**Response:**

```json
{
  "originalUrl": "https://example.com/some/very/long/link",
  "shortUrl": "http://localhost:5000/abc123",
  "clicks": 7,
  "logs": [
    { "timestamp": "2025-09-05T12:30:00Z", "referrer": "twitter.com" },
    { "timestamp": "2025-09-05T13:10:00Z", "referrer": "whatsapp" }
  ]
}
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to fork this repo and submit a PR.

----
