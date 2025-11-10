# 🔐 Behavioral Authentication Chrome Extension

**AI-Powered Continuous User Authentication for Chrome**

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Manifest](https://img.shields.io/badge/manifest-v3-green)
![Status](https://img.shields.io/badge/status-demo--ready-orange)

---

## 🎯 Overview

This Chrome extension provides **real-time behavioral authentication** using machine learning models trained on keystroke dynamics and mouse movement patterns. It continuously monitors user behavior and detects anomalies that may indicate unauthorized access.

### Key Features

✅ **Real-Time Monitoring**
- Keystroke dynamics (hold time, flight time, typing rhythm)
- Mouse movement patterns (speed, curvature, click behavior)
- Continuous background analysis

✅ **AI-Powered Anomaly Detection**
- 70.5% accuracy Generalized Linear Model (keystroke)
- 58.2% accuracy Best Model (mouse - trained October 28, 2025)
- Adaptive baseline learning

✅ **3-Tier Security System**
- **Full Access**: Normal browsing for authenticated users
- **Limited Access**: Restricts passwords and sensitive sites
- **Blocked Access**: Terminates session and clears data

✅ **Encrypted Security Alerts**
- HTTPS-based encrypted notifications
- Email alerts with anomaly details
- User-controlled response options

---

## 🚀 Quick Start

### Installation

1. **Load Extension** (Developer Mode):
   ```
   Chrome → Extensions → Load Unpacked → Select chrome-extension/ folder
   ```

2. **Train Baseline**:
   - Click extension icon
   - Press "Train Baseline"
   - Type and browse naturally for 2-3 minutes

3. **Enable Monitoring**:
   - Toggle "Enable Monitoring" → ON
   - Set sensitivity level (Medium recommended)

📖 **Full Installation Guide**: See [INSTALLATION.md](INSTALLATION.md)

---

## 📊 How It Works

### 1. Behavioral Capture
Content scripts track:
- **Keystrokes**: Timing between keydown/keyup events
- **Mouse**: Movement speed, distance, curvature
- Data buffered and sent to background every 5 seconds

### 2. Feature Extraction
Background service worker extracts:
- Average hold time
- Average flight time  
- Typing speed (WPM)
- Error rate
- Mouse speed/straightness
- Pause frequency

### 3. Anomaly Scoring
AI model compares current behavior to baseline:
- Z-score normalization
- Weighted feature scoring (60% keystroke, 40% mouse)
- Sigmoid confidence calculation
- Threshold: 65% = anomaly detected

### 4. Security Response
On anomaly detection:
1. **Freeze** browser (blur page, disable interactions)
2. **Alert** user with 3-button modal
3. **Apply** access level based on response:
   - "Yes, it's me" → Full access
   - "Someone I know" → Limited access
   - "No, it's not me" → Terminate session

---

## 🗂️ Architecture

```
chrome-extension/
├── manifest.json              # Manifest V3 config
│
├── background/
│   ├── service-worker.js      # Main orchestration (310 lines)
│   └── anomaly-detector.js    # AI inference engine (260 lines)
│
├── content/
│   ├── behavior-tracker.js    # Data capture (180 lines)
│   └── session-controller.js  # Freeze/unfreeze (200 lines)
│
├── popup/
│   ├── popup.html             # Extension UI
│   ├── popup.css              # Styling
│   └── popup.js               # Stats display
│
├── alert/
│   ├── security-alert.html    # Security modal
│   ├── security-alert.js      # Alert logic + HTTPS encryption
│   ├── access-denied.html     # Limited access page
│   └── session-ended.html     # Termination page
│
├── models/
│   ├── keystroke-threshold.json  # GLM thresholds (70.5%)
│   ├── mouse-threshold.json      # Mouse thresholds (58.2%)
│   ├── B.rmp                     # Keystroke model from Altair AI (376 KB)
│   └── Mouse.rmp                 # Mouse model from Altair AI
│
├── access-control/
│   └── permission-manager.js     # 3-tier access enforcement
│
├── utils/
│   ├── crypto.js              # AES-256 encryption
│   └── storage.js             # Secure data persistence
│
└── icons/                     # Extension icons (16/48/128)
```

**Total Code**: ~1,500+ lines of production-ready JavaScript

---

## 🧪 Testing Guide

### Basic Functionality Test

1. **Install & Load**:
   ```
   ✓ Extension appears in chrome://extensions/
   ✓ No errors in background console
   ✓ Icon visible in toolbar
   ```

2. **Popup UI Test**:
   ```
   ✓ Open popup → Shows stats
   ✓ Keystroke counter increments
   ✓ Mouse counter increments
   ✓ Confidence score updates
   ```

3. **Behavior Tracking Test**:
   ```
   ✓ Type on any webpage → Keystrokes captured
   ✓ Move mouse → Mouse events recorded
   ✓ Check background console for logs
   ```

### Security Flow Test

#### Test 1: Normal Usage (Full Access)
```
1. Browse normally
2. Observe green status in popup
3. No alerts triggered
Expected: Full access maintained
```

#### Test 2: Anomaly Detection (Limited Access)
```
1. Simulate unusual typing (very fast/slow)
2. Anomaly score crosses 65% threshold
3. Browser freezes + alert modal appears
4. Click "Someone I know"
Expected: Limited access mode activated
         Password fields blocked
         Sensitive sites redirected
```

#### Test 3: Session Termination (Blocked)
```
1. Trigger anomaly alert
2. Click "No, it's not me"
Expected: All tabs closed
         Browsing data cleared
         Session-ended page shown
         Email alert sent
```

---

## 🎨 User Interface

### Extension Popup
- **Status Indicator**: Green (active) / Orange (limited) / Red (blocked)
- **Real-Time Stats**: Keystroke count, mouse events, match score
- **Confidence Bar**: Visual authentication confidence (0-100%)
- **Actions**: Train baseline, view history, settings

### Security Alert Modal
- **Anomaly Score**: Percentage + severity label
- **Detection Time**: When anomaly was detected
- **3 Response Buttons**:
  - ✅ "Yes, it's me" (Green) → Full access
  - 👥 "Someone I know" (Orange) → Limited access
  - ❌ "No, it's not me" (Red) → Block immediately
- **Security Notice**: Encryption + email alert confirmation

---

## 🔐 Security & Privacy

### Data Storage
- **Local Only**: All behavioral data stored in Chrome local storage
- **No Cloud**: No external servers (except email alerts)
- **Encrypted**: Sensitive data encrypted with AES-256-GCM
- **User Control**: Clear data anytime from Settings

### Permissions
| Permission | Purpose |
|------------|---------|
| `storage` | Save behavioral patterns and settings |
| `tabs` | Monitor active browsing context |
| `activeTab` | Inject content scripts |
| `scripting` | Execute behavior tracking |
| `declarativeNetRequest` | Block restricted sites |
| `alarms` | Periodic anomaly checks (30s intervals) |
| `notifications` | Security alerts |
| `<all_urls>` | Track behavior across all sites |

### Email Alerts
- Encrypted using Web Crypto API (AES-GCM)
- Sent via HTTPS webhook
- Contains: timestamp, anomaly score, browser info, user response
- Configurable in Settings

---

## 📈 Model Information

### Keystroke Dynamics Model
- **Algorithm**: Generalized Linear Model (GLM)
- **Accuracy**: 70.5%
- **Training Data**: CMU dataset (20,400 samples, 51 users)
- **Features**: 34 (hold time, flight time, typing speed, error rate, etc.)
- **Source**: Trained in Altair AI Studio
- **File**: `models/keystroke-threshold.json`

### Mouse Dynamics Model
- **Algorithm**: Best Model from Altair AI Studio
- **Accuracy**: 58.2%
- **Training Data**: Balabit dataset (60,905 samples, 65 users)
- **Features**: 43 (speed, curvature, straightness, pauses, etc.)
- **Source**: Trained in Altair AI Studio (October 28, 2025)
- **File**: `models/mouse-threshold.json`

---

## 🛠️ Configuration

### Sensitivity Levels
| Level | Threshold | Description |
|-------|-----------|-------------|
| Low | 80%+ | Only critical anomalies trigger alerts |
| **Medium** | 65%+ | **Recommended** - Balanced detection |
| High | 50%+ | Very sensitive, may false-positive |

### Adaptive Learning
- Baseline updates every 100-150 samples
- Exponential moving average (α = 0.1)
- User-specific pattern adaptation

---

## 🐛 Troubleshooting

### Extension Not Capturing Behavior
**Fix**: Refresh all tabs after installation (content scripts only inject on load)

### Anomaly Detection Too Sensitive
**Fix**: Increase sensitivity to "Low" in Settings or train longer baseline

### Models Not Loading
**Fix**: Verify `models/*.json` files exist and are valid JSON

### Security Alerts Not Appearing
**Fix**: Check `alert/security-alert.html` is web-accessible in manifest

### Full detailed troubleshooting**: See [INSTALLATION.md](INSTALLATION.md#troubleshooting)

---

## 📅 Demo (October 29, 2025)

### Demo Flow
1. **Show Real-Time Monitoring** (2 min)
   - Open popup, display stats
   - Type → Show keystroke capture
   - Move mouse → Show mouse tracking

2. **Trigger Anomaly** (3 min)
   - Simulate unusual behavior
   - Show freeze mechanism
   - Display security alert modal

3. **Demonstrate Security Levels** (5 min)
   - Full access: Normal browsing
   - Limited access: Block passwords/banks
   - Blocked: Terminate session + clear data

**Total Demo Time**: ~10 minutes

---

## 🚧 Future Enhancements

- [x] Export mouse model from Altair AI (✅ Completed October 28, 2025 - 58.2% accuracy)
- [ ] Convert SVG icons to PNG (for better Chrome compatibility)
- [ ] Add history page with anomaly timeline
- [ ] Implement proper email webhook service
- [ ] Add multi-user support (household sharing)
- [ ] Machine learning model retraining in-browser
- [ ] Biometric integration (fingerprint/face)

---

## 📝 License

**Educational/Demo Project**  
Created for behavioral authentication research and demonstration.

---

## 👨‍💻 Developer

**Project**: Behavior-Based Continuous Authentication  
**Platform**: Chrome Extension (Manifest V3)  
**AI Training**: Altair AI Studio  
**Models**: Keystroke (70.5%) + Mouse (58.2%)  
**Demo Date**: October 29, 2025

---

## 📧 Support

For questions or issues:
1. Check [INSTALLATION.md](INSTALLATION.md)
2. Review Chrome DevTools console logs
3. Verify all files present in `chrome-extension/` folder

---

**🎉 Ready to Deploy!**

Install the extension, train your baseline, and enjoy AI-powered behavioral authentication!

---

**Version**: 1.0.0  
**Last Updated**: January 29, 2025  
**Status**: Demo-Ready ✅
