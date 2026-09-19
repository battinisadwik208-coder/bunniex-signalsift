# SignalSift model card

## Intended use
Educational, first-pass safety guidance for students evaluating opportunity messages. The output is warning signals and verification actions, not a fraud verdict.

## Transparent scoring
- Sensitive credentials: +30
- Money or payment language: +28
- Unusual domain: +20
- Urgency: +18
- Strong guarantee: +14
- Generic personalisation: +8
- HTTP-only link: +12
- Opportunity link not obviously institution-linked: +12
- Institution-like domain adjustment: -8 (never a safety guarantee)

Scores are clipped to 0–99: high risk is 60+, review carefully is 30–59, and lower risk is below 30.

## Strengths

- Inspectable explanations.
- Works without uploading the message.
- Does not request account credentials.
- Conservative guidance around money and authentication codes.

## Limitations

A clever scam may not match the phrase list. Legitimate messages can contain risky-looking language. Domain endings are weak evidence. The model cannot prove sender identity or inspect a live webpage and is English-first in this MVP.

## Safety boundary

When payment, OTPs, passwords, or identity documents are involved, users are told to stop and verify through an independent official channel.
