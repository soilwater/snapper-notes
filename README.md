# 🦎 Snapper - Field Data Collection PWA

A modern, minimalist Progressive Web App for field data collection. Perfect for farmers, crop scouts, researchers, and agricultural consultants.

## ✨ Features

- **📸 Photo Capture** - Take photos directly from your device camera
- **📝 Comments** - Add field notes and observations
- **📍 GPS Location** - Automatically capture location data
- **🕐 Timestamp** - Auto-record when each capture was taken
- **🏷️ Keywords** - Add up to 3 hashtag-style keywords per capture
- **💾 Local Storage** - All data stored on your device (no server required)
- **📥 Export Options** - Download individual images with metadata or export all data as CSV
- **🔄 Offline First** - Works without internet connection
- **📱 Installable** - Can be installed as an app on mobile devices

## 🚀 Quick Start

### Installation

1. **Option A: Direct Use**
   - Open `snapper.html` in any modern web browser
   - That's it! No build process, no dependencies

2. **Option B: Install as PWA (Mobile)**
   - Open `snapper.html` in your mobile browser
   - Tap the "Add to Home Screen" button
   - Launch from your home screen like a native app

3. **Option C: Local Server (for development)**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Or using Node.js
   npx serve
   
   # Then visit: http://localhost:8000/snapper.html
   ```

## 📖 How to Use

### Capturing Data

1. **Take a Photo**
   - Click the "Take Photo" button
   - Use your device camera to capture the field condition
   - Photo is automatically processed

2. **Add Details**
   - The app automatically captures GPS location and timestamp
   - Add your field observations in the comment box
   - Add up to 3 keywords (type and press Enter)
   - Keywords are saved for future use

3. **Save**
   - Click "Save Capture" to store your data
   - All data is saved locally on your device

### Managing Captures

- **View All Captures** - Scroll through all your saved field data
- **Download Individual** - Download a single capture with embedded metadata
- **Download All** - Bulk download all captures as images
- **Export CSV** - Export all metadata to a spreadsheet-compatible CSV file
- **Delete** - Remove individual captures
- **Clear All** - Reset the app and remove all stored data

## 🎨 Design Philosophy

Snapper follows a modern, minimalist design approach with:

- **Natural Color Palette** - Greens and earth tones suited for agricultural use
- **Clean Typography** - DM Sans for readability, JetBrains Mono for data
- **Smooth Animations** - Delightful micro-interactions without distraction
- **Mobile-First** - Optimized for field use on smartphones
- **Zero Friction** - No login, no accounts, instant use

## 🔧 Technical Details

### Stack
- Pure HTML5, CSS3, and JavaScript
- No external dependencies or frameworks
- Progressive Web App (PWA) capable
- Service Worker for offline functionality

### Browser Storage
- Uses `localStorage` for data persistence
- Stores images as base64 data URIs
- Maximum storage varies by browser (~5-10MB typical)

### Location Services
- Uses browser Geolocation API
- Requires user permission
- Works offline if location services are enabled

### Privacy
- **100% Local** - All data stays on your device
- **No Server** - No data transmitted anywhere
- **No Tracking** - No analytics or tracking scripts
- **No Authentication** - No personal information collected

## 📊 Export Formats

### Individual Image Export
- JPEG image with embedded text metadata overlay
- Includes: photo, comment, timestamp, GPS, keywords
- Filename: `snapper_[timestamp].jpg`

### CSV Export
- Spreadsheet-compatible format
- Columns: ID, Timestamp, Latitude, Longitude, Comment, Keywords
- Filename: `snapper_export_[timestamp].csv`

## 🌾 Use Cases

### For Farmers
- Document crop health and growth stages
- Track irrigation and fertilizer applications
- Record pest or disease observations
- Share field conditions with consultants

### For Crop Scouts
- Standardize field inspections
- Create georeferenced field reports
- Track changes over time
- Generate data for analysis

### For Researchers
- Collect field trial data
- Document experimental plots
- Create visual records with metadata
- Export data for statistical analysis

## 🔒 Browser Support

- **Chrome/Edge** - Full support ✅
- **Safari** - Full support ✅
- **Firefox** - Full support ✅
- **Mobile Browsers** - Full support ✅

Requires:
- Modern browser with ES6 support
- Camera access (for photo capture)
- Geolocation API (for GPS)
- localStorage (for data storage)

## ⚡ Performance

- **Lightweight** - < 50KB total (HTML + CSS + JS)
- **Fast** - Renders in < 100ms
- **Offline** - Works without internet
- **No Build** - Direct deployment

## 🛠️ Customization

The app is built as a single HTML file for easy customization:

- **Colors** - Edit CSS variables in `:root`
- **Keywords** - Modify `commonKeywords` array in JavaScript
- **UI Text** - All text is in the HTML, easy to translate
- **Logo** - Replace SVG in header section

## 📱 Installation on Mobile

### iOS (Safari)
1. Open Snapper in Safari
2. Tap the Share button
3. Select "Add to Home Screen"
4. Tap "Add"

### Android (Chrome)
1. Open Snapper in Chrome
2. Tap the menu (three dots)
3. Select "Add to Home screen"
4. Tap "Add"

## 🤝 Workflow

```
Capture → Add Notes → Auto-GPS → Auto-Timestamp → Save
                                                      ↓
                                              Local Storage
                                                      ↓
                                    Download/Export → Share
```

**One Direction:** The app is designed for capturing and exporting data, not for re-importing. Once downloaded, share with consultants, upload to cloud storage, or import into other software.

## 💡 Tips

- **Grant Location Permission** - For accurate GPS data
- **Use in Good Light** - For best photo quality
- **Build Keyword Library** - Reuse keywords for consistency
- **Export Regularly** - Backup your data by exporting periodically
- **Clear Storage** - If device storage is low, export then clear old captures

## 🐛 Troubleshooting

**Location not working?**
- Check browser permissions for location access
- Ensure location services are enabled on device

**Photos not saving?**
- Check available storage space
- Browser localStorage might be full (5-10MB limit)

**App not installing?**
- Must be served over HTTPS (or localhost for testing)
- Check that manifest.json and sw.js are accessible

## 📄 License

Open source - use freely for personal or commercial projects.

## 🎯 Future Ideas

While keeping the app simple and dependency-free, potential enhancements:
- Multiple photo support per capture
- Offline map preview of locations
- Voice-to-text for comments
- Image compression options
- Dark mode
- Additional export formats (JSON, GeoJSON)

---

**Built with ❤️ for agricultural professionals**

Need help? The entire app is in one file - view the source to understand how it works!
