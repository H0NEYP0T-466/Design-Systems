# Security Policy

The **Design-Systems** team and community take the security and integrity of our codebase, interactive showcases, and documentation very seriously. We appreciate your efforts to responsibly disclose any security vulnerabilities you may identify.

---

## 🛡 Supported Versions

Because **Design-Systems** is a static web repository comprised of HTML5, CSS3, and lightweight client-side scripts, security updates and patches are continuously applied to the latest `master` branch.

| Branch / Release | Supported          |
| ---------------- | ------------------ |
| `master` (latest)| :white_check_mark: |
| Older revisions  | :x:                |

---

## 🚨 Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues, discussions, or social channels.**

If you discover a security vulnerability or potential threat in this repository, please report it via one of the following methods:

1. **GitHub Private Vulnerability Reporting (Preferred)**:
   - Go to the repository's [Security Tab](https://github.com/H0NEYP0T-466/Design-Systems/security).
   - Click on **"Report a vulnerability"** under Advisories.
   - Fill in the vulnerability details privately with the maintainers.

2. **Direct Email**:
   - Send an encrypted or direct email to the project maintainer at:
     **`fa-23-bscs-466@lgu.edu.pk`**
   - Use the subject line: `[SECURITY VULNERABILITY] Design-Systems - <Brief Summary>`

---

## 📋 What to Include in Your Report

To help us investigate and triage your report quickly, please include:
- A clear description of the vulnerability and its potential impact.
- Affected design system directories or files (e.g., `kraken/kraken.html`).
- Step-by-step instructions or a Minimal Reproducible Example (PoC).
- Any details on relevant browsers, environments, or network conditions.
- Suggestions or patches for remediating the vulnerability (optional).

---

## ⏱ Vulnerability Handling Policy & Response Timeline

When a report is received:

1. **Initial Acknowledgment**: We will acknowledge receipt of your vulnerability report within **48 hours**.
2. **Triage & Validation**: The maintainers will investigate and validate the findings within **5 business days**.
3. **Patch Development & Testing**: We will develop and test a remediation patch in a private fork or draft advisory.
4. **Resolution & Release**: A fix will be committed directly to `master`.
5. **Public Disclosure**: Once the fix is published and verified, credit will be given to the reporter (if desired) and a public security advisory will be published.

---

## 🔒 Scope & Common Considerations

Since this repository contains static HTML, CSS tokens, and client-side JavaScript demonstrations:
- **Cross-Site Scripting (XSS)**: Standalone HTML files must not execute untrusted user input or dynamic `eval` / `innerHTML` without sanitization.
- **Third-Party CDNs**: Web font imports and external assets must originate strictly from verified sources (e.g., Google Fonts, cdnjs).
- **Phishing / Impersonation**: Demonstrations of brand design systems are educational specimens and must not harvest credentials or simulate deceptive phishing interfaces.

Thank you for helping keep **Design-Systems** and the open-source community safe and secure!
