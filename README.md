# Cold QR Scanner (Cold Wallet Animated QR Reader)

A small, fully **offline** Android app that reads **animated QR sequences** from a computer screen, reassembles them into CSV files, and saves them directly to `Download/ColdQRScanner/`.

---

## 📥 Download & Install (Testing v1.0)

- **Latest APK Download**: [Download ColdQRScanner_v1.0.apk](app/ColdQRScanner_v1.0.apk)
- **Direct GitHub Release**: [GitHub Releases v1.0](https://github.com/ssomethingg00/cold_wallet/releases/tag/v1.0)

---

## 🔒 Security & Privacy Guarantees

- **100% Offline**: `android.permission.INTERNET` is **NOT** declared.
- **Zero Third-Party Telemetry**: No analytics, no ads, no cloud, no Play Services.
- **On-Device QR Decoding**: CameraX with ZXing Core (`com.google.zxing:core`) decoding locally on your phone.
- **Permissions**: `CAMERA` (for scanning) and `VIBRATE` (for haptic feedback).
- **minSdk**: 26 (Android 8.0+) | **targetSdk**: 36

---

## 📱 Features

1. **Animated QR Reconstruction**:
   - Reassembles `CSQR i/n label` multi-part animated sequences out-of-order.
   - Automatically saves completed transfers as `<NNN>_<label>_<yyyyMMdd_HHmm>.csv` into `Download/ColdQRScanner/`.
2. **Single QR Transactions**:
   - Scans single transactions / addresses (`0x...`, base64) into an in-memory list without duplicate scans.
   - Saves on demand via **Save singles** as `<NNN>_scanned_<yyyyMMdd_HHmm>.txt`.
3. **In-App History**:
   - View all saved transfers directly in the app.
   - **Open**: Inspect the first 50 lines in a monospace viewer.
   - **Share**: Export to system share sheet via `FileProvider`.
4. **Testing Paste Dialog**:
   - Allows pasting raw QR text directly to test assembly without a camera.
