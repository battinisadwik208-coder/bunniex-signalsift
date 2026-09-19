# SignalSift

SignalSift is a privacy-first student safety toolkit for checking scholarship, internship, course, job, and prize messages before clicking, paying, or sharing sensitive information. It is a distinct project built for the BunnieX Hackathon 2026.

## What it does

- Accepts a message and optional link.
- Detects explainable signals: urgency, payment requests, credential requests, unusually strong promises, suspicious domains, HTTP-only links, and generic personalisation.
- Produces a 0–100 warning score with a human-readable explanation.
- Gives a safer next action instead of pretending to prove fraud.
- Stores only the last five checks in browser local storage.
- Includes realistic sample messages for a fast demo.

## Run locally

No build step is required. Open `index.html` in a browser or run `python -m http.server 8080` in this folder.

## Privacy and limitations

Analysis runs in the browser. There is no backend, analytics, login, or data upload. Do not paste passwords, OTPs, identity documents, or private financial information. A low score does not prove safety. The current version does not fetch live links or verify sender identity.

## Model disclosure

The MVP uses a transparent weighted signal model rather than an opaque classifier. Each matched signal contributes a documented weight, and official-looking domains receive only a small confidence adjustment. See `MODEL_CARD.md`.

## Demo flow

1. Click **Scholarship fee**.
2. Click **Analyze signals**.
3. Show the payment, OTP, urgency, and suspicious-domain explanations.
4. Compare the internship and official-looking samples.
5. Explain why a low score is not a guarantee.

## Future scope

A user-controlled URL reputation lookup, multilingual analysis, campus reporting workflow, and retrieval-backed explanation layer can be added while preserving data minimisation.
