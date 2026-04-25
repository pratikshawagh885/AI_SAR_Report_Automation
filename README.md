# ⚡ SAR Nexus v5 — Compliance + Banking Platform

## 🚀 Run in 3 Commands

```bash
cd SAR_Nexus_v5/frontend
npm install
npm start
```
Opens → **http://localhost:3000**  ·  Node.js 16+ required

---

## 🔑 Login Credentials

| Role  | Email             | Password   |
|-------|-------------------|------------|
| Admin | admin@sar.io      | admin123   |
| User  | *(created by admin)* | *(set by admin)* |

> **First time?** Log in as Admin → go to Users tab → Add New User → copy the email/password → log in as that user.

---

## 🗺️ How It Works

```
Admin logs in                  User logs in
     │                              │
     ▼                              ▼
Admin Dashboard              User Dashboard
 ├─ Dashboard (pending txns)   ├─ Overview (balance, charts)
 ├─ Users (add/remove)         ├─ Transactions (history)
 ├─ Transactions (all)         └─ Analytics (monthly trends)
 ├─ Analysis (monthly charts)
 ├─ SAR Reports                    │
 └─ Audit Log              Transfer Page
                            ├─ Step 1: Recipient
                            ├─ Step 2: Amount + Type
                            └─ Step 3: PIN confirm (1234)
                                      │
                                      ▼
                             Admin sees it instantly
                             → Approve / Reject / Flag SAR
```

---

## ✨ Features

**Admin Panel**
- ➕ Add users with name, email, password, phone
- 🗑 Remove users
- ⏳ Review pending transactions → **Approve**, **Reject** (auto-refunds), or **Flag as SAR**
- 📊 Monthly volume, approval/rejection charts, per-user analysis
- 📋 SAR reports with approve, reject, file on-chain
- 📜 Full audit log of every action

**User Portal**
- 💰 Balance card with live updates
- 💸 3-step transfer wizard (Account / Bank / Phone)
- 📊 Monthly analytics charts
- 📋 Transaction history with status (Pending / Approved / Rejected)
- 🔄 Balance auto-refunded when admin rejects

**All data persists** in browser localStorage — no backend needed.

---

## 🛠 Project Structure

```
SAR_Nexus_v5/
└── frontend/
    ├── public/index.html
    └── src/
        ├── App.jsx                  ← Routing (admin/user guards)
        ├── context/AuthContext.jsx  ← Login + dynamic user management
        ├── data/store.js            ← All state + DB operations
        └── pages/
            ├── Login.jsx            ← Admin / User login
            ├── AdminDashboard.jsx   ← Full admin panel (6 tabs)
            ├── UserDashboard.jsx    ← User banking (3 tabs)
            └── TransferPage.jsx     ← Money transfer wizard
```
