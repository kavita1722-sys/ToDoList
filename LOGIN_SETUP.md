# To Do Manager - Login Setup Guide

## ✅ Login Page Created!

Your authentication system is now ready! Here's how to set it up and use it:

### 1. **Create a Superuser (Admin Account)**

Run this command in your terminal:
```bash
python manage.py createsuperuser
```

You'll be prompted to enter:
- Username (e.g., `admin`)
- Email (e.g., `admin@example.com`)
- Password (enter a secure password)

### 2. **Create Regular Users**

You can create users in two ways:

#### Option A: Via Django Admin Panel
1. Go to `http://localhost:8000/admin/`
2. Log in with your superuser credentials
3. Click on "Users" 
4. Click "Add User"
5. Enter username and password
6. Save

#### Option B: Via Python Shell
```bash
python manage.py shell
```

Then in the shell:
```python
from django.contrib.auth.models import User
User.objects.create_user(username='john', password='john123')
User.objects.create_user(username='jane', password='jane123')
```

### 3. **Test the Login**

1. Open `http://localhost:8000/` or `http://localhost:8000/login/`
2. Enter your username and password
3. Click "🔓 Login"
4. You'll be redirected to the home page
5. Your username will appear in the top navigation
6. Click "Logout" to exit

### 4. **Features**

✅ **Authentication Required For:**
- Home page (Dashboard)
- Tasks page
- Add Task page
- Users page

✅ **Public Pages:**
- Login page (accessible to everyone)

✅ **Navigation Shows:**
- When logged in: Home, Tasks, Users, Username, Logout
- When logged out: Login link only

### 5. **Admin Panel**

Access the full Django admin at: `http://localhost:8000/admin/`

Here you can:
- Manage users
- Create categories
- Create tags
- Manage tasks
- View todo lists

## 🎨 Login Page Design

The login page features:
- Beautiful gradient background
- Smooth animations
- Responsive design (works on mobile & desktop)
- Error/success messages
- Demo credentials display
- Professional UI with emojis

## 📱 Responsive Design

The login page is fully responsive and works great on:
- Desktop (1920px+)
- Tablets (768px - 1024px)
- Mobile (320px - 767px)

## Notes

- Passwords are securely hashed
- Session timeout can be configured
- Users are protected by Django's CSRF protection
- All sensitive operations require login

Enjoy managing your tasks! 🎉
