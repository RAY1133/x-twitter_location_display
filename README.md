# X / Twitter Location Display

A Chrome extension that displays user location information from X/Twitter profiles directly in your timeline.

![X Location Display](https://img.shields.io/badge/version-1.2.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## Features

- 🌍 **Automatic Location Detection** - Shows user locations from their About section directly in timeline
- 🎨 **Native Design** - Clean badges that match X/Twitter's interface
- ⚡ **High Performance** - 24-hour caching with rate limiting
- 🌙 **Dark Mode Support** - Seamlessly works with X's dark theme
- 🔒 **Privacy-Focused** - All data stored locally, no external tracking
- 🛡️ **Security Hardened** - XSS protection and input validation

## Installation

### Option 1: From Chrome Web Store (Recommended)
*Coming soon - Link will be added once published*

### Option 2: Load Locally (Development/Testing)

#### Prerequisites
- Google Chrome browser (or any Chromium-based browser like Edge, Brave, etc.)
- Basic understanding of how to navigate files on your computer

#### Step-by-Step Installation:

1. **Download the Extension**
   - Click the green "Code" button at the top of this page
   - Select "Download ZIP"
   - Extract the ZIP file to a folder on your computer (e.g., `C:\Extensions\x-location-display` or `~/Extensions/x-location-display`)

2. **Open Chrome Extensions Page**
   - Open Google Chrome
   - Type `chrome://extensions/` in the address bar and press Enter
   - OR click the three-dot menu → More Tools → Extensions

3. **Enable Developer Mode**
   - Look for the "Developer mode" toggle in the top-right corner
   - Click it to turn it ON (it should turn blue)

4. **Load the Extension**
   - Click the "Load unpacked" button that appears after enabling Developer mode
   - Navigate to the folder where you extracted the extension files
   - Select the folder and click "Select Folder" or "Open"

5. **Verify Installation**
   - You should see "X / Twitter Location Display" appear in your extensions list
   - Make sure the toggle is ON (blue)
   - You should see the extension icon in your Chrome toolbar

6. **Test the Extension**
   - Go to [X.com/Twitter](https://x.com)
   - Click the extension icon
   - Follow [@Rayomand14](https://x.com/Rayomand14) to unlock the extension
   - Wait 6 seconds, then click "Activate Extension"
   - Browse your timeline - location badges will appear next to usernames!

#### Troubleshooting Local Installation

**Extension not loading?**
- Make sure you selected the correct folder (the one containing `manifest.json`)
- Check that all files are present (manifest.json, content.js, background.js, etc.)

**Not seeing location badges?**
- Make sure you completed the follow + activation steps in the popup
- Try refreshing the X.com page
- Check the browser console (F12) for any errors

**Extension disappeared after Chrome restart?**
- This is normal for unpacked extensions
- Go back to `chrome://extensions/` and make sure it's still enabled
- You may need to reload it by clicking the refresh icon

## How It Works

1. **Install** the extension using one of the methods above
2. **Activate** by following [@Rayomand14](https://x.com/Rayomand14) (supports development!)
3. **Browse** X/Twitter normally - location badges appear automatically next to usernames

The extension intercepts X's GraphQL API responses and displays publicly available location data from user profiles without requiring additional API calls.

## Privacy

- ✅ Only displays publicly available information from user profiles
- ✅ All location data is cached locally in your browser
- ✅ No data is sent to external servers
- ✅ No tracking or analytics
- ✅ Open source and auditable

## Permissions

- **storage**: Cache location data locally for better performance
- **host_permissions (x.com, twitter.com)**: Access X's API to retrieve location information

## Technical Details

**Built with:**
- Manifest V3
- Vanilla JavaScript (no dependencies)
- Chrome Extension APIs

**Architecture:**
- Content script runs in MAIN world to intercept fetch requests
- Rate limiting (max 5 concurrent requests)
- Duplicate request prevention
- Safe DOM manipulation with XSS protection

## Development

The codebase is clean and well-documented:

```
manifest.json    # Extension configuration
content.js       # Main functionality (fetch interception, badge injection)
background.js    # Background service worker (unused, for future features)
popup.html/js    # Extension popup UI with follow gate
styles.css       # Location badge styling
```

## Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## Support Development

If you find this extension useful, consider:
- ⭐ Starring this repository
- 🐦 Following [@Rayomand14](https://x.com/Rayomand14)
- 🐛 Reporting issues or suggesting improvements

## License

MIT License - Feel free to use and modify as needed.

## Version History

**v1.2.0** (Current)
- Initial public release
- Follow gate implementation
- Full error handling and security hardening
- Clean, production-ready code

## Author

Created by [@Rayomand14](https://x.com/Rayomand14)

---

**Note:** This extension is not affiliated with or endorsed by X Corp or Twitter, Inc.
