# 📚 Wikipedia Metadata DB

This project helps us collect and explore **metadata** from **Wikipedia**, **Wikimedia**, and **Wikibooks**. Users can search through the collection and save their favorite articles, images, or books into custom collections.

It’s built to be **simple**, **clean**, and easy to grow.

---

## 🧠 What It Does

- 📡 Pulls data from Wikipedia/Wikimedia APIs
- 🗃️ Saves useful metadata in a local database (like titles, authors, categories)
- 🔍 Lets users search, filter, and view that metadata in a web interface
- 🧺 Allows people to create their own collections of assets
- 🔄 Keeps the database up-to-date with scheduled updates

---

## 📁 Folder Structure

```txt
wikipedia-metadata-db/
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── models.py
│   │   ├── schemas.py
│   │   ├── crud.py
│   │   ├── database.py
│   │   ├── fetcher.py
│   │   └── routes/
│   │       ├── assets.py
│   │       └── collections.py
│   ├── .env
│   └── requirements.txt
│
├── frontend/
│   └── src/
│       ├── App.tsx
│       ├── main.tsx
│       ├── pages/
│       ├── components/
│       └── services/
│           └── api.ts
│
├── scripts/
│   └── run_fetcher.py
│
├── .gitignore
└── README.md
```

---

## 🛠️ What Each File/Folder Does

### 🧩 `backend/`

- **`main.py`** – This is the starting point of the backend (runs the FastAPI app).
- **`models.py`** – Defines the shape of data we store in the database (like assets and collections).
- **`schemas.py`** – Handles what data goes in and out of the API (clean and validated).
- **`crud.py`** – Functions to read/write from the database.
- **`database.py`** – Connects to the PostgreSQL database.
- **`fetcher.py`** – Fetches metadata from Wikipedia/Wikimedia and updates our database.
- **`routes/`**
  - **`assets.py`** – API routes to list, filter, or view assets.
  - **`collections.py`** – API routes to create and manage user collections.
- **`.env`** – Stores our database connection string and secrets.
- **`requirements.txt`** – List of Python packages the backend needs.

---

### 🎨 `frontend/`

- **`main.tsx`** – The entry point for the React app.
- **`App.tsx`** – Sets up the overall layout of the app.
- **`pages/`** – Different views/pages like home, asset browser, or collections.
- **`components/`** – Reusable building blocks like buttons, cards, search bars, etc.
- **`services/api.ts`** – Makes calls to the backend API (like “get assets” or “add to collection”).

---

### ⚙️ `scripts/`

- **`run_fetcher.py`** – Lets us manually trigger a metadata update. Can also be scheduled with a cron job to run regularly.

---

## 🚀 How to Run It Locally

### 🐍 Backend (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### ⚛️ Frontend (React + Vite)

```bash
cd frontend
npm install
npm run dev
```

---

## 🧪 Example Use Cases

- Researchers creating curated knowledge sets
- Students organizing resources by subject
- App developers building learning or reading tools using open content

---

## 🤝 Want to Contribute?

Totally welcome! Just fork this repo, make a new branch, and submit a pull request. Even small suggestions or edits are helpful.

---

## 📬 Questions?

You can reach me at **kishore.reddy.allu@gmail.com** or open an issue on GitHub.

---
