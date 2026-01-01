# 🐕 SniffSnax

**Can My Dog Eat This?** — Instant pet food safety checker

A Progressive Web App (PWA) that helps dog owners quickly check if foods are safe, need caution, or are toxic for their furry friends.

![SniffSnax](icons/icon.svg)

## ✨ Features

- 🔍 **Instant Search** — Search 200+ foods instantly
- ✅ **Clear Results** — Safe, Caution, or Toxic with explanations
- 🐕 **Multiple Dog Profiles** — Add up to 5 dogs with different needs
- 📏 **Personalized Portions** — Based on your dog's weight
- 💡 **Smart Tips** — Considers age, health conditions, allergies
- 📱 **Works Offline** — No internet needed after first load
- 📲 **Installable** — Add to home screen like a native app

## 🚀 Quick Deploy

### Option 1: Vercel (Recommended)
```bash
npm i -g vercel
cd sniffsnax
vercel
```

### Option 2: Netlify
1. Drag & drop the `sniffsnax` folder to [netlify.com/drop](https://netlify.com/drop)
2. Done! Get your URL instantly

### Option 3: GitHub Pages
1. Create a new repo on GitHub
2. Upload all files
3. Go to Settings → Pages → Deploy from main branch

### Option 4: Any Static Host
Upload these files to any static hosting:
- `index.html`
- `manifest.json`
- `service-worker.js`
- `icons/` folder

## 📁 File Structure

```
sniffsnax/
├── index.html          # Main app (HTML + React)
├── manifest.json       # PWA manifest
├── service-worker.js   # Offline caching
├── icons/
│   ├── icon.svg        # Source icon
│   ├── icon-72.png     # Generate these
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-180.png    # Apple touch icon
│   ├── icon-192.png
│   ├── icon-384.png
│   └── icon-512.png
└── README.md
```

## 🎨 Generate App Icons

You need PNG icons for the PWA to work properly. Use the included `icon.svg` to generate them:

### Option 1: Online Tool
1. Go to [realfavicongenerator.net](https://realfavicongenerator.net)
2. Upload `icons/icon.svg`
3. Download the generated icons
4. Place them in the `icons/` folder

### Option 2: Using ImageMagick
```bash
# Install ImageMagick first
brew install imagemagick  # macOS
apt install imagemagick   # Ubuntu

# Generate all sizes
for size in 72 96 128 144 152 180 192 384 512; do
  convert icons/icon.svg -resize ${size}x${size} icons/icon-${size}.png
done
```

### Option 3: Using Sharp (Node.js)
```bash
npm install sharp
```
```javascript
const sharp = require('sharp');
const sizes = [72, 96, 128, 144, 152, 180, 192, 384, 512];

sizes.forEach(size => {
  sharp('icons/icon.svg')
    .resize(size, size)
    .png()
    .toFile(`icons/icon-${size}.png`);
});
```

## 📱 Install as App

### iOS (Safari)
1. Open the deployed URL in Safari
2. Tap Share button
3. Tap "Add to Home Screen"
4. Tap "Add"

### Android (Chrome)
1. Open the deployed URL in Chrome
2. Tap the menu (⋮)
3. Tap "Install app" or "Add to Home screen"
4. Tap "Install"

### Desktop (Chrome/Edge)
1. Open the deployed URL
2. Click the install icon in the address bar
3. Click "Install"

## 🛠️ Customization

### Add More Foods
Edit the `foodDatabase` array in `index.html`:

```javascript
{ 
  name: 'food name', 
  status: 'safe',  // 'safe', 'caution', or 'toxic'
  emoji: '🍎', 
  note: 'Description and tips',
  portion: 'Recommended amount',      // for safe foods
  warning: 'Warning message',         // for caution foods
  danger: 'Danger description',       // for toxic foods
  action: 'What to do if eaten'       // for toxic foods
}
```

### Change Theme Colors
Edit the `theme_color` in `manifest.json` and the Tailwind classes in `index.html`.

### Add More Considerations
Edit the `specialConsiderations` array in `index.html`.

## 🔒 Privacy

- **No data collection** — Everything stays on your device
- **No accounts** — No sign-up required
- **No tracking** — No analytics or cookies
- **Offline first** — Works without internet

## 📄 License

MIT License — Free to use, modify, and distribute.

## 🐾 Credits

Made with ❤️ for dog lovers everywhere.

---

**Disclaimer:** This app provides general guidance only. Always consult your veterinarian for specific dietary advice for your pet.
