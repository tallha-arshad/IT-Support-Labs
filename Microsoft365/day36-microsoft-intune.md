# Day 36 - Microsoft Intune (Endpoint Management)

## Key Concepts
Microsoft Intune is a cloud-based service for Mobile Device Management (MDM) and Mobile Application Management (MAM). It allows IT administrators to manage and secure devices (Windows, Mac, iOS, Android) over the internet without needing them physically connected to the company network.

There are two main pillars to Intune:
1. Compliance Policies: Rules that a device must follow to be considered "safe" (e.g., requiring a PIN, requiring BitLocker encryption). If a device fails, it is blocked from company data.
2. Configuration Profiles: Settings that are pushed to a device to configure it (e.g., pushing a Wi-Fi password, blocking the camera, or installing an app).

## Lab (Conceptual Review)
Note: My current Microsoft 365 Business Basic tenant does not include an Intune license, so I am documenting the core concepts and workflows before setting up a dedicated Intune trial environment.

- **Device Enrollment:** Reviewed how devices are enrolled into Intune (Windows Autopilot for corporate laptops, or the Company Portal app for mobile devices).
- **Compliance Policy Creation:** Reviewed the workflow for creating a policy to enforce password requirements and disk encryption on Windows devices.
- **Configuration Profiles:** Reviewed how to push device restrictions, such as disabling USB storage or blocking the camera, to prevent data leaks.

## Why It Matters
In modern IT and MSP environments, engineers do not touch every laptop physically. Intune allows remote management, enforcement of security policies, and rapid deployment of apps, which is critical for a remote workforce.

## Interview Q&A

**Q: What is the difference between a Compliance Policy and a Configuration Profile in Intune?**
A: A Compliance Policy checks the device to see if it meets security standards (like having a password) and blocks access if it fails. A Configuration Profile actively changes or pushes settings to the device (like installing an app or configuring Wi-Fi).

**Q: How do you enroll a new employee's laptop into Intune without touching it?**
A: Using Windows Autopilot. The hardware ID is registered to the company. When the user turns on the laptop and signs in with their company email, Intune automatically configures the device, installs required apps, and applies security policies.
