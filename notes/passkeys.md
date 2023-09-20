---
id: cq5zfpb7ksjheeeyxstixjl
title: Passkeys
desc: ''
updated: 1695244611221
created: 1691521859657
---
# Move over passwords, passkeys are my new best friend! - Daphne Liu
[Slides](daphneliu.com/passkeys.pdf) |
[Talk on YouTube](https://www.youtube.com/watch?v=a3yZUPMMTQw) |
Daphne Liu @thebetterdaphne

## Passkeys
Replacement for passwords that let users sign in with their device lock screen.
- Touch ID
- Face ID
- Windows Hello
- Anroid Prompt
- Other biometric usage

Creates the ability for users to log in on multiple different devices. Connections with your phone to the computer can be done with using QR Codes and camera usage, OR creating a passkey on the desktop.

Connecting passkeys allows the ability to sync to cloud services for multi-device usage.

## Security Comparison
1. Passwords
    - Basically useless.
    - Need to lookup in app
2. Password + 2FA
    - Susceptible to phishing with intercepted text messages.
3. Passkeys
    - Phishing resistent
    - Built into computer/phone
4. Hardware Security KEy
    - ie, Yubikey - a physical device
    - Need to carry

## How Passkeys Work
AKA - "Discoverable Credentials"
Secure with public key cryptography. The encryption converts the message with one key.

Ex: A public key is like a mailing address, and a private key is like the mailbox key. Only you can access the private key.

Private keys can be used to prove identity. A server has a public key that can be accessed with that identity.

Phishing is prevented as the site is the only location that can provide the proper public key for the private key to fit into.

No separate hardware needed, faster for users to use, and bound to website origin - creating phishing resistant options.

## Passkey Support
WebAuthentication API (WebAuthn)
1. Used to supplement passwrods - uses a hardware device as a second factor.
2. Replaces passwords - uses a hardware device as a single factor (Passkeys)

## Creating Passkeys
Registration (Attestation)
Your Website (Relying Party)
The user will add a new passkey that will verify against the user biometrics.

## Takeaway
Use an existing library for backend authentication