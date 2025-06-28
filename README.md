# 🔐 Memo Password Generator

A hash-based PDF password generator for government memo files using trusted time sources and file hashes. Designed to ensure non-repudiation, chain-of-trust, and easy verification of documents, especially in contexts requiring audit-traceable workflows like COA or CSC compliance.

## 🌐 Features

- 🔑 **Password Generation** for:
  - First file using trusted date only
  - Next file using previous file's hash + current date
- 🧾 **Verification**:
  - Attempt to open the file using the derived password
  - Match success/failure is visually shown
- 🔗 **Hash Chain Logic** to link documents securely
- 🌍 **Uses NTP Sources**:
  - PAGASA (`https://bagong.pagasa.dost.gov.ph/`)
  - TIME.GOV (`https://time.gov/`)
- 🧠 **Client-side Only**: No backend or file uploads
- 📎 **PDF.js for password-protected file verification**

## 🔧 Modes

1. **First File**
   - Generates a password from `SHA256("FIRST" + date)`
   - For initial memo file creation  
   - ✅ **Current First File Password**: `70BBD8C9CD026ABA4D8F1BC2743188FE`

2. **Verify First File**
   - Takes a date and file
   - Derives password and attempts PDF open

3. **Next File**
   - Requires a file (previous memo)
   - Uses its hash + current date to derive password

4. **Verify File**
   - Uses previous file + date to generate password
   - Tries opening selected file with derived password

5. **Chain Files**
   - 🔧 _[Planned]_ Will verify a series of memos by chaining their hashes and dates

## ✅ Verifiability

- First files can be uploaded to GitHub or emailed for immutability.
- Later files can be verified using their hash + the date they were generated.
- Supports manual or automated audit trails.

## 🔒 Security

- Passwords are 32-character SHA-256 substrings
- Date-fetched from trusted public sources
- Files are never uploaded—everything runs client-side

## 📤 Deployment

Just host the `index.html` on GitHub Pages or any static web host. All assets are CDN-loaded.

---

Created for secure personal HR workflows and COA-traceable documentation chains.  
Contributions and audits welcome.
