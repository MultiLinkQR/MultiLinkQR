# 🚀 Multi QR Manager - Quick Guide

## ⚡ Get Started in 2 Minutes

### 1. Open the App
- **Option A**: Double-click `admin.html` → Enter password → Access dashboard
- **Option B**: Double-click `edit.html` → Create user profile directly (no login needed)

### 2. Add a User
- **From Dashboard**: Click "➕ Add New User" (requires login)
- **Direct Access**: Open `edit.html` directly (no login needed)
- Fill in username, full name, and social links
- Click "💾 Save User"
- Copy the JSON that appears
- Open `data/clients.json` and add the JSON to the array
- Save the file

### 3. Test It
- Refresh the dashboard
- Click "📱 Show QR" on your user
- Download the QR code (PNG or SVG)
- Scan with phone - it works!

## 🔐 Security Features
- **Public Profile Creation**: Anyone can create profiles via `edit.html`
- **Protected Dashboard**: Password required for management features
- **Password Protection**: Admin dashboard secured with password
- **User Isolation**: Each profile needs unique username+code
- **Session Timeout**: Auto-logout after 24 hours

## 🌐 Deploy Online (Optional)

### GitHub Pages:
1. **Update login credentials** in `credentials/login_credentials.json`:
   ```json
   [
     {
       "username": "admin",
       "password": "YourSecurePassword123!",
       "role": "main_admin",
       "isActive": true
     }
   ]
   ```

2. Update `script.js` line 5:
   ```javascript
   baseUrl: 'https://YOUR-USERNAME.github.io/YOUR-REPO/'
   ```

3. Push to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```

4. Enable GitHub Pages:
   - Go to repo Settings → Pages
   - Source: Deploy from branch
   - Branch: main → / (root) → Save

5. Wait 2 minutes, visit your URL!

### Production Deployment:
- **Netlify/Vercel**: Better for production (private repos, env vars)
- **Enable HTTPS**: Always use SSL certificates
- **Login Credentials**: Manage admin accounts via `credentials/login_credentials.json`

## 🔑 Key Features

- **Multiple users** with same username allowed
- **Unique codes** for each user (auto-generated)
- **50+ platforms** supported - see [PLATFORMS.md](PLATFORMS.md)
- **Secure profiles** - need code to access
- **Download QR** as PNG or SVG
- **Mobile friendly** design
- **Admin authentication** with password protection

## 📝 Important Files

- `admin.html` - **Admin login (for dashboard access)**
- `index.html` - Dashboard (protected - requires login)
- `edit.html` - **Add/edit users (public access - no login needed)**
- `user.html` - Public profiles (QR access only)
- `data/clients.json` - Main user database
- `data/personal.json` - Personal user accounts
- `credentials/login_credentials.json` - Admin login accounts

## 🐛 Quick Fixes

- **Can't login?** Check credentials in `credentials/login_credentials.json`
- **Need to add user?** Use `edit.html` directly (no login needed)
- **QR not working?** Check `data/clients.json` has the user
- **Can't see user?** Refresh dashboard (Ctrl+Shift+R)
- **Access denied?** URL needs both username and code
- **Can't access?** Check credentials in `credentials/login_credentials.json` or clear browser storage

## 🎯 That's It!

Your Multi QR Manager is ready! Create digital business cards for your customers.

---

## 🔗 Navigation

**🚀 [QUICK_GUIDE.md](QUICK_GUIDE.md)** | **🌐 [PLATFORMS.md](PLATFORMS.md)** | **🏠 [../README.md](../README.md)**

**Need help?** Check the main README.md file.
