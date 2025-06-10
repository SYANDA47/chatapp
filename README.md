
# 📱 Django Chat App

A simple real-time chat application built with Django and Django Channels, deployed on [Railway](https://railway.app/).

## 🚀 Live Demo
[https://chatapp-production-50ad.up.railway.app/](https://chatapp-production-50ad.up.railway.app/)

---

## 📌 Features

- User authentication (Signup/Login)
- Real-time chat using WebSockets
- Django Channels and Redis integration
- PostgreSQL database
- Deployed with Railway + Nixpacks

---

## 🧑‍💻 Tech Stack

- **Backend:** Django, Django REST Framework, Django Channels
- **WebSockets:** Redis + Channels
- **Database:** PostgreSQL (Railway)
- **Frontend:** HTML, CSS, Bootstrap, JS
- **Deployment:** Railway with Nixpacks

---

## ⚙️ Getting Started (Local Setup)

### 1. Clone the repo

```bash
git clone https://github.com/SYANDA47/chatapp.git
cd chatapp
```

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Setup the database

```bash
python manage.py migrate
```

### 5. Create a superuser

```bash
python manage.py createsuperuser
```

### 6. Run the development server

```bash
python manage.py runserver
```

---

## 🛠️ Deployment (Railway)

1. Connect the GitHub repo on [Railway](https://railway.app/)
2. Use **Nixpacks** as the builder.
3. Add a `Procfile`:

```bash
web: gunicorn chat_project.wsgi --log-file -
```

4. Add the following environment variables:
   - `SECRET_KEY`
   - `DEBUG=False`
   - `ALLOWED_HOSTS=chatapp-production-xxxxx.up.railway.app`
   - `CSRF_TRUSTED_ORIGINS=http://chatapp-production-xxxxx.up.railway.app,https://chatapp-production-xxxxx.up.railway.app`
   - `DATABASE_URL` (automatically provided by Railway Postgres plugin)

5. Enable Redis and link to your Django Channels settings.

---

## ✅ To-Do / Improvements

- [ ] Private chat rooms
- [ ] Chat history
- [ ] Media support (images/attachments)
- [ ] User status (online/offline)
- [ ] Responsive UI

---

## 👤 Author

**Shadrack Syanda Mutia**  
📧 [syandamutia@gmail.com](mailto:syandamutia@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/shadrackmutia) | [GitHub](https://github.com/SYANDA47)
