# Chrome Extension Installation Guide

## 🚀 Behavioral Authentication Chrome Extension

### Quick Installation (Developer Mode)

#### Step 1: Prepare Extension
The extension is ready to install from:
```
C:\AltairAI\DataMerge\behavior-authentication\chrome-extension\
```

#### Step 2: Open Chrome Extensions Page
1. Open Google Chrome
2. Navigate to: `chrome://extensions/`
3. Or click: **Menu (⋮)** → **Extensions** → **Manage Extensions**

#### Step 3: Enable Developer Mode
1. Toggle **Developer mode** switch in the top-right corner
2. This reveals additional options

#### Step 4: Load Extension
1. Click **"Load unpacked"** button
2. Navigate to: `C:\AltairAI\DataMerge\behavior-authentication\chrome-extension\`
3. Click **"Select Folder"**
4. Extension should now appear in your extensions list ✅

#### Step 5: Pin Extension (Optional)
1. Click the **Extensions** icon (puzzle piece) in Chrome toolbar
2. Find "Behavioral Auth"
3. Click the **pin** icon to keep it visible

---

## ⚙️ Initial Configuration

### First Run Setup
1. Click the extension icon
2. Configure settings:
   - ✅ **Enable Monitoring**: ON
   - 🎯 **Sensitivity**: Medium (recommended)
3. Click **"Train Baseline"** to establish your behavioral profile
   - Type naturally for 2-3 minutes
   - Move mouse normally
   - Extension learns your patterns

### Model Setup
The extension comes with pre-trained model thresholds from Altair AI:
- **Keystroke Model**: 70.5% accuracy (Generalized Linear Model)
- **Mouse Model**: 58.2% accuracy (Best Model from Altair AI Studio)

---

## 📊 Features Overview

### Real-Time Monitoring
- ⌨️ **Keystroke Dynamics**: Hold time, flight time, typing speed
- 🖱️ **Mouse Dynamics**: Speed, curvature, click patterns
- 🎯 **Anomaly Detection**: AI-powered pattern matching

### Security Levels
1. **Full Access** (Green)
   - Normal browsing
   - All features enabled

2. **Limited Access** (Orange)
   - Password fields blocked
   - Sensitive sites restricted
   - Banking/email protected

3. **Blocked** (Red)
   - Session terminated
   - All tabs closed
   - Browsing data cleared

### Security Alerts
When anomalies detected:
1. Browser freezes
2. Security alert modal appears
3. Choose response:
   - ✅ "Yes, it's me" → Full access restored
   - 👥 "Someone I know" → Limited access mode
   - ❌ "No, it's not me" → Block and terminate

---

## 🔧 Troubleshooting

### Extension Not Loading
**Error**: "Manifest file is missing or unreadable"
- **Fix**: Ensure `manifest.json` exists in extension folder
- Verify all files copied correctly

### No Behavioral Data Collected
**Issue**: Stats show 0 keystrokes/mouse events
- **Fix**: 
  - Refresh any open tabs
  - Extension needs page reload to inject content scripts
  - Check browser console for errors (F12 → Console)

### Models Not Loading
**Error**: Anomaly detection not working
- **Fix**: 
  - Verify `models/keystroke-threshold.json` exists
  - Check `models/mouse-threshold.json` exists
  - Both models are already configured (keystroke 70.5%, mouse 58.2%)

### Permissions Issues
**Error**: Extension can't access pages
- **Fix**: 
  - Check manifest permissions granted
  - Re-install extension if needed
  - Some pages (chrome://) are restricted by design

---

## 📝 Model Updates

### Updating Keystroke Model
Your current model from Altair AI (70.5% accuracy):
1. Export model from Altair AI Studio
2. Convert to JSON threshold format
3. Replace `models/keystroke-threshold.json`
4. Reload extension

### Updating Mouse Model
Mouse model is already configured (58.2% accuracy, trained October 28, 2025):
1. Model exported from Altair AI Studio ✅
2. Thresholds extracted and configured ✅
3. `models/mouse-threshold.json` ready ✅
4. If you retrain with new data:
   ```json
   {
     "modelInfo": {
       "accuracy": <your_accuracy>,
       "trainingDate": "<date>"
     },
     "features": { ... }
   }
   ```
4. Reload extension

---

## 🎯 Demo Preparation (Oct 29)

### Pre-Demo Checklist
- [ ] Extension installed and working
- [ ] Baseline training completed
- [ ] Test all 3 security scenarios:
  - [ ] Normal usage → Full access
  - [ ] Simulated anomaly → Limited access
  - [ ] "Not me" response → Blocked access
- [x] Mouse model exported ✅ (Completed October 28, 2025)
- [ ] Screenshots/screen recording prepared

### Demo Flow
1. **Show Extension Popup**
   - Display real-time stats
   - Show confidence score
   
2. **Demonstrate Normal Usage**
   - Type naturally
   - Show green status
   
3. **Trigger Anomaly**
   - Simulate unusual pattern
   - Show freeze + alert modal
   
4. **Security Responses**
   - Option 1: Full access restoration
   - Option 2: Limited access mode
   - Option 3: Session termination

---

## 📧 Support

### Email Configuration
To receive security alerts:
1. Open extension popup
2. Click ⚙️ Settings
3. Enter email address
4. Alerts will be encrypted and sent via HTTPS

### Logs and Debugging
Enable verbose logging:
1. Open Chrome DevTools (F12)
2. Console tab
3. Look for messages prefixed with:
   - 🔒 Session Controller
   - 🚨 Security Alert
   - 🎯 Anomaly Detector
   - 📊 Behavior Tracker

---

## 🔐 Security Notes

### Data Privacy
- All behavioral data stored **locally** in Chrome storage
- No external transmission except security alerts
- Encryption used for sensitive data
- Clear data anytime from Settings

### Permissions Explained
- `storage`: Save behavioral patterns and settings
- `tabs`: Monitor active browsing
- `scripting`: Inject behavior tracking
- `declarativeNetRequest`: Block restricted sites
- `alarms`: Periodic anomaly checks
- `notifications`: Security alerts

---

## 📦 Files Structure
```
chrome-extension/
├── manifest.json               # Extension configuration
├── background/
│   ├── service-worker.js       # Main background logic
│   └── anomaly-detector.js     # AI inference engine
├── content/
│   ├── behavior-tracker.js     # Keystroke/mouse capture
│   └── session-controller.js   # Freeze/unfreeze logic
├── popup/
│   ├── popup.html              # Extension popup UI
│   ├── popup.css               # Popup styling
│   └── popup.js                # Popup logic
├── alert/
│   ├── security-alert.html     # Security alert modal
│   ├── security-alert.css      # Alert styling
│   ├── security-alert.js       # Alert logic
│   ├── access-denied.html      # Limited access page
│   └── session-ended.html      # Termination page
├── models/
│   ├── keystroke-threshold.json # Keystroke model (70.5%)
│   └── mouse-threshold.json     # Mouse model (placeholder)
├── icons/                       # Extension icons
├── utils/                       # Crypto & storage utilities
└── access-control/              # Permission management
```

---

## ✅ Success!

Your Behavioral Authentication Chrome Extension is ready!

**Next Steps:**
1. Install extension ✅
2. Train baseline
3. Test security flows
4. Update mouse model (when ready)
5. Rock your Oct 29 demo! 🎉

---

**Version**: 1.0.0  
**Last Updated**: January 29, 2025  
**Model**: Keystroke (70.5%) | Mouse (Pending)
