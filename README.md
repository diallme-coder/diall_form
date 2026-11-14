# diall_form — Appointment request form

A one-page form (`index.html`) people open by scanning a QR code to request an appointment. No build step.

- **Live page:** https://diallme-coder.github.io/diall_form/ (enable GitHub Pages: Settings → Pages → `main` / root)
- **QR codes:** `qr-card.png` (printable card), `qr.png` / `qr.svg` (code only)

## What visitors fill in
First name, last name, phone number, a date, a time of day (morning / afternoon / evening) and a required tick box asking to be called to confirm.

## Where requests go
Submissions are emailed to the inbox set in `INBOX` in `index.html`, via [FormSubmit](https://formsubmit.co). The first submission sends a one-time activation email that must be confirmed. After activating, replace the address in `INBOX` with the random alias FormSubmit provides so the email isn't visible in the page source. If sending fails, visitors are offered a pre-filled email instead.

## Phone alerts
Each request also sends an instant push notification through [ntfy](https://ntfy.sh). Install the ntfy app (iPhone or Android) and subscribe to the topic in `NTFY_TOPIC` in `index.html`. The topic name is public in the page source, so the alert only shows the date and time slot. Names and phone numbers go to email only.

## Run locally
```
python3 -m http.server 8000
```
