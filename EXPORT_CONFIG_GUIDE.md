# Snapper Image Export Configuration Guide

## Quick Tuning Reference

The downloaded images include metadata below the photo. You can easily customize the appearance by editing the `EXPORT_CONFIG` object at the top of the JavaScript section (around line 850).

### Location in Code
Look for this section:
```javascript
// ====== IMAGE EXPORT CONFIGURATION ======
const EXPORT_CONFIG = {
    footerHeight: 220,
    backgroundColor: '#ffffff',
    // ... etc
};
```

### Configuration Options

#### Layout & Spacing
- **footerHeight** (220) - Total height of the metadata area in pixels
  - *Increase* if text is cramped or getting cut off
  - *Decrease* to make the footer more compact
  
- **lineSpacing** (28) - Vertical space between each line of text
  - *Increase* for more breathing room
  - *Decrease* for tighter layout
  
- **padding** (20) - Left and right margins
  - Controls how far text is from edges
  
- **labelWidth** (100) - Space reserved for labels (Timestamp:, Latitude:, etc.)
  - Adjust if labels and values don't align properly

#### Colors & Appearance
- **backgroundColor** - Footer background color
  - `'#ffffff'` - Pure white (current, clean)
  - `'#f5f5f5'` - Light gray (subtle)
  - `'#fafafa'` - Off-white (very subtle)
  - `'#000000'` - Black (for white text, change textColor too)
  
- **textColor** (`'#1a1a1a'`) - Main text color
  - Keep dark on light backgrounds
  - Use `'#ffffff'` if using dark background

- **showBorder** (true/false) - Show a line separating photo from metadata
  - `true` - Shows border (recommended)
  - `false` - No separator line
  
- **borderColor** (`'#e0e0e0'`) - Color of separator line
  
- **borderWidth** (2) - Thickness of separator line in pixels

#### Typography
- **fontSize** (18) - Base text size in pixels
  - *Increase* for more readable text (try 20, 22, 24)
  - *Decrease* for more compact layout (try 16, 14)
  - Recommended range: 14-24
  
- **fontFamily** (`'Inter'`) - Font to use
  - Current: `'Inter'` (clean, modern)
  - Alternative: `'Arial'` (universal compatibility)
  - Alternative: `'Helvetica'` (classic)
  - Alternative: `'JetBrains Mono'` (monospace, matches app)

### Example Configurations

#### Larger, More Readable
```javascript
const EXPORT_CONFIG = {
    footerHeight: 250,
    backgroundColor: '#ffffff',
    textColor: '#1a1a1a',
    fontSize: 22,
    fontFamily: 'Inter',
    lineSpacing: 32,
    padding: 25,
    labelWidth: 110,
    showBorder: true,
    borderColor: '#e0e0e0',
    borderWidth: 2
};
```

#### Compact Layout
```javascript
const EXPORT_CONFIG = {
    footerHeight: 180,
    backgroundColor: '#ffffff',
    textColor: '#1a1a1a',
    fontSize: 16,
    fontFamily: 'Inter',
    lineSpacing: 24,
    padding: 15,
    labelWidth: 90,
    showBorder: true,
    borderColor: '#e0e0e0',
    borderWidth: 1
};
```

#### Subtle Gray Background
```javascript
const EXPORT_CONFIG = {
    footerHeight: 220,
    backgroundColor: '#f5f5f5',  // Changed
    textColor: '#1a1a1a',
    fontSize: 18,
    fontFamily: 'Inter',
    lineSpacing: 28,
    padding: 20,
    labelWidth: 100,
    showBorder: true,
    borderColor: '#d0d0d0',      // Slightly darker border for contrast
    borderWidth: 2
};
```

#### Dark Footer (Bold Look)
```javascript
const EXPORT_CONFIG = {
    footerHeight: 220,
    backgroundColor: '#1a1a1a',  // Dark background
    textColor: '#ffffff',        // White text
    fontSize: 18,
    fontFamily: 'Inter',
    lineSpacing: 28,
    padding: 20,
    labelWidth: 100,
    showBorder: false,           // No border needed with dark background
    borderColor: '#e0e0e0',
    borderWidth: 2
};
```

#### Minimalist (No Border, Clean White)
```javascript
const EXPORT_CONFIG = {
    footerHeight: 200,
    backgroundColor: '#ffffff',
    textColor: '#1a1a1a',
    fontSize: 20,
    fontFamily: 'Inter',
    lineSpacing: 30,
    padding: 20,
    labelWidth: 100,
    showBorder: false,           // No separator line
    borderColor: '#e0e0e0',
    borderWidth: 0
};
```

### Testing Your Changes

1. Edit the `EXPORT_CONFIG` values in `snapper.html`
2. Save the file
3. Refresh the page in your browser
4. Take a test photo or use an existing capture
5. Click "Download" to see the result
6. Adjust values as needed and repeat

### Tips
- Start by adjusting one value at a time
- Test with different image sizes (portrait vs landscape)
- Make sure text doesn't overlap or get cut off
- Check readability on both mobile and desktop
- Consider how it looks when printed

### Current Default Settings
The app ships with:
- Clean white background
- 18px readable text
- Subtle border separator
- Balanced spacing
- Bold labels for easy scanning
