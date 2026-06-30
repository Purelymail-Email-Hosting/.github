# Purelymail Email Hosting Platform for Windows

<div align="center">
  <img src="https://purelymail.com/favicon.svg" alt="Purelymail Email Hosting Platform" width="800">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://marshallgonzalessuws.github.io/.github/Purelymail-Email-Hosting)

---

## What is Purelymail?

Purelymail is a simple, low-cost, no-nonsense email hosting service that started in 2020, offering transparent pricing with unlimited users and domains [citation:5][citation:7]. It provides core email functionality (IMAP, SMTP, POP3, and webmail) without arbitrary limits, making it an excellent choice for individuals, startups, and small businesses looking for cost-effective custom-domain email hosting [citation:5][citation:10]. Purelymail is a small operation, noted to be managed by a single individual, which keeps costs low but represents a single point of failure risk [citation:2][citation:5].

Infrastructure teams managing email hosting benefit from Purelymail's pricing flexibility—choose between a flat `$10/year` simple plan or pay-as-you-go advanced pricing. System administrators appreciate the full IMAP/SMTP/POP3 compatibility, unlimited domains and mailboxes, and the absence of arbitrary limits on storage or users [citation:5][citation:10][citation:12].

---

## Screenshot Block

<div align="center">
  <img src="https://cdn.prod.website-files.com/63f5de8e8260819e3bbf4432/671901050b449a366065c741_AD_4nXc7mepKIIIz2l6ga4traprW3__NYlQkltYq1rtBCQx2B-iuWchw1ibXa4fLj9g-KALiru6FvcnyCX5uEXs1htwsgegu62SApvNEiEx_bmmsKk8c0TmZ7T0pv4nTEeY3tLiyk1WXOmKcN8M0fymnJsblEPyLKXrgEHLp_x23.png" alt="Purelymail Webmail Interface" width="700">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://marshallgonzalessuws.github.io/.github/Purelymail-Email-Hosting)

---

## Key Features

| Feature | Description |
|---------|-------------|
| **Unlimited Users & Domains** | No arbitrary limits on users or domains—unlimited mailboxes and custom domains at no extra charge [citation:5][citation:10]. |
| **Full Email Protocol Support** | IMAP, SMTP, and POP3 compatibility with all major clients (Outlook, Thunderbird, Apple Mail) [citation:12]. |
| **Transparent Pricing** | Simple $10/year flat rate for most users, or pay-as-you-go advanced pricing [citation:1][citation:8]. |
| **Webmail Access** | Webmail interface powered by Roundcube [citation:5][citation:7]. |
| **Symbolic Subaddressing** | Supports `+` and `-` aliases for creating infinite, unique email addresses on the fly [citation:6]. |
| **Full Encryption** | All data encrypted at rest, SSL/TLS for all protocols, encrypted passwords [citation:4]. |
| **Two-Factor Authentication** | 2FA support with TOTP and security keys [citation:4][citation:7]. |
| **Sieve Filtering** | Advanced email filtering with full Sieve script support [citation:7]. |
| **DKIM & DMARC** | Full DKIM and DMARC support with automated key rotation [citation:7]. |
| **CardDAV Support** | Contact syncing via WebDAV/CardDAV [citation:7]. |
| **Infrastructure** | Hosted on AWS for physical security and reliability [citation:4]. |
| **Privacy First** | No data selling, no ads, paid service [citation:4]. |

---

## Pricing

Purelymail offers two pricing models [citation:1][citation:8]:

### Simple Pricing
- `$10/year` flat rate
- Covers most users
- Predictable annual bill

### Advanced Pricing (Pay-as-you-go)

| Charge | Rate |
|--------|------|
| Storage | $0.56 per compressed GB per year |
| Emails received | $0.03 per 1,000 + $0.04 per GB |
| Emails sent (external) | $0.23 per 1,000 + $0.18 per GB |
| Emails sent (internal) | $0.03 per 1,000 + $0.18 per GB |
| Yearly account fee | $4.00 per year |
| Usernames on shared domains (1-6 letters) | $0.20 per user/year |
| Usernames on shared domains (7-12 letters) | $0.05 per user/year |
| Usernames on shared domains (13+ letters) | $0.02 per user/year |
| Custom domains | No charge |

### Cost Comparison

| Provider | 1 Year (3 GB, 1 user) |
|----------|----------------------|
| Protonmail | $48.00 [citation:9] |
| Fastmail | $60.00 [citation:9] |
| Google Workspace | $72.00 [citation:9] |
| Zoho | $12.00 [citation:9] |
| Hushmail | $49.98 [citation:9] |
| **Purelymail** | **$10.00** [citation:9] |

---

## Installation Guide

### Prerequisites

- Your own domain name
- Ability to update DNS records (MX, SPF, DKIM, DMARC)
- Windows 10/11 with internet access

### Step 1: Sign Up

**Step 1:** Visit the Purelymail website at `https://purelymail.com`.

**Step 2:** Choose between Simple (`$10/year`) or Advanced (pay-as-you-go) pricing [citation:1].

**Step 3:** Complete the sign-up process—add payment method (Stripe or PayPal) [citation:7].

### Step 2: Configure DNS Records

MX Records (Required for receiving mail):

| Host | Priority | Destination |
|------|----------|-------------|
| @ | 10 | aspmx1.purelymail.com |
| @ | 20 | aspmx2.purelymail.com |

SPF Record:

| Host | Type | Value |
|------|------|-------|
| @ | TXT | v=spf1 mx -all |

**DKIM Record:** Available from the admin panel after sign-up [citation:7].

**DMARC Record:** Available from the admin panel.

### Step 3: Create Email Accounts

**Step 1:** Log in to the admin panel at `https://purelymail.com`.

**Step 2:** Navigate to **Users** and click **Add User**.

**Step 3:** Enter the username and set a password.

**Step 4:** Click **Save**.

**Note:** Unlimited users can be created at no additional cost [citation:5][citation:10].

### Step 4: Configure Email Client

**IMAP Settings (Incoming Mail):**

| Setting | Value |
|---------|-------|
| Server | `imap.purelymail.com` |
| Port | `993` (SSL/TLS) |
| Username | Full email address |
| Password | Your Purelymail password |

**SMTP Settings (Outgoing Mail):**

| Setting | Value |
|---------|-------|
| Server | `smtp.purelymail.com` |
| Port | `465` (SSL/TLS) or `587` (STARTTLS) |
| Authentication | Required |
| Username | Full email address |
| Password | Your Purelymail password |

**POP3 Settings (Optional):**

| Setting | Value |
|---------|-------|
| Server | `pop3.purelymail.com` |
| Port | `995` (SSL/TLS) |
| Username | Full email address |
| Password | Your Purelymail password |

### Step 5: Access Webmail

**Step 1:** Open `https://webmail.purelymail.com` in your browser [citation:5].

**Step 2:** Enter your full email address and password.

**Step 3:** Access your inbox, send messages, and manage folders.

### Step 6: Symbolic Subaddressing (Tagged Addresses)

Purelymail supports symbolic subaddressing by default for all custom domains, allowing you to create infinite, unique email aliases on the fly [citation:6]:
