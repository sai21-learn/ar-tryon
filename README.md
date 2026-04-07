# AR Watch Try-On - WebAR Project

A simple, elegant AR experience to visualize watches on your wrist in real-time using A-Frame and AR.js.

## 🎯 Features

✅ **Real-time AR Visualization** - See watches on your wrist instantly  
✅ **Color Variants** - Gold, Silver, Black, Rose Gold  
✅ **Size Adjustment** - Scale watch up/down with slider  
✅ **Rotation Control** - Rotate watch to see different angles  
✅ **Screenshot Capture** - Save and share your AR try-ons  
✅ **Mobile Optimized** - Works on any modern smartphone  
✅ **No Installation** - Pure HTML + CDN libraries  

## 📱 Requirements

- **Device**: Modern smartphone (iOS 12+, Android 8+)
- **Browser**: Chrome, Safari, Firefox, or Edge with WebAR support
- **Camera**: Phone camera with permission
- **HTTPS**: Required for WebAR (use Vercel for free hosting)

## 🚀 Quick Start

### Option 1: Local Testing (HTTP)
1. Save `ar-tryon-watch.html` to your computer
2. Open in browser: `file:///path/to/ar-tryon-watch.html`
3. Allow camera access when prompted
4. Position wrist in frame

### Option 2: Deploy to Vercel (Recommended)

```bash
# 1. Create a project folder
mkdir ar-tryon
cd ar-tryon

# 2. Create a vercel.json
cat > vercel.json << 'EOF'
{
  "buildCommand": "",
  "outputDirectory": "."
}
EOF

# 3. Deploy
vercel --prod
```

Or directly upload `ar-tryon-watch.html` to Vercel:
- Rename it to `index.html`
- Drag-drop to [vercel.com](https://vercel.com)
- Get instant HTTPS URL

### Option 3: GitHub + Vercel Auto-Deploy
```bash
# 1. Create repo
git init
git add ar-tryon-watch.html
git commit -m "Initial AR project"
git push origin main

# 2. Connect to Vercel (auto-deploys on push)
vercel --prod
```

## 🎮 How to Use

1. **Open on Mobile** - Use HTTPS URL on any smartphone
2. **Allow Camera** - Grant camera permission when prompted
3. **Position Wrist** - Hold wrist in center of screen
4. **Customize**:
   - **Color**: Select from dropdown (Gold, Silver, Black, Rose Gold)
   - **Size**: Use slider to scale watch larger/smaller
   - **Rotate**: Drag slider to spin watch around
5. **Capture**: Tap 📸 button to save screenshot

## 📂 File Structure

```
ar-tryon-watch.html      # Single file - entire project
```

That's it! No build process, no dependencies to install.

## 🔧 How It Works

### Architecture
```
Camera Feed
    ↓
A-Frame Scene + AR.js
    ↓
Hand Position Simulation
    ↓
Watch Entity Updates
    ↓
Color/Scale/Rotation Applied
    ↓
Screen Display + Capture
```

### Key Components

**A-Frame 3D Scene**
- Uses A-Frame for 3D rendering
- AR.js for WebAR marker-less detection
- Three.js under the hood

**Watch Model**
- Built with A-Frame primitives (cylinder + torus)
- Fully customizable colors and materials
- Real-time updates from UI controls

**Hand Tracking**
- Simulated hand position for MVP
- Can be upgraded to real pose detection with TensorFlow.js
- Smooth animations at 30fps

**UI Controls**
- Color picker dropdown
- Scale adjustment slider (0.8x - 1.5x)
- Rotation slider (0° - 360°)
- Screenshot capture button

## 🎨 Customization

### Change Watch Model
Replace the cylinder + torus with a glTF model:

```html
<a-entity id="watch" gltf-model="url(watch.glb)" ...></a-entity>
```

### Add More Products
Extend the control panel:

```html
<div class="control-group">
    <label for="productSelect">Product:</label>
    <select id="productSelect">
        <option value="watch">Watch</option>
        <option value="ring">Ring</option>
        <option value="sunglasses">Sunglasses</option>
    </select>
</div>
```

### Add Material Variants
```javascript
function updateWatchMaterial(material) {
    const watch = document.getElementById('watch-face');
    watch.setAttribute('material', `metalness: ${material.metalness}; roughness: ${material.roughness}`);
}
```

## 📊 Performance Tips

- Keep watch model under 50KB
- Use mobile-friendly polygon counts
- Limit hand tracking updates to 30fps
- Compress textures with TinyPNG
- Test on actual devices (not just desktop)

## 🐛 Troubleshooting

**"AR Not Supported"**
- Use a modern mobile device (iOS 12+, Android 8+)
- Ensure camera permission is granted
- Try different browser (Chrome usually works best)

**Camera not appearing**
- Check HTTPS (required for WebAR)
- Verify camera permissions in settings
- Restart browser

**Watch not visible**
- Adjust initial position in code (line ~185: `position="0 0 -0.5"`)
- Check console for errors (F12 → Console tab)
- Ensure device is well-lit

**Performance issues**
- Reduce watch model complexity
- Limit hand tracking frequency
- Close other browser tabs

## 📸 Next Steps

**To enhance this project:**
1. Replace cube watch with real 3D model from Sketchfab
2. Add real hand pose detection (TensorFlow.js)
3. Implement product catalog with API
4. Add QR code for sharing
5. Store user captures to gallery

## 🔗 Resources

- **A-Frame Docs**: https://aframe.io/docs/
- **AR.js Docs**: https://ar-js-org.github.io/AR.js-Docs/
- **Free 3D Models**: https://sketchfab.com
- **Three.js Docs**: https://threejs.org/docs/

## 📄 License

MIT - Use freely for personal & commercial projects

## 🚀 Deployment URLs

Once deployed, share with:
- Direct link: `https://your-domain.com`
- QR code (generate from link)
- Social media post
- Email to friends

---

**Built with ❤️ using A-Frame + AR.js**

Questions? Check browser console (F12) for helpful errors.
# ar-tryon
