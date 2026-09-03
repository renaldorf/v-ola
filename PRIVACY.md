# Privacy Policy for V-ola

**Effective Date:** March 2025  
**Developer / Organization:** ParAus Labs  
**Contact:** [renaldofig@gmail.com](mailto:renaldofig@gmail.com)

---

## 1. Introduction & Core Philosophy
**V-ola** is built by **ParAus Labs** as a player-first, distraction-free guitar songbook and practice companion. We strongly believe that your personal repertoire, practice data, and musical arrangements belong solely to you.

Our core technical architecture operates on a **zero-telemetry, offline-first principle**:
- We do not run proprietary user-tracking servers.
- We do not collect, sell, or rent your personal data.
- We do not integrate third-party ad networks or user analytics SDKs.

---

## 2. Information We Handle & Where It Stays

### 2.1 Songbook & Repertoire Data (Local SQLite Storage)
- **What is stored:** All songs, lyrics, chords, tabs, custom arrangements, transpositions, capo positions, setlists, and practice history.
- **Where it is stored:** 100% locally on your device within the application's sandboxed SQLite Room database.
- **Accessibility:** ParAus Labs has no access to your songbook. If you uninstall the app without backing up or exporting your files, this data is permanently removed by your operating system.

### 2.2 Audio Data & Microphone Access
- **Purpose:** Used exclusively for real-time guitar pitch detection (Chromatic Tuner) and acoustic rhythm onset following (Live Tempo Assistant).
- **Processing:** Audio is processed ephemerally in device RAM using native digital signal processing (Fast Fourier Transform and YIN algorithms).
- **Zero Recording / Zero Transmission:** Audio frames are analyzed in real-time buffers of fractions of a second and immediately discarded. No audio is ever recorded to disk, transmitted across the internet, or analyzed for speech/biometrics.
- **Permission Deferral:** Microphone access is never requested on startup; it is requested only at the exact moment you open the Tuner or enable the Live Tempo Assistant.

### 2.3 Camera Access (Optional Barcode Scanner)
- **Purpose:** Used solely for peer-to-peer (P2P) song import via on-screen QR codes.
- **Processing:** Handled locally via Google ML Kit Barcode Scanning. No video streams or captured images are ever saved, stored, or sent to any server.

### 2.4 Google Drive Vault Backup (Optional)
- **Scope (`drive.appdata`):** If you choose to enable cloud backup, V-ola uses the restricted Google Drive Application Data Folder.
- **Isolation:** V-ola can only read and write its own encrypted/JSON backup files within this hidden app folder. It cannot access your personal Google Drive documents, photos, or other files.
- **Direct Connection:** Backup syncs communicate directly between your Android device and your personal Google Drive account. No intermediate server or third-party proxy is involved.

### 2.5 In-App Purchases (Early Supporter / Coffee Tip)
- In-app purchases are handled directly by the **Google Play Billing API**.
- ParAus Labs never receives, processes, or stores your credit card numbers, billing addresses, or banking details. Transactions are governed by the [Google Play Terms of Service](https://play.google.com/about/play-terms/).

---

## 3. Third-Party Services
V-ola integrates only the minimum essential services provided by the Android platform and Google Play:
- **Google Play Services / Billing:** For secure purchase entitlement verification.
- **Google Play Services / ML Kit:** For on-device QR barcode parsing.
- **Google Sign-In (Optional):** Only used if you explicitly connect Google Drive for personal vault backups.

---

## 4. Children’s Privacy
V-ola is a general-audience musical tool suitable for all ages. It does not knowingly collect any personal information from children or any other users.

---

## 5. Changes to This Policy
We may update this Privacy Policy from time to time to reflect app updates or regulatory compliance. Any updates will be published in this repository and within the application's About section.

---

## 6. Contact Us
If you have any questions or feedback regarding this Privacy Policy or V-ola's offline architecture, please contact us at:

**ParAus Labs**  
Email: [renaldofig@gmail.com](mailto:renaldofig@gmail.com)  
Project Repository: [https://github.com/renaldofig/vola](https://github.com/renaldofig/vola)
