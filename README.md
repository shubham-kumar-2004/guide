# SeedSigner User Guide (Draft)

This guide provides an introduction to the SeedSigner DIY Bitcoin signing device, detailing core functionalities such as setup, seed generation, seed management, and transaction signing. Written in Markdown for easy translation, it is intended to help users of all skill levels get started quickly and securely.

> **Note:** This is an initial draft. Community feedback is welcome for refining content, improving clarity, and adding translations.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Device Setup](#device-setup)
3. [Seed Generation](#seed-generation)
4. [Seed Management](#seed-management)
5. [Signing Transactions](#signing-transactions)
6. [Troubleshooting & FAQs](#troubleshooting--faqs)
7. [Resources](#resources)
8. [License & Credits](#license--credits)

---

## Introduction

SeedSigner is a DIY (Do It Yourself) Bitcoin signing device that helps users securely manage their Bitcoin private keys offline. By assembling your own hardware and using open-source software, you maintain control over your keys and reduce reliance on pre-built commercial hardware wallets.

**Key Features:**
- Offline key generation and signing for enhanced security.
- Fully open-source software and hardware plans.
- Customizable build approach with accessible, low-cost hardware components.

**What You’ll Need:**
- A fully assembled SeedSigner device (Raspberry Pi Zero, camera module, display, etc.).
- A microSD card loaded with the SeedSigner software.
- (Optional) Extra microSD cards for storing settings or backups.

![SeedSigner Device Overview](./images/seedsigner_device_overview.jpg "Example device, camera module, and screen")

---

## Device Setup

1. **Prepare the Hardware**  
   - Assemble the Raspberry Pi Zero, camera module, and display according to the official hardware instructions.  
   - Ensure all connections are firmly seated to avoid any loose components.

2. **Install SeedSigner on microSD**  
   - Flash the SeedSigner software image onto a microSD card using a tool such as [balenaEtcher](https://www.balena.io/etcher/).  
   - Insert the microSD into the Raspberry Pi Zero.

3. **Power On & Initial Configuration**  
   - Power up the device using a USB power source.  
   - The SeedSigner interface should appear on the display; follow on-screen prompts to configure language, date, and time if needed.

![Hardware Assembly Screenshot](./images/hardware_assembly.jpg "Example of a user connecting the camera module")

---

## Seed Generation

SeedSigner can generate a new Bitcoin seed offline, ensuring maximum security.

1. **Choose “Generate Seed”**  
   - From the main menu, select the “Generate Seed” option.  
   - Follow any on-screen instructions (e.g., moving the device around to capture randomness).

2. **View & Record the Seed Words**  
   - The device will display a 12- or 24-word mnemonic phrase (BIP39 standard).  
   - Carefully write down the words in order on a piece of paper.  
   - Double-check for correct spelling; store in a secure, private location.

3. **Verify the Seed**  
   - The device may prompt you to confirm certain words to ensure accuracy.  
   - Confirm each requested word to complete seed generation.

![Seed Generation Screenshot](./images/seed_generation.jpg "Example seed words displayed on screen")

---

## Seed Management

SeedSigner operates without storing any seed in persistent memory, meaning each seed is erased upon power-off.

- **Import Existing Seed:**  
  If you have a pre-existing seed, input it manually via the keypad or scan a QR code (if supported).  
- **Backup & Offline Storage:**  
  Keep physical copies of your seeds offline.  
- **Security Best Practices:**  
  Never share or digitize your mnemonic beyond the secure environment of SeedSigner or other trusted hardware devices.

---

## Signing Transactions

A key function of SeedSigner is offline transaction signing. Typically, you’ll create a transaction on a watch-only wallet, then finalize it with SeedSigner:

1. **Create a Transaction on Your Online Wallet**  
   - Use a compatible wallet software to construct a new Bitcoin transaction.  
   - Export the unsigned transaction data as a QR code or file.

2. **Scan or Load the Unsigned Transaction**  
   - If using QR codes, select “Scan Unsigned Transaction” on SeedSigner.  
   - Align the wallet’s QR code with the SeedSigner camera.

3. **Confirm Transaction Details**  
   - Review transaction outputs, fees, and addresses on the SeedSigner screen.  
   - If correct, approve signing.

4. **Export the Signed Transaction**  
   - A signed transaction QR code or file is generated.  
   - Import the signed transaction back into your wallet for broadcast to the Bitcoin network.

![Signing Workflow Screenshot](./images/signing_workflow.jpg "Example of scanning a QR code for an unsigned transaction")

---

## Troubleshooting & FAQs

- **Device Not Powering On**  
  - Check all cables and ensure your USB power source meets voltage and amperage requirements (5V, 2A+ recommended).

- **Camera Not Detecting QR Code**  
  - Make sure the lens is clear.  
  - Adjust lighting or focus distance.

- **Forgot or Lost Seed**  
  - Unfortunately, if you lose your seed words, you can’t recover Bitcoin funds.  
  - Always maintain secure backups.

---

## Resources

- [SeedSigner GitHub Repository](https://github.com/SeedSigner/seedsigner)  
  Contains the latest software, documentation, and community discussions.
- [Official README](https://github.com/SeedSigner/seedsigner/blob/main/README.md)  
  Step-by-step assembly guides, additional usage tips, and project roadmap.

---

## License & Credits

- **License:** MIT (See the repository for full license details.)  
- **Credits:**  
  - SeedSigner core team and contributors.  
  - Open-source community participants for testing, bug reports, and feature requests.

---

# End of Draft
