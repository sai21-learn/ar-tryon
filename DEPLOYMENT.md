# 🚀 Quick Deployment Guide

Deploy your AR Try-On app in **2 minutes** for FREE.

---

## Option 1: Upload to Vercel (Easiest)

### Step 1: Prepare Files
```bash
# Create a folder
mkdir ar-tryon
cd ar-tryon

# Rename your HTML file to index.html
cp ar-tryon-accessories.html index.html
```

### Step 2: Deploy
Go to **[vercel.com](https://vercel.com)** and:
1. Click **"Upload"** (no login needed first time)
2. Drag & drop your `index.html` file
3. Click **Deploy**
4. Get your live URL instantly (e.g., `https://ar-tryon-abc123.vercel.app`)

Done! ✅ Your app is LIVE.

---

## Option 2: Git + Auto-Deploy (Better)

### Step 1: Create GitHub Repo
```bash
# Initialize git in your project
cd ar-tryon
git init
git add index.html
git commit -m "Initial AR project"
git branch -M main

# Create repo on github.com, then:
git remote add origin https://github.com/YOUR_USERNAME/ar-tryon.git
git push -u origin main
```

### Step 2: Connect to Vercel
1. Go to [vercel.com](https://vercel.com)
2. Click **"Import Project"**
3. Paste your GitHub repo URL
4. Click **Import**
5. Wait 30 seconds...
6. Get your live URL

**Bonus**: Every time you push to GitHub, Vercel auto-deploys! 🚀

---

## Option 3: Vercel CLI (Pro)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd ar-tryon
vercel --prod

# Done! Live URL printed to console
```

---

## ✅ Testing on Mobile

1. Copy your Vercel URL (e.g., `https://ar-tryon-xyz.vercel.app`)
2. On your **phone**, open that URL in Chrome/Safari
3. Grant camera permission
4. Position wrist in frame
5. Customize colors & size
6. Tap **📸 Capture** to save

---

## 🎯 Hackathon Checklist

- [ ] Code pushed to GitHub
- [ ] Deployed to Vercel (HTTPS required)
- [ ] Works on mobile (tested on real device)
- [ ] Screenshot/video saved
- [ ] Share link ready
- [ ] README updated with your info

---

## 📊 Demo Link Format

Share this way:
```
🎨 AR Watch Try-On - Try it on your wrist!
https://ar-tryon-xyz.vercel.app

Position your wrist in the camera frame to see watches in AR.
Change colors, size, and rotation using controls at the bottom.
```

---

## 🔗 Share Everywhere

- **Twitter/X**: Tweet the link with #AR #WebAR
- **LinkedIn**: Post to your network
- **GitHub**: Add to your portfolio
- **Discord**: Share in hackathon server
- **QR Code**: Generate from [qr-server.com](https://qr-server.com/api/qr?size=200x200&data=YOUR_URL)

---

## 🆘 Troubleshooting Deployment

**"HTTPS required for WebAR"**
→ Vercel automatically gives you HTTPS ✅

**"Camera not working"**
→ Make sure you're on the HTTPS URL, not HTTP

**"Page not loading"**
→ Wait 60 seconds for Vercel to finish deploying
→ Hard refresh (Ctrl+Shift+R on desktop, refresh on mobile)

---

## 💡 Pro Tips

1. **Custom Domain** (Optional)
   - Go to Vercel project settings
   - Add your domain (e.g., ar-tryon.yourdomain.com)
   - Free HTTPS included

2. **Add to Home Screen** (Mobile)
   - Tap share → "Add to Home Screen"
   - Creates native app-like icon

3. **Analytics** (Optional)
   - Vercel shows basic analytics automatically
   - See visitors, countries, browsers

4. **Environment Variables**
   - Add API keys in Vercel settings if needed
   - Useful for future product catalog API

---

## 📈 Next: Make it Better

After deployment:
- Add real 3D models from Sketchfab
- Connect to e-commerce API
- Add product catalog
- Implement real hand pose detection
- Save user captures to database

---

**You're ready! Deploy now and share your AR app! 🎉**
