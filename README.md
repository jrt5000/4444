# Four444 Offline PWA 📱

Your habit tracking app with **full offline functionality** for iPhone!

## 📦 What's Included

- **index.html** - Your complete habit tracker (identical functionality)
- **service-worker.js** - Caches all resources for offline use
- **manifest.json** - PWA configuration for installation

## 🚀 Quick Start

### Option 1: GitHub Pages (Recommended - Free & Easy!)

1. **Create a new repository** on GitHub
2. **Upload all 3 files** (index.html, service-worker.js, manifest.json)
3. **Enable GitHub Pages**:
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: main
   - Click Save
4. **Access your URL** (usually `https://yourusername.github.io/repo-name`)
5. **On iPhone**:
   - Open the URL in Safari
   - Tap the Share button (square with arrow)
   - Select "Add to Home Screen"
   - Name it and tap "Add"

✅ **Done!** Your app now works offline!

### Option 2: Other Free Hosting

**Netlify:**
1. Drag & drop the folder at [netlify.com/drop](https://netlify.com/drop)
2. Get instant URL
3. Add to iPhone home screen

**Vercel:**
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the folder
3. Follow prompts
4. Add to iPhone home screen

### Option 3: Local Testing

```bash
# Using Python (built into Mac/Linux)
python3 -m http.server 8000

# Or using Node.js
npx http-server

# Or using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser

## 🧪 Testing Offline Mode

1. **First visit** (with internet):
   - Open the app
   - Check browser console for: "✅ Service Worker registered successfully"
   - Wait a few seconds for caching to complete

2. **Go offline**:
   - Enable Airplane Mode on iPhone
   - Or disconnect WiFi/cellular data
   - Or use browser DevTools → Network → Offline

3. **Refresh the page**:
   - The app still loads! 🎉
   - All your data is there (stored in localStorage)
   - Everything works perfectly offline

## 🔧 How It Works

### First Visit (Online):
1. Service worker installs
2. Caches React, ReactDOM, Babel, and Tailwind CSS
3. Caches the HTML and manifest

### Subsequent Visits (Offline):
1. Service worker intercepts all requests
2. Serves cached resources instantly
3. Your habit data is already in localStorage
4. Result: **100% offline functionality!**

## ⚙️ Technical Details

### Why These Files?

- **index.html**: Your app (identical to original, just added service worker registration)
- **service-worker.js**: Required separate file (can't be inline due to security)
- **manifest.json**: Makes the app installable and provides app metadata

### Why It Needs a Server

Service workers have security requirements:
- Must be served over HTTPS (or localhost for testing)
- Can't run from `file://` URLs (double-clicking the HTML won't work)
- Must be in a proper web context

### What Gets Cached

```javascript
- The HTML file (your app)
- React (18)
- ReactDOM (18)
- Babel (for JSX transformation)
- Tailwind CSS (for styling)
```

### Your Data

Your habit tracking data was **already offline**:
- Stored in browser's localStorage
- Never sent to any server
- Persists across browser sessions
- Works offline automatically

The service worker adds offline support for the **libraries** (React, etc.)

## 🎯 Features

✅ **Full Offline Mode** - Works without internet after first load  
✅ **Installable** - Add to home screen like a native app  
✅ **Fast Loading** - Cached resources load instantly  
✅ **Data Persistence** - All your habits stored locally  
✅ **No Backend Needed** - Pure client-side app  
✅ **Privacy First** - Nothing leaves your device  

## 🐛 Troubleshooting

**Service Worker not registering?**
- Make sure you're accessing via HTTP/HTTPS (not file://)
- Check browser console for error messages
- Verify all 3 files are in the same directory
- Try hard refresh (Cmd+Shift+R or Ctrl+Shift+R)

**Not working offline?**
- Wait for "Service Worker registered" message
- Give it 5-10 seconds to cache on first visit
- Check Network tab in DevTools to see if resources cached
- Try refreshing once after first visit

**Cache not updating?**
- Change the version in service-worker.js: `CACHE_NAME = 'four444-offline-v2'`
- Or unregister service worker in DevTools → Application → Service Workers

## 📱 iPhone Specific

**Adding to Home Screen:**
1. Open in Safari (not Chrome/Firefox)
2. Tap Share button
3. Scroll down and tap "Add to Home Screen"
4. Edit name if desired
5. Tap "Add"

**Looks like a native app:**
- No browser chrome
- Full screen experience
- Custom app icon
- Smooth animations
- Offline support

## 🔒 Privacy & Security

- **No tracking** - Zero analytics or telemetry
- **No accounts** - No login required
- **No servers** - Data never leaves your device
- **Open source** - All code visible in the files
- **Local storage** - Everything stays on your iPhone

## 📚 Resources

- [MDN: Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)
- [Web.dev: PWA](https://web.dev/progressive-web-apps/)
- [Apple: iOS Web App](https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

---

**Made with ❤️ for offline-first habit tracking**

Need help? Check the browser console for detailed logging from the service worker.
