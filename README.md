# 🔐 Memo-to-File Password Generator

Generate secure, deterministic passwords for digital memos using the SHA-256 hash of a file and the current date (`YYYYMMDD`). Ideal for sealing daily government or organizational memos with tamper-evident audit trails.

## ✅ Features

- Uses file content (SHA-256) + date to generate password
- Output format: `M2F-[6charHash]-[YYYYMMDD]`
- Offline and secure – no data leaves the browser
- Built with Alpine.js and TailwindCSS
- GitHub Pages ready

## 🕒 Recommended Practice

To ensure audit integrity, base the date input on a **trusted time source**, such as:
- [PAGASA Time](https://bagong.pagasa.dost.gov.ph/)
- Any NTP-synced system clock (e.g., PC or phone)

This ensures consistent, tamper-resistant timestamps when generating memo passwords.

## 📄 Usage

1. Select the previous memo file (e.g., PDF)
2. Choose the official date (`YYYY-MM-DD`)
3. Click "Generate Password"
4. Use the output for memo sealing or secure referencing

## 🔐 Output Format

