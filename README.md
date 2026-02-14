# GEAuthenticator 🔐

> *Secure two-factor authentication for the modern web*

---

## 🌟 **Elevate Your Account Security**

**GEAuthenticator** transforms your browser into a powerful authentication hub. Generate time-based one-time passwords (TOTP) instantly — no phone needed, no cloud dependency, no compromises. Every code is generated locally, ensuring your secrets never leave your device.

---

## 📸 **Screenshot Gallery**

### 1. **Welcome Screen – Empty State**

<img src="https://i.imgur.com/hjdpZV3.png" alt="Welcome Screen" width="600"/>

*This is your first encounter with GEAuthenticator right after installation. The design is clean, minimal, and intentionally sparse to make your next step absolutely clear. The main area displays "No Accounts Yet" in friendly typography, with a prominent button below reading "Add your first authenticator account" that invites you to begin your 2FA journey. At the very bottom, a subtle but reassuring footer states "Military-grade encryption • Secure backup" — setting the tone for security and trust from the very first moment. There's no clutter, no confusing options, just a single clear path forward.*

---

### 2. **Add Account – Manual Setup**

<img src="https://i.imgur.com/ieHWkPL.png" alt="Add Account Screen" width="600"/>

*When you click the "Add Account" button, this is the screen that appears. At the top, the headline reads "Add Account" with the subtitle "Protect with 2FA" beneath it. Two toggle options sit below: **Setup** (highlighted as active) and **Import** (inactive), clearly indicating which mode you're in. The form presents two simple fields. The first is labeled "Account Name" with a placeholder showing "example@gmail.com" — suggesting you use the email or username associated with the account. The second field is labeled "Setup Key" where you'll paste or type the secret key provided by the service, with "JBSWY3DPEHPK3PXP" shown as an example. Below the input fields, there's a helpful hint section labeled "Example Keys:" showing common formats like "JBSWY3DPEHPK3PXP" and "GEZDGNBVGY3TQOJQ..." to guide you. At the bottom, two buttons sit side by side: [Cancel] on the left and [Save] on the right, with the Save button styled more prominently as the primary action. The entire form is clean, well-spaced, and focused — no distractions, just what you need to add your account.*

---

### 3. **Add Account – Import View**

<img src="https://i.imgur.com/2QN0ZA5.png" alt="Import Screen" width="600"/>

*The Import view shares the same header as the Setup screen — "Add Account" with "Protect with 2FA" — but now the **Import** toggle is active while **Setup** is dimmed. Below the toggles, you'll find a text area labeled "Migration Key" or "Import Data" where you can paste the migration codes exported from other authenticator apps like Google Authenticator or Authy. This is the key feature: instead of manually entering each account one by one, you can paste a single block of text containing all your accounts at once. GEAuthenticator parses this data and extracts every account automatically. Before finalizing, the interface shows a preview of what will be imported, listing each account name so you can verify everything is correct and catch any duplicates. This screen transforms what could be a tedious migration process into something that takes just seconds. The [Cancel] and [Import] buttons sit at the bottom, with Import styled as the primary action.*

---

### 4. **Active Account with Live Code**

<img src="https://i.imgur.com/MhNkaw5.png" alt="Active Account Screen" width="600"/>

*This is the main dashboard — what you'll see most often when using GEAuthenticator. The top bar shows the extension name "G Authenticator" with the tagline "Secure two-factor authentication" as a consistent brand reminder. Below this, your account is displayed prominently. The account identifier shows "j a c o k b o o o r m @ g m a i l . c o m" with spaces between each character, making it highly readable and preventing any confusion when reading the address. Just beneath the email, you'll see metadata: "Added: 09/5/2025" — a helpful timestamp giving you context about when this account was set up. The 6-digit code "8 4 6  9 0 8" is displayed in two groups of three digits (846 and 908), following the standard format that makes codes easier to read and transcribe accurately. The digits are large, bold, and dominate the visual space so you can see them instantly at a glance. Below the code, a visual timer shows "● 1s" with a pulsing dot — this indicates there's just 1 second remaining before the code refreshes. The dot pulses gently, providing an at-a-glance status indicator, and as the seconds count down from 30 to 0, you always know exactly how much time you have left to use the current code. The entire card is clickable — tapping anywhere on it copies the code to your clipboard, with a subtle visual confirmation that the copy was successful. It's simple, fast, and exactly what you need in the moment.*

---

## 🔑 **Understanding Secret Keys: The 32-Character Standard**

One of the most common questions users have is: **"Why 32 characters, and what format should they be in?"**

The standard format for TOTP secret keys is based on Base32 encoding. The reference format is "ABCDEFGHIJKLMNOPQRSTUVWXYZ234567" and an example actual key might look like "JBSWY3DPEHPK3PXP". Keys are typically 32 characters long (some services use 16-character keys, which are also accepted), use only uppercase letters A-Z and digits 2-7 to avoid confusing characters like 0,1,8,9 that could be mistaken for letters, and are case-insensitive so you can enter lowercase and GEAuthenticator converts to uppercase automatically.

To find your secret key when setting up 2FA, look for the QR code on the website and then find a link that says "Can't scan it?" or "Manual setup" — click that to reveal the text key and copy it exactly. If GEAuthenticator says your key is invalid, check for extra spaces, incorrect characters like 0,1,8,9 or special symbols, and verify the length is either 16 or 32 characters.

---

## 🎯 **Import vs Setup: What's the Difference?**

Use **Setup (Manual)** when you have a single new account to add, when the service gave you a text key, or when setting up 2FA for the first time. You type or paste one key at a time and choose the account name yourself.

Use **Import** when switching from another authenticator app, when you have many accounts to transfer, or when recovering from a lost device. You paste a block of migration data containing multiple accounts at once, and account names are preserved from the original app.

For example, when switching from Google Authenticator, use its "Export" feature to generate a migration string, then paste that into GEAuthenticator's import field — all your accounts appear instantly.

---

## 🔐 **Security You Can Trust**

"Military-grade encryption" isn't just a phrase — it's our foundation. GEAuthenticator uses **AES-256 encryption** for all stored secrets, the same standard used by governments worldwide. Even if someone gains access to your browser's storage, they cannot read your 2FA secrets without your encryption passphrase.

We've built **zero-knowledge architecture** so that we as developers have no way to access your data. There are no cloud servers storing your secrets, no telemetry sending your accounts back to us. Your 2FA data belongs entirely to you.

The extension is **open source**, meaning the entire codebase is available for public review. Security researchers and concerned users can audit every line of code to verify there are no backdoors or hidden surprises.

GEAuthenticator works **offline first**, generating codes using only your computer's clock and your stored secrets. No one can intercept your codes in transit, and the extension works even without internet access.

With **secure backup**, when you export your accounts, the backup file is encrypted with a password you choose. Without that password, the backup is just random data. Store it anywhere — only you can restore it.

---

## ✨ **Pro Tips**

- **Pin the extension** to your browser toolbar for one-click access
- **Use descriptive account names** like "Work Google" instead of just "Google" if you have multiple accounts
- **Export a backup** immediately after adding new accounts and store it securely
- **Check your computer's clock** if codes aren't working — TOTP relies on accurate time
- **Keep your service backup codes** even after adding them to GEAuthenticator

---

## ❤️ **Open Source Soul**

GEAuthenticator is built with love by developers who believe security should be accessible to everyone, transparent by design, beautiful to use, and free forever. There are no "premium" features behind a paywall, no subscription, no data selling — just a tool that does its job and respects its users.

---

## 📬 **Stay Connected**

- **Report issues** — found a bug? Let us know on GitHub
- **Request features** — we're listening to your feedback
- **Contribute code** — developers of all skill levels welcome
- **Spread the word** — tell a friend, write a blog post, share on social media

---

## ⚖️ **License**

MIT License — use it personally or commercially, modify it, distribute it. The only requirement is that you include the original copyright notice.

---

<p align="center">
  <b>GEAuthenticator</b><br>
  Secure two-factor authentication for everyone<br>
  🔐 Military-grade encryption • Secure backup • Open source
</p>

<p align="center">
  <sub>Made with ❤️ for a more secure internet</sub>
</p>
