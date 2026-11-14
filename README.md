# diall_form — Appointment request form

A one-page form (`index.html`) people open by scanning a QR code to request an appointment. No build step.

- **Live page:** https://diallme-coder.github.io/diall_form/ (enable GitHub Pages: Settings → Pages → `main` / root)
- **QR codes:** `qr-card.png` (printable card), `qr.png` / `qr.svg` (code only)

## What visitors fill in
Name, phone, optional email, reason, preferred date and time, an alternative time, meeting format (in person / phone / video) and a message.

## Where requests go
Submissions are emailed to the inbox set in `INBOX` in `index.html`, via [FormSubmit](https://formsubmit.co). The first submission sends a one-time activation email that must be confirmed. After activating, replace the address in `INBOX` with the random alias FormSubmit provides so the email isn't visible in the page source. If sending fails, visitors are offered a pre-filled email instead.

## Run locally
```
python3 -m http.server 8000
```
