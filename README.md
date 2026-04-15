# FinanceWithYu Cloud Infrastructure

A self-hosted cloud storage and content management system built to support a growing finance-focused content workflow using **Nextcloud**, **Apache**, **PHP**, **MariaDB**, and **external block storage**.

---

## Overview

This project documents the design, deployment, and troubleshooting of a **self-hosted private cloud infrastructure** created to support the media and content workflow of a growing Instagram finance brand, **FinanceWithYu**.

The motivation behind this project came from observing a practical limitation in using third-party storage platforms like Google Drive for structured content storage, access control, and long-term scalability. Instead of continuing to depend entirely on external SaaS storage, I decided to build a private cloud solution using open-source tools and student cloud resources.

This project was deployed on a Linux-based VPS with HTTPS, database integration, and mounted external storage, making it a real-world infrastructure project rather than a theoretical academic exercise.

---

## Problem Statement

As the amount of digital content increased, managing media files through standard cloud storage tools became inefficient for the following reasons:

- Lack of full control over storage organization
- Dependency on third-party service limits and pricing
- Need for secure, browser-based file access
- Growing requirement for scalable storage
- Need for a cleaner workflow for content assets

The goal was to design a system that:
- provides private cloud file access,
- supports future scaling,
- integrates external storage cleanly,
- and demonstrates real-world infrastructure deployment skills.

---

## Solution

To solve this problem, I designed and deployed a **self-hosted Nextcloud-based private cloud** on a VPS.

The deployment includes:

- Ubuntu-based Linux server
- Apache2 web server
- PHP 8.2 with PHP-FPM
- MariaDB database
- Nextcloud as the private cloud platform
- HTTPS using SSL certificates
- External mounted storage integrated through Nextcloud’s External Storage support

The final system allows users to securely access files through the browser while keeping application logic, metadata, and storage concerns properly separated.

---

## Tech Stack

### Operating System
- Ubuntu Server

### Web Layer
- Apache2
- SSL / HTTPS

### Backend / Runtime
- PHP 8.2
- PHP-FPM

### Database
- MariaDB

### Application
- Nextcloud

### Storage
- Local VPS disk for OS and application
- External mounted block storage for media/file storage

### Infrastructure Concepts Used
- DNS and domain routing
- HTTPS configuration
- Virtual host configuration
- External storage integration
- Linux permissions and ownership
- Service management and debugging
- Real-world troubleshooting and recovery

---

## Architecture Summary

The system follows a simple but production-relevant architecture:

1. A user opens the custom domain in the browser.
2. DNS resolves the domain to the VPS public IP.
3. Apache2 receives HTTPS requests.
4. PHP-FPM processes Nextcloud PHP application logic.
5. Nextcloud reads and writes:
   - metadata to MariaDB
   - files to mounted external storage
6. Users interact with content through the Nextcloud web interface.

---

## Architecture Diagram

See the architecture diagram here:

architecture/nextcloud_architecture_diagram.png

If the image does not render directly in your viewer, open it from the architecture/ folder.

---

## Key Features

- Self-hosted private cloud deployment
- Secure browser-based access over HTTPS
- External mounted storage added as managed storage inside Nextcloud
- Separation of system/app layer and file storage layer
- Real-world debugging of infrastructure issues
- Resource-efficient deployment using student cloud/domain benefits
- Suitable for media/content workflows

---

## Real-World Use Case

This project was built to support the content workflow of **FinanceWithYu**, a growing finance-focused Instagram page.  
Instead of depending fully on Google Drive for content storage, this deployment created a controlled private cloud system that could support real uploads, storage organization, and secure access.

Because this project was tied to an actual use case and user need, it became a strong hands-on exercise in:

- infrastructure setup,
- deployment,
- debugging,
- security basics,
- and storage management.

---

## Screenshots

Project screenshots are available under the `screenshots/` folder.

Recommended screenshots included in this repository:

- `screenshots/nextcloud-dashboard.png`
- `screenshots/external-storage-settings.png`
- `screenshots/storage-mounted.png`
- `screenshots/security-warnings.png`

These screenshots help demonstrate the actual deployment and can still serve as proof of the project even if the live deployment is no longer active in the future.

---

## Challenges Faced

This project involved significant troubleshooting and recovery work, which became one of its strongest learning outcomes.

Major issues included:

- DNS conflicts between multiple hosting targets
- Nextcloud trusted domain errors
- Apache virtual host misconfiguration
- database authentication failures
- PHP compatibility problems
- port conflicts from mixed or legacy web server processes
- external storage permission handling

Detailed write-ups are available in:

- `troubleshooting/issues-faced.md`
- `troubleshooting/sanitized-log-snippets.md`

---

## Lessons Learned

This project taught me the importance of:

- verifying compatibility before deployment,
- keeping infrastructure simple and clean,
- avoiding mixed service stacks,
- documenting problems and fixes,
- thinking in terms of architecture, not just installation,
- and using available resources efficiently.

One of the biggest takeaways was that real infrastructure projects are not only about getting the final application online, but also about recovering from misconfigurations, debugging complex interactions, and learning how systems behave under failure.

---

## Project Status

**Status:** Functional and documented

### Completed
- VPS provisioning
- Linux setup
- Apache + PHP-FPM setup
- MariaDB database setup
- Nextcloud deployment
- HTTPS setup
- External storage integration
- basic documentation

### Planned / Future Improvements
- Redis for file locking and performance
- cron background jobs
- Fail2Ban
- 2FA
- automated backups
- PHP and Nextcloud upgrade strategy
- monitoring and alerting

See `roadmap.md` for the full roadmap.

---

## Repository Structure

```text
financewithyu-cloud-infra/
├── README.md
├── roadmap.md
├── architecture/
│   └── nextcloud_architecture_diagram.png
├── screenshots/
│   ├── nextcloud-dashboard.png
│   ├── external-storage-settings.png
│   ├── security-warnings.png
│   └── storage-mounted.png
├── troubleshooting/
│   ├── issues-faced.md
│   └── sanitized-log-snippets.md
└── docs/
    ├── setup-summary.md
    └── deployment-notes.md
