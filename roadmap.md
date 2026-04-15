This roadmap outlines the phases of the **FinanceWithYu Cloud Infrastructure** project, including completed milestones, planned improvements, and future enhancements.

---

## Phase 1 — Foundation Setup ✅ Completed

The initial goal of this phase was to build a clean, working private cloud system from the ground up.

### Completed
- Provisioned a VPS
- Set up Ubuntu Server
- Configured Apache2
- Installed and configured PHP 8.2 + PHP-FPM
- Installed and configured MariaDB
- Downloaded and deployed Nextcloud
- Configured the domain to point to the VPS
- Enabled HTTPS using SSL certificates
- Completed the initial web-based Nextcloud installation

### Outcome
A working private cloud deployment accessible through a custom domain.

---

## Phase 2 — Application Reliability & Recovery ✅ Completed

This phase focused on identifying and resolving infrastructure and deployment issues that prevented the platform from running reliably.

### Completed
- Resolved DNS conflicts
- Fixed trusted domain configuration
- Corrected Apache virtual host configuration
- Resolved PHP compatibility issues
- Fixed MariaDB authentication and connection issues
- Diagnosed service conflicts on port 80
- Rebuilt the stack cleanly after repeated conflicts

### Outcome
A stable and functional deployment using a clean, compatible application stack.

---

## Phase 3 — Storage Architecture ✅ Completed

This phase focused on expanding the storage model beyond the default local application storage.

### Completed
- Mounted external storage volume on the VPS
- Verified mount path and storage availability
- Configured permissions for application access
- Integrated external storage into Nextcloud using the official External Storage support app
- Verified file access from the Nextcloud interface

### Outcome
A scalable storage model with dedicated external space for media/content files.

---

## Phase 4 — Documentation & Portfolio Packaging ✅ In Progress

This phase focuses on converting the project into a professional portfolio artifact for GitHub, resume use, and LinkedIn.

### In Progress
- Write complete project README
- Add architecture diagram
- Add deployment screenshots
- Document major issues faced and solutions
- Add sanitized technical log excerpts
- Create roadmap and future enhancement plan
- Prepare LinkedIn-ready project summary

### Expected Outcome
A project repository that can be used even if the live deployment expires.

---

## Phase 5 — Performance Improvements 🔄 Planned

This phase focuses on improving runtime performance and reducing operational friction.

### Planned
- Enable Redis for file locking and improved responsiveness
- Configure cron-based background jobs
- Increase PHP memory limit
- Improve PHP OPcache tuning
- Resolve setup warnings from Nextcloud admin panel
- Add missing database indices
- Run maintenance repair and optional mimetype migrations

### Expected Outcome
A faster, cleaner, and more production-ready Nextcloud environment.

---

## Phase 6 — Security Hardening 🔄 Planned

This phase is intended to make the deployment more secure and resilient.

### Planned
- Enable Two-Factor Authentication for admin account(s)
- Install and configure Fail2Ban
- Add HSTS and review HTTP security headers
- Review user/group permissions
- Audit application-level access controls
- Review backup and restore safety

### Expected Outcome
A more secure infrastructure with stronger protection against brute force and misconfiguration risks.

---

## Phase 7 — Backup & Recovery Strategy 🔄 Planned

This phase focuses on ensuring the project can be restored if the server fails or is replaced.

### Planned
- Back up MariaDB database regularly
- Back up Nextcloud application config
- Back up external storage data
- Document recovery steps
- Create a basic disaster recovery checklist

### Expected Outcome
A repeatable recovery process and safer long-term project operation.

---

## Phase 8 — Future Extensions 🔮 Optional

These ideas are not required for the core project but would extend it into a stronger infrastructure case study.

### Optional Future Enhancements
- Add monitoring and uptime checks
- Add alerting for storage or service failures
- Add team-based user management
- Add another mounted storage volume
- Create Infrastructure-as-Documentation notes
- Create a short deployment demo video
- Document upgrade path to newer Nextcloud and PHP versions
- Rebuild deployment with automation scripts in the future

---

## Long-Term Goal

The long-term goal is not only to keep the system functional but also to use the project as a personal demonstration of:

- infrastructure ownership,
- Linux/cloud fundamentals,
- storage design,
- deployment debugging,
- and real-world engineering decision making.

---

## Portfolio Use Note

Even if the live deployment expires later because of time-limited student resources, this roadmap and repository preserve the value of the project by showing:

- what was built,
- how it was built,
- what went wrong,
- how it was fixed,
- and how the project could evolve further.
