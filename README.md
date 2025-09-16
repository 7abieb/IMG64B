A modern, client-side web tool for encrypting and decrypting images to/from secure Base64 strings using AES encryption. Built with HTML, CSS, and JavaScript—no server required!

---

# Image Base64 Encryptor/Decryptor

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with HTML/CSS/JS](https://img.shields.io/badge/Made%20with-HTML%20%7C%20CSS%20%7C%20JS-blue)](https://developer.mozilla.org/en-US/docs/Web)
[![CryptoJS](https://img.shields.io/badge/Encryption-CryptoJS%20(AES)-green)](https://www.npmjs.com/package/crypto-js)

A lightweight, fully client-side web application for securely encrypting images to Base64 strings and decrypting them back to viewable images. Perfect for sharing sensitive images privately or embedding encrypted data in text formats (e.g., emails, configs, or APIs). Uses AES-256 symmetric encryption via CryptoJS for security, all running in your browser—no data leaves your device.

## 🚀 Features
- **Encrypt Images**: Upload any image (PNG, JPG, GIF, etc.), convert to Base64, and encrypt with a password. Outputs a secure string ready to copy/paste.
- **Decrypt Images**: Paste an encrypted Base64 string and password to recover and preview the original image.
- **Modern UI**: Clean, responsive design with dark gradients, hover effects, and mobile-friendly layout (built with vanilla HTML/CSS/JS—no frameworks).
- **Privacy-Focused**: Everything processes client-side. No uploads to servers, no tracking.
- **Easy to Use**: Single HTML file—open in any modern browser (Chrome, Firefox, Edge, Safari).
- **Error Handling**: Validates inputs, shows success/error messages, and handles invalid passwords gracefully.
- **Lightweight**: ~5KB minified (plus CDN for CryptoJS). Supports images up to ~10MB.

## 📱 Screenshots
### Encryption Section
![Encryption UI](screenshots/encryption.png)
*(Upload an image, enter password, and get encrypted Base64)*

### Decryption Section
![Decryption UI](screenshots/decryption.png)
*(Paste encrypted string, enter password, and view decrypted image)*

### Full App View
![Full App](screenshots/full-app.png)
*(Responsive design on desktop and mobile)*

*Note: Add actual screenshots to a `/screenshots` folder in your repo and update the image paths above.*

## 🛠️ Installation & Setup
1. **Download**: Clone or download this repo as a ZIP.
2. **Run**: Simply open `index.html` (or rename the provided HTML file) in your web browser. No build tools, servers, or installations needed!
3. **Offline Use**: The app works offline after loading (CryptoJS loads via CDN on first visit, but you can download it locally if preferred).
4. **Customization**: Edit the HTML/CSS/JS directly. To make it fully offline, download CryptoJS and reference it locally:
- Download from [CryptoJS GitHub](https://github.com/brix/crypto-js).
- Replace `<script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>` with a local path.

### Dependencies
- **CryptoJS** (v4.1.1): For AES encryption/decryption (loaded via CDN for simplicity).
- No other external libraries—pure vanilla JS.

## 📖 How to Use

### 1. Encrypt an Image
- Click "Choose File" and select an image (e.g., PNG, JPG).
- Enter a strong password in the "Enter encryption password" field.
- Click **Encrypt to Base64**.
- Copy the encrypted string from the output textarea (safe to store/share).

**Example Output**: `U2FsdGVkX1+...` (AES-encrypted Base64).

### 2. Decrypt an Image
- Paste the encrypted Base64 string into the textarea.
- Enter the exact same password.
- Click **Decrypt and Show Image**.
- The original image will preview on the right if successful.

**Tips**:
- Use the same password for encrypt/decrypt—it's symmetric encryption.
- Wrong password? You'll see an error (decrypted data will be garbage).
- For large images, processing may take a few seconds.

### Example Workflow
1. Encrypt a confidential diagram to a string.
2. Email the string securely.
3. Recipient pastes it into the tool with the shared password to view the image.

## 🔒 Security Notes
- **Encryption Strength**: Uses AES-256 (industry-standard symmetric encryption). Secure as long as your password is strong (e.g., 12+ characters, mix of letters/numbers/symbols).
- **Client-Side Only**: No data is sent to any server—your images and keys stay private.
- **Base64 Limitation**: Base64 is encoding (not encryption), so we encrypt the Base64 string for security. The output is safe to transmit as text.
- **Best Practices**:
- Never share passwords plainly.
- For production use, consider hashing passwords or adding key derivation (e.g., PBKDF2—not included here for simplicity).
- Browser storage: Avoid saving encrypted strings in localStorage without additional protection.
- **Not for...**: Ultra-sensitive data (use proper crypto libraries like Web Crypto API for advanced needs). This is a convenience tool.

## ⚠️ Limitations
- **File Size**: Browser may struggle with images >10MB—use smaller files for best performance.
- **MIME Detection**: Decryption assumes PNG as default; for other formats, the image may not display perfectly (enhance by storing MIME type separately).
- **Browser Compatibility**: Modern browsers only (IE not supported).
- **No Asymmetric Encryption**: Symmetric only (same password for encrypt/decrypt). For public-key crypto, extend with libraries like OpenPGP.js.

## 🤝 Contributing
Contributions welcome! Fork the repo, make changes, and submit a pull request. Ideas for improvements:
- Add MIME type preservation.
- Support file downloads (encrypted/decrypted).
- Integrate Web Crypto API for native browser encryption.
- Dark/Light mode toggle.

Report issues or suggest features in the [Issues](https://github.com/yourusername/image-base64-encryptor/issues) tab.

## 📄 License
This project is licensed under the MIT License—see the [LICENSE](LICENSE) file for details. (Feel free to add one if not already present.)

## 🙏 Acknowledgments
- Built with love using vanilla web technologies.
- CryptoJS by [Evan Vosberg](https://github.com/brix) for encryption.
- Inspired by secure data sharing needs in web apps.

---

**Star this repo if it helps!** 🚀 Questions? Open an issue or contact me.

---

