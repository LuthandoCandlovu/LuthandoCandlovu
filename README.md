# 🌟 SkyWatch Africa (MVP)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.109-green.svg)

A simple citizen-science astronomy app where users can:
- Submit sky observations (type, description, location, time)
- View all reports on a live interactive map
- Browse recent observations in real-time

Reports are saved to SQLite and displayed on a web page with map + list. This is an **MVP** you can push to GitHub and improve later (photo upload + AI detection coming next).

---

## ⚙️ Requirements

- **Python 3.10+** (3.11 is perfect)
- **VS Code** (recommended)
- **Git** for pushing to GitHub

---

## 🚀 Setup & Run

### 1️⃣ Run the Backend (FastAPI)

Open terminal in the project folder:

```bash
cd backend
python -m venv venv

# Windows:
venv\Scripts\activate

# Mac/Linux:
source venv/bin/activate

pip install -r requirements.txt
uvicorn app.main:app --reload
```

**Backend URLs:**
- API: http://127.0.0.1:8000
- Docs: http://127.0.0.1:8000/docs
- Health: http://127.0.0.1:8000/health

A SQLite file `skywatch.db` will be created inside `backend/`.

### 2️⃣ Run the Frontend

**Option A** (easy): Open `frontend/index.html` in your browser.

**Option B** (recommended): Use VS Code extension **Live Server**
- Right-click `frontend/index.html` → **Open with Live Server**

---

## 🧪 Test It

1. ✅ Start backend
2. ✅ Open frontend
3. ✅ Click **"Use my GPS"** (or type latitude/longitude)
4. ✅ Fill in observation details
5. ✅ Click **"Submit report"**
6. ✅ You'll see it on the map and in the list!

---

## 📤 Push to GitHub

In the project root:

```bash
git init
git add .
git commit -m "SkyWatch Africa MVP: reports + map"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/skywatch-africa.git
git push -u origin main
```

> **Need help with GitHub?** See [GITHUB_SETUP.md](GITHUB_SETUP.md) for detailed instructions.

---

## 🔮 Next Upgrades (Research-Level Features)

To make this a professional research platform, add:

- [ ] **Photo/video upload** (FastAPI `UploadFile`)
- [ ] **Validation** (cloud/blur/dark checks)
- [ ] **Simple ML detection/classification**
- [ ] **Export endpoint**: `/reports.csv` for researchers
- [ ] **User accounts + moderation**
- [ ] **Data quality metrics**
- [ ] **API authentication**
- [ ] **Mobile apps**

---

## 📁 Project Structure

```
skywatch-africa/
├── backend/
│   ├── app/
│   │   ├── main.py          # FastAPI app & endpoints
│   │   ├── database.py      # SQLAlchemy models
│   │   └── schemas.py       # Pydantic validation
│   ├── requirements.txt
│   └── skywatch.db          # Created automatically
├── frontend/
│   ├── index.html           # Main page
│   ├── css/style.css        # Styling
│   └── js/app.js            # Frontend logic
├── README.md
└── LICENSE
```

---

## 🛠️ Tech Stack

**Backend:**
- FastAPI (Python web framework)
- SQLAlchemy (ORM)
- SQLite (Database)
- Uvicorn (ASGI server)

**Frontend:**
- HTML5/CSS3/JavaScript
- Leaflet.js (Interactive maps)
- OpenStreetMap tiles

---

## 🐛 Troubleshooting

**Backend won't start?**
```bash
cd backend
pip install -r requirements.txt --upgrade
```

**Frontend can't connect?**
- Ensure backend is running at http://127.0.0.1:8000
- Check browser console (F12) for errors

**GPS not working?**
- Use HTTPS or localhost
- Grant browser location permissions

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file.

---

## 🤝 Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## ⭐ Show Your Support

Give a ⭐ if this project helped you!

---

*Built with ❤️ for citizen scientists across Africa* 🌍✨

