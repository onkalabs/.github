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
| [Sign](https://github.com/onkalabs/sign) | Production alpha for document execution. Authenticated senders prepare multi-document packages, order signers, place fields, and send invitations. Signers use secure links without logging in. Execution evidence is append-only, completed PDFs are hash-verified in Drive, and client Portal surfaces show contract status rather than the Sign product. [Open Sign](https://sign.onkalabs.com). |

### ONKA Sign alpha

ONKA Sign 0.1.0 Alpha is ONKA's standalone agreement-execution system and ONKA is its first customer. It
extracts the signing engine formerly embedded in HQ and Pay into one production owner. The sender application
requires an approved ONKA login. Every signer receives a capability link and never creates an account.

The alpha supports ordered multi-document packages, ordered signers, signature, initials, date and text
fields, durable invitation receipts, scheduled reminders, append-only evidence, retry-safe completion,
independently verified Drive artifacts, tenant API keys, signed webhooks, an HQ read projection, and a
contract-only Portal projection. The former Pay signing route is retired.

Alpha means ONKA is validating the complete flow on its own agreements before broader client use. It does not
mean public signup, a general document editor, or notarisation.

### Analytics integration

Each ONKA-built site is registered separately when Analytics is enabled. The collector is served from the site's own origin and sends only to same-origin paths. Analytics owns collection and reporting, and HQ reads fleet health and aggregate results. Portal composition and Forms aggregate delivery are pending integrations. CMS remains a separate schema boundary. Monitor supplies availability and Vercel deployment evidence but does not aggregate Analytics errors. Provision currently registers site metadata and known routes; client-site rewrite installation is still manual.

Anonymous measurement uses no persistent visitor identifier. Enhanced analytics is inactive until the client site has reviewed bilingual consent configuration and the visitor affirmatively enables the applicable category. ONKA does not create an identity graph across unrelated client organizations.

Client-specific delivery repositories live separately under `onka-clients`. Company records and internal governance live under `onka-inc`.

Ottawa and Montréal, Canada · [onkalabs.com](https://www.onkalabs.com)
