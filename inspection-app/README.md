# 🔍 Inspection App – Setup Guide

## Files
- `index.html` → Mobile Inspector App (Staff use cheyyum)
- `admin.html` → Admin Dashboard (edminsp.vercel.app/admin.html)
- `manifest.json` → PWA install support
- `vercel.json` → Vercel config

---

## Step 1: Firebase Setup (Free)

1. **firebase.google.com** → Go
2. "Get started" → Google account login
3. "Add project" → Project name: `inspection-app` → Continue
4. Google Analytics: OFF → Create project
5. Left menu → **Build** → **Firestore Database**
   - "Create database" → "Start in test mode" → Next → Done
6. Left menu → **Build** → **Storage**
   - "Get started" → "Start in test mode" → Done
7. Left menu → **Project Settings** (gear icon)
   - "Your apps" section → Web app `</>` icon click
   - App nickname: `inspection-web` → Register app
   - **Copy the firebaseConfig object** → Save it

---

## Step 2: Add Firebase Config

Both `index.html` and `admin.html` la idha replace pannum:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",           // ← உங்கள் key
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

---

## Step 3: Deploy to Vercel

### Option A: Drag & Drop (Easy!)
1. **vercel.com** → Sign up (GitHub account use pannum)
2. Dashboard → "Add New" → "Project"
3. "Browse" → This folder select pannum (3 files)
4. Deploy → Done!
5. URL கிடைக்கும்: `https://your-app.vercel.app`

### Option B: GitHub (Best)
1. GitHub la new repo create pannum
2. Files upload pannum
3. Vercel → "Import Git Repository"
4. Auto-deploy aaagum!

---

## Step 4: Admin Password Change

`admin.html` la line edit pannum:
```js
const ADMIN_USER = 'admin';      // ← Change username
const ADMIN_PASS = 'admin123';   // ← Change password
```

---

## URLs after Deploy:
- **Staff App**: `https://your-app.vercel.app/` (Mobile la open pannum)
- **Admin**: `https://your-app.vercel.app/admin.html`

## Android Install (PWA):
1. Chrome browser la Staff App URL open pannum
2. Address bar la "Install" button or menu → "Add to Home Screen"
3. App icon phone home screen la varum! ✅

---

## Admin Login Default:
- Username: `admin`
- Password: `admin123`
(Deploy panninaapuram change pannum!)
