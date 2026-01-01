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


## 🐾 Credits

Made with ❤️ for dog lovers everywhere.

---

**Disclaimer:** This app provides general guidance only. Always consult your veterinarian for specific dietary advice for your pet.
