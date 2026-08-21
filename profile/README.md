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
| Sign | Document signing, evidence and verification services. |

### Analytics integration

Each ONKA-built site is registered separately when Analytics is enabled. The collector is served from the site's own origin and sends only to same-origin paths. Analytics owns collection and reporting, and HQ reads fleet health and aggregate results. Portal composition and Forms aggregate delivery are pending integrations. CMS remains a separate schema boundary. Monitor supplies availability and Vercel deployment evidence but does not aggregate Analytics errors. Provision currently registers site metadata and known routes; client-site rewrite installation is still manual.

Anonymous measurement uses no persistent visitor identifier. Enhanced analytics is inactive until the client site has reviewed bilingual consent configuration and the visitor affirmatively enables the applicable category. ONKA does not create an identity graph across unrelated client organizations.

Client-specific delivery repositories live separately under `onka-clients`. Company records and internal governance live under `onka-inc`.

Ottawa and Montréal, Canada · [onkalabs.com](https://www.onkalabs.com)
