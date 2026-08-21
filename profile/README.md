<p align="center">
  <img src="onka-banner.png" alt="ONKA · Engineering Smarter Businesses" width="100%">
</p>

## ONKA Products and Platform

**Engineering Smarter Businesses.**

This organization contains ONKA's products, shared platform code, public web properties, and reusable technical systems.

## Platform systems

| System | Role |
|---|---|
| ONKA HQ | Internal control plane and relationship layer for companies, contacts, deals, projects and operations. |
| Analytics | First-party website and product analytics. Anonymous aggregate collection is the default; consent-aware visitors, sessions, events, funnels, campaigns, performance, replay, revenue and attribution can be enabled per client. |
| CMS | Structured content and publishing infrastructure for ONKA-built sites. |
| Forms | First-party form collection and routing. Analytics aggregate delivery is a pending integration. |
| Portal | Client-facing composition layer for approved ONKA services and reports. |
| Monitor | Fleet health, uptime and operational evidence for ONKA systems and client sites. |
| Provision | Idempotent registration and installation workflows across ONKA infrastructure. |
| Identity | Shared access foundation for approved client-facing systems. |
| [Sign](https://github.com/onkalabs/sign) | Standalone document execution. Authenticated senders upload PDFs, add any recipients by email, order signers, place fields, and send invitations. Signers use secure links without logging in. [Open Sign](https://sign.onkalabs.com) or read the [0.2.0 Alpha release](https://github.com/onkalabs/sign/releases/tag/sign-v0.2.0-alpha.0). |

### ONKA Sign alpha

ONKA Sign 0.2.0 Alpha is ONKA's standalone document-execution application, and ONKA is its first customer. It
extracts the signing engine formerly embedded in HQ and Pay into one production owner. The sender application
requires an approved ONKA login. A sender can upload one or more PDFs, enter any signer's email address, order
the recipients, and place signature, initials, name, signed-date, text, or checkbox fields on the pages. Every
signer receives a secure capability link and never creates an account.

Each PDF remains an individual document and can be downloaded separately after execution. A package groups
multiple documents so the assigned recipients can complete them in one signing flow. Sign does not require a
CRM company or client record for a standalone package. HQ can originate its own agreement packages through
the same engine, while client Portal surfaces expose only the relevant contract status and completed files.

The alpha also carries ordered signing, durable invitation receipts, scheduled reminders, append-only
evidence, retry-safe completion, independently verified Drive artifacts, tenant API keys, signed webhooks,
and explicit user-facing refusal states. Sign does not save reusable personal signatures and does not sign
automatically on anyone's behalf.

Alpha means the reviewed application and production data boundary are released while ONKA validates the full
real-document flow with Josh, Steven, and external email recipients before beta. It does not mean public
signup, automatic signing, or notarisation.

### Analytics integration

Each ONKA-built site is registered separately when Analytics is enabled. The collector is served from the site's own origin and sends only to same-origin paths. Analytics owns collection and reporting, and HQ reads fleet health and aggregate results. Portal composition and Forms aggregate delivery are pending integrations. CMS remains a separate schema boundary. Monitor supplies availability and Vercel deployment evidence but does not aggregate Analytics errors. Provision currently registers site metadata and known routes; client-site rewrite installation is still manual.

Anonymous measurement uses no persistent visitor identifier. Enhanced analytics is inactive until the client site has reviewed bilingual consent configuration and the visitor affirmatively enables the applicable category. ONKA does not create an identity graph across unrelated client organizations.

Client-specific delivery repositories live separately under `onka-clients`. Company records and internal governance live under `onka-inc`.

Ottawa and Montréal, Canada · [onkalabs.com](https://www.onkalabs.com)
