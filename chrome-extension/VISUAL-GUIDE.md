# 📸 VISUAL INSTALLATION GUIDE - With Screenshot Instructions

## 🎯 Complete Visual Walkthrough for Chrome Extension Installation

This guide shows you EXACTLY what you'll see on screen at each step.

---

## 🖥️ STEP-BY-STEP WITH VISUALS

### **STEP 1: Open Chrome Extensions Page**

#### What You'll Do:
Type this in your Chrome address bar:
```
chrome://extensions/
```

#### What You'll See:
```
┌─────────────────────────────────────────────────────────────────┐
│  ← → ⟳  chrome://extensions/                              ☰ ⋮  │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Extensions                                    🔍 Search   ⚙️   │
│                                                                  │
│  [Developer mode                                          OFF ] │
│                                                                  │
│  📦 Existing Extension 1                                        │
│  📦 Existing Extension 2                                        │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Look For**: Toggle switch labeled "Developer mode" in top-right corner

---

### **STEP 2: Enable Developer Mode**

#### What You'll Do:
Click the "Developer mode" toggle switch

#### Before (OFF):
```
[Developer mode                                          OFF ]
```

#### After (ON):
```
[Developer mode                                          ON  ]

  [Load unpacked]  [Pack extension]  [Update]
```

**Look For**: Three new buttons appear below the toggle

---

### **STEP 3: Click "Load Unpacked"**

#### What You'll Do:
Click the "Load unpacked" button

#### What You'll See:
Windows File Explorer opens:

```
┌─────────────────────────────────────────────────────────────────┐
│  Select Folder                                          - ☐ ✕   │
├─────────────────────────────────────────────────────────────────┤
│  ⌂ > This PC > Local Disk (C:)                                 │
├──────────────┬──────────────────────────────────────────────────┤
│              │  Name                    Date modified     Type   │
│  Quick       ├──────────────────────────────────────────────────┤
│  access      │  📁 AltairAI            10/28/2025        Folder │
│              │  📁 Program Files       10/20/2025        Folder │
│  🖥️ This PC  │  📁 Users               10/15/2025        Folder │
│  ☁️ OneDrive │  📁 Windows             10/10/2025        Folder │
│              │                                                   │
└──────────────┴───────────────────────────────────────────────────┘
                              [Select Folder]  [Cancel]
```

---

### **STEP 4: Navigate to Extension Folder**

#### Path to Follow:
```
C:\
  └── AltairAI
       └── DataMerge
            └── behavior-authentication
                 └── chrome-extension  ← SELECT THIS!
```

#### What You'll Click:
1. Double-click **"AltairAI"** folder
2. Double-click **"DataMerge"** folder
3. Double-click **"behavior-authentication"** folder
4. **Single-click** **"chrome-extension"** folder (highlight it, don't open!)
5. Click **"Select Folder"** button

#### Final View Before Clicking "Select Folder":
```
┌─────────────────────────────────────────────────────────────────┐
│  Select Folder                                          - ☐ ✕   │
├─────────────────────────────────────────────────────────────────┤
│  ⌂ > C: > AltairAI > DataMerge > behavior-authentication       │
├──────────────┬──────────────────────────────────────────────────┤
│              │  Name                    Date modified     Type   │
│  Quick       ├──────────────────────────────────────────────────┤
│  access      │  📁 chrome-extension    10/28/2025        Folder │ ← Highlighted!
│              │  📁 data                10/25/2025        Folder │
│  🖥️ This PC  │  📁 notebooks           10/26/2025        Folder │
│  ☁️ OneDrive │  📁 src                 10/27/2025        Folder │
│              │                                                   │
└──────────────┴───────────────────────────────────────────────────┘
                              [Select Folder]  [Cancel]
                                     ↑
                                 CLICK HERE!
```

---

### **STEP 5: Extension Loaded Successfully**

#### What You'll See:
The extensions page now shows your extension:

```
┌─────────────────────────────────────────────────────────────────┐
│  Extensions                                    🔍 Search   ⚙️   │
│                                                                  │
│  [Developer mode                                          ON  ] │
│                                                                  │
│  [Load unpacked]  [Pack extension]  [Update]                   │
│                                                                  │
│ ┌───────────────────────────────────────────────────────────┐  │
│ │ 🛡️ Behavioral Authentication                        ON ⚪  │  │
│ │ Behavioral biometrics for continuous authentication      │  │
│ │ ID: abcdefghijklmnopqrstuvwxyz123456                     │  │
│ │ Version: 1.0.0                                            │  │
│ │                                                           │  │
│ │ [Details]  [Remove]  [⟳]  [Errors]                       │  │
│ └───────────────────────────────────────────────────────────┘  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**✅ SUCCESS INDICATORS**:
- Blue shield icon appears
- Name: "Behavioral Authentication"
- Toggle is ON (blue)
- **NO red "Errors" button** (if errors appear, see troubleshooting)

---

### **STEP 6: Pin Extension to Toolbar**

#### What You'll Do:
Click the puzzle piece icon in Chrome toolbar

#### What You'll See:
```
┌─────────────────────────────────────────┐
│  Chrome Toolbar                          │
│  [←] [→] [⟳] [https://...]  [★] [🧩] [⋮]│
│                                    ↑      │
│                              CLICK HERE!  │
└─────────────────────────────────────────┘

Opens dropdown:

┌─────────────────────────────────────┐
│  Extensions                          │
├─────────────────────────────────────┤
│  🛡️ Behavioral Authentication   📌  │ ← Click pin icon
│  📧 Gmail Extension             📌  │
│  🔖 Other Extension             📌  │
├─────────────────────────────────────┤
│  Manage extensions →                │
└─────────────────────────────────────┘
```

#### After Pinning:
```
┌─────────────────────────────────────────┐
│  Chrome Toolbar                          │
│  [←] [→] [⟳] [https://...]  [★] [🛡️] [⋮]│
│                                    ↑      │
│                         Extension icon    │
│                         now visible!      │
└─────────────────────────────────────────┘
```

---

### **STEP 7: Open Extension Popup**

#### What You'll Do:
Click the extension icon (🛡️) in toolbar

#### What You'll See:
```
┌──────────────────────────────────────────┐
│  🛡️ Behavioral Auth                      │
├──────────────────────────────────────────┤
│                                          │
│  ● Monitoring Active                     │
│  Access Level: FULL                      │
│                                          │
│ ┌──────┐ ┌──────┐ ┌──────┐              │
│ │ ⌨️   │ │ 🖱️   │ │ 🎯   │              │
│ │  0   │ │  0   │ │ --   │              │
│ │Keystro│ │Mouse │ │Match │              │
│ └──────┘ └──────┘ └──────┘              │
│                                          │
│  Authentication Confidence      0%       │
│  ╔════════════════════════╗              │
│  ║                        ║              │
│  ╚════════════════════════╝              │
│                                          │
│  🎓 Train Baseline                       │
│  📊 View History                         │
│                                          │
│  Enable Monitoring          ON           │
│  Sensitivity            [Medium ▼]       │
│                                          │
│  v1.0.0              ⚙️ Settings         │
└──────────────────────────────────────────┘
```

**Initial State**:
- Status: Green dot, "Monitoring Active"
- Keystrokes: 0
- Mouse: 0
- Match Score: --
- Confidence: 0%

---

### **STEP 8: Train Baseline**

#### What You'll Do:
Click "Train Baseline" button, then type on any webpage

#### Button States:

**Before Click**:
```
┌──────────────────────┐
│ 🎓 Train Baseline    │
└──────────────────────┘
```

**During Training**:
```
┌──────────────────────┐
│ ⏳ Training...       │
└──────────────────────┘
```

**After Training (as you type)**:
```
┌──────────────────────────────────────────┐
│  🛡️ Behavioral Auth                      │
├──────────────────────────────────────────┤
│                                          │
│  ● Monitoring Active                     │
│  Access Level: FULL                      │
│                                          │
│ ┌──────┐ ┌──────┐ ┌──────┐              │
│ │ ⌨️   │ │ 🖱️   │ │ 🎯   │              │
│ │ 247  │ │ 863  │ │ 82%  │  ← Numbers increasing!
│ │Keystro│ │Mouse │ │Match │              │
│ └──────┘ └──────┘ └──────┘              │
│                                          │
│  Authentication Confidence     85%       │
│  ╔════════════════════════╗              │
│  ║██████████████████      ║  ← Bar filling!
│  ╚════════════════════════╝              │
│                                          │
└──────────────────────────────────────────┘
```

**Target Stats**:
- Keystrokes: 200+ (aim for 300-500)
- Mouse: 500+ (aim for 800-1000)
- Match: 75-90%
- Confidence: 80-90%

---

### **STEP 9: Trigger Anomaly (For Testing)**

#### What You'll Do:
Type VERY slowly or VERY fast (different from your baseline)

#### What You'll See - Freeze Occurs:
```
┌─────────────────────────────────────────────────────────────────┐
│  Your Webpage (BLURRED)                                          │
│  ╔════════════════════════════════════════════════════════════╗ │
│  ║                                                            ║ │
│  ║  Everything becomes blurred and greyed out                 ║ │
│  ║                                                            ║ │
│  ║  You cannot click anything                                 ║ │
│  ║                                                            ║ │
│  ║  Mouse clicks don't work                                   ║ │
│  ║                                                            ║ │
│  ╚════════════════════════════════════════════════════════════╝ │
└─────────────────────────────────────────────────────────────────┘
```

#### Security Alert Modal Appears:
```
┌────────────────────────────────────────────────────────────┐
│                                                            │
│                          🛡️                                │
│                                                            │
│           Unusual Behavior Detected                        │
│                                                            │
│  We've detected behavioral patterns that don't match       │
│  your typical usage. For your security, we need to         │
│  verify your identity.                                     │
│                                                            │
│  ┌──────────────────────────────────────────────┐         │
│  │ Anomaly Score:        72.3% (High)           │         │
│  │ Detected at:          10:45:23 AM            │         │
│  └──────────────────────────────────────────────┘         │
│                                                            │
│  Is this you using this browser?                          │
│                                                            │
│  ┌──────────────────────────────────────────────┐         │
│  │         ✓                                    │         │
│  │    Yes, it's me                              │  GREEN  │
│  │    Continue with full access                 │         │
│  └──────────────────────────────────────────────┘         │
│                                                            │
│  ┌──────────────────────────────────────────────┐         │
│  │         👥                                    │         │
│  │    Someone I know                            │  ORANGE │
│  │    Limited access mode                       │         │
│  └──────────────────────────────────────────────┘         │
│                                                            │
│  ┌──────────────────────────────────────────────┐         │
│  │         ✕                                    │         │
│  │    No, it's not me                           │  RED    │
│  │    Block access immediately                  │         │
│  └──────────────────────────────────────────────┘         │
│                                                            │
│  ⚠️ Security Notice: Your response will be logged         │
│     and encrypted before transmission to your email.      │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

---

### **STEP 10: Response - Limited Access Mode**

#### What You'll Do:
Click the ORANGE button "Someone I know"

#### What You'll See - Limited Access Banner:
```
┌─────────────────────────────────────────────────────────────────┐
│ ┌───────────────────────────────────────────────────────────┐   │
│ │ 🔒 Limited Access Mode                                    │   │
│ │ Passwords and sensitive settings are restricted.          │   │
│ │ Restore Full Access                                       │   │ ← Orange banner
│ └───────────────────────────────────────────────────────────┘   │
│                                                                  │
│  Your Normal Webpage Content                                    │
│                                                                  │
│  Username: [user123        ]  ← Works                           │
│  Password: [🔒 BLOCKED     ]  ← Disabled!                       │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Try to Visit Bank Site**:
```
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│                          🔒                                      │
│                                                                  │
│                    Access Denied                                │
│                                                                  │
│  You are currently in Limited Access Mode. This website has     │
│  been restricted for your security.                             │
│                                                                  │
│  Why am I seeing this?                                          │
│  Our behavioral authentication system detected unusual          │
│  activity patterns. For your protection, access to sensitive    │
│  websites has been temporarily restricted.                      │
│                                                                  │
│                    [← Go Back]                                  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

### **STEP 11: Response - Session Terminated**

#### What You'll Do:
Trigger another anomaly, click RED button "No, it's not me"

#### What You'll See:
```
Processing... (2 seconds)

Then all tabs close and this page appears:

┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│                          🔒                                      │
│                                                                  │
│                  Session Terminated                             │
│                                                                  │
│  For your security, this browsing session has been terminated   │
│  due to detected unauthorized access patterns.                  │
│                                                                  │
│  🛡️ Security Actions Taken                                      │
│  ✓ All browser tabs have been closed                           │
│  ✓ Browsing history has been cleared                           │
│  ✓ Cookies and cached data removed                             │
│  ✓ Stored passwords and form data cleared                      │
│  ✓ Active sessions terminated                                  │
│                                                                  │
│  📧 Security Alert Sent: An encrypted notification has been     │
│  sent to your registered email address.                         │
│                                                                  │
│     [Start New Session]  [Extension Settings]                   │
│                                                                  │
│  Terminated at: 10/29/2025, 10:47:15 AM                        │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🎬 DEMO VISUAL FLOW

### Flow Diagram:
```
START
  │
  ├─→ [Extension Icon in Toolbar]
  │        │
  │        ├─→ Click icon → Popup opens
  │        │
  │        └─→ Shows: Green status, 0 stats
  │
  ├─→ [Type on Webpage]
  │        │
  │        └─→ Stats increase in real-time
  │             Keystrokes: 0 → 247
  │             Mouse: 0 → 863
  │             Confidence: 0% → 85%
  │
  ├─→ [Type Differently - Trigger Anomaly]
  │        │
  │        ├─→ Page blurs and freezes
  │        │
  │        └─→ Security alert modal appears
  │
  ├─→ [Response Options]
  │    │
  │    ├─→ GREEN: "Yes, it's me"
  │    │    └─→ Full access restored
  │    │
  │    ├─→ ORANGE: "Someone I know"
  │    │    └─→ Limited mode + banner
  │    │         └─→ Passwords blocked
  │    │         └─→ Banks redirected
  │    │
  │    └─→ RED: "No, it's not me"
  │         └─→ All tabs close
  │              └─→ Session ended page
  │
END
```

---

## ✅ VISUAL SUCCESS CHECKLIST

**You'll know it's working when you see**:

- [x] Extension card appears (no red errors)
- [x] Icon appears in toolbar (blue shield)
- [x] Popup opens when clicked
- [x] Stats increase when typing
- [x] Confidence bar fills up
- [x] Page blurs when anomaly triggers
- [x] Security modal appears
- [x] Buttons respond to clicks
- [x] Limited mode shows orange banner
- [x] Termination closes all tabs

---

## 🐛 VISUAL TROUBLESHOOTING

### ❌ If You See Red "Errors" Button:
```
┌───────────────────────────────────────┐
│ 🛡️ Behavioral Authentication     ON  │
│ [Details] [Remove] [⟳] [Errors (3)]  │ ← Red button!
└───────────────────────────────────────┘
```

**Fix**: Click "Errors" to read them, then reload extension

---

### ❌ If Stats Stay at Zero:
```
┌──────┐ ┌──────┐
│ ⌨️   │ │ 🖱️   │
│  0   │ │  0   │  ← Not increasing!
└──────┘ └──────┘
```

**Fix**: Refresh the webpage (F5), try new tab

---

### ❌ If No Modal Appears:
```
[Screen is blurred but no modal shows]
```

**Fix**: Check popup blockers, reload extension

---

## 📸 SCREENSHOT TIPS FOR DEMO

### What to Screenshot:
1. Extensions page with your extension loaded
2. Popup showing high stats (300+ keystrokes)
3. Security alert modal with all 3 buttons
4. Limited access banner
5. Session terminated page

### When to Take Screenshots:
- During setup (for backup)
- After successful test
- During actual demo (as backup proof)

---

## 🎯 FINAL VISUAL CHECKLIST

**Before Demo, Verify You Can See**:
- [ ] Extension icon in toolbar
- [ ] Green status dot in popup
- [ ] Stats increasing (200+ keystrokes)
- [ ] Confidence bar at 75%+
- [ ] Security alert triggers
- [ ] All 3 buttons work

**You're Ready! 🚀**

---

**Visual Guide Version**: 1.0  
**Last Updated**: October 28, 2025  
**Demo Date**: October 29, 2025
