# 🔗 Multi QR Manager

Create digital business cards with QR codes. Perfect for business card services!

## ✨ **What It Does**

- 📱 **Generate QR codes** for customer profiles
- 👥 **Manage multiple users** from one dashboard
- 🎨 **Beautiful profiles** with social media links
- 🔐 **Secure access** with unique codes
- 📱 **Mobile friendly** design

## 🚀 **Quick Start**

### **Option A: Full Management (Admin)**
1. **Open `admin.html`** → Enter password → Access dashboard
2. **Click "➕ Add New User"** to create profiles
3. **Click "📱 Show QR"** to generate QR codes
4. **Download and print** for customers

### **Option B: Quick Profile Creation (Public)**
1. **Open `edit.html`** directly (no login needed)
2. **Fill in user details** and social links
3. **Save and get JSON** to add to database
4. **Generate QR codes** from dashboard

## 🔐 **Security Features**

- **Public Profile Creation:** Anyone can create profiles via `edit.html` (no login needed)
- **Protected Management:** Dashboard requires admin password
- **Session Management:** Auto-logout after 24 hours
- **User Isolation:** End users can only access their own profiles via QR codes
- **Input Protection:** XSS prevention and input sanitization
- **Multi-User Login:** Multiple admin accounts with role-based access

## 📚 **Documentation**

- **🚀 [docs/QUICK_GUIDE.md](docs/QUICK_GUIDE.md)** - Complete setup guide
- **🌐 [docs/PLATFORMS.md](docs/PLATFORMS.md)** - All 50+ supported platforms

## 📁 **Files**

- `admin.html` - **Admin login page (for dashboard access)**
- `index.html` - Dashboard (protected - requires login)
- `edit.html` - **Add/edit users (public access - no login needed)**
- `user.html` - Public user profiles (accessible via QR)
- `data/clients.json` - Main user database
- `data/personal.json` - Personal user accounts
- `credentials/login_credentials.json` - Admin login accounts

## ⚠️ **Important Security Notes**

1. **Update login credentials** in `credentials/login_credentials.json`
2. **Never share admin.html URL** with end users
3. **Only share QR codes** - they lead to secure user profiles
4. **Admin session expires** after 24 hours for security
5. **Multi-user access** - Multiple admin accounts with different permissions

## 🎯 **That's It!**

Simple, powerful, and ready to use!

---

## 🔗 **Navigation**

**🚀 [docs/QUICK_GUIDE.md](docs/QUICK_GUIDE.md)** | **🌐 [docs/PLATFORMS.md](docs/PLATFORMS.md)**

---

**Built with ❤️ for modern business QR services**