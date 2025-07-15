# 📋 Vue Job Board
A simple web app built to explore and practice Vue.js fundamentals. <br />
This project mocks a job platform for managing Vue-related job postings. Users can: <br />

- ✅ View job listings
- ✅ Add new jobs
- ✅ Edit existing jobs
- ✅ Delete jobs

It uses a ```jobs.json``` file served by **json-server** to simulate a backend API. Styling is done with **Tailwind CSS**, and **Vite** is used as the frontend build tool for fast development.

---

## ⚙️ Tech Stack
- **Vue 3** - Frontend framework
- **Vite** - Build tool for modern frontend development
- **Tailwind CSS** - Utility-first CSS framework for styling
- **Axios** - HTTP client to communicate with API
- **Vue Toastification** - Toast notifications

---

## 📁 Project Structure

```
/src
├── assets
│   ├── img/
│   │   └── logo.png
│   └── main.css
├── components
│   ├── BackButton.vue
│   ├── Card.vue
│   ├── Hero.vue
│   ├── HomeCard.vue
│   ├── JobListing.vue
│   ├── JobListings.vue
│   ├── Navbar.vue
├── Router
│   └── index.js
├── views
│   ├── AddView.vue
│   ├── EditView.vue
│   ├── HomeView.vue
│   ├── JobsView.vue
│   ├── JobView.vue
│   ├── NotFound.vue
├── App.vue
├── jobs.json
├── main.js
```

---

## 📦 Installation & Setup

**1. Clone the repository**
```bash
git clone https://github.com/jdavidIP/Vue-Job-Board.git
cd Vue-Job-Board
```

**2. Install dependencies**
```bash
npm install
```

**3. Run JSON Server (mock API)**
```bash
npm run server
```

**4. Start Development server**
```bash
npm run dev
```

The app will be running at http://localhost:3000.

---

## 🔥 Features
- 📄 View all jobs – Browse Vue-related job postings
- ➕ Add jobs – Create new job entries
- ✏️ Edit jobs – Modify existing job details
- ❌ Delete jobs – Remove job postings with confirmation
- 🍞 Toast notifications – Feedback on user actions
- 💅 Responsive UI – Clean design with Tailwind CSS

---

## 🌐 API Mocking
This project uses [JSON Server](https://github.com/typicode/json-server.git) to serve data from ```src/jobs.json```. All API calls are proxied through ```/api``` (configured in ```vite.config.js```):
```js
server: {
  port: 3000,
  proxy: {
    "/api": {
      target: "http://localhost:5000",
      changeOrigin: true,
      rewrite: (path) => path.replace(/^\/api/, ""),
    },
  },
},
```

Example API endpoint to get all job postings:
```bash
GET /api/jobs
```

---

## 📖 Learnings
This project was created to practice:
- ✅ Vue 3 Composition API
- ✅ Vue Router (nested routes, dynamic params, 404 handling)
- ✅ State management with reactive and ref
- ✅ API integration with Axios
- ✅ Tailwind for rapid styling
- ✅ Mocking REST APIs with JSON Server

---

## 🧑‍💻 Author

**Jose Ibanez**

[My GitHub](https://github.com/jdavidIP)

[My LinkedIn](https://www.linkedin.com/in/jose-ibanez-polo-622314253/)
