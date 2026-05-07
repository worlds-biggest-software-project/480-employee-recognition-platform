# Standards & API Reference

> Project: Employee Recognition Platform · Generated: 2026-05-07

## Industry Standards & Specifications

### ISO Standards

**ISO/IEC 27001:2022 — Information Security Management Systems**
- URL: https://www.iso.org/standard/27001
- The baseline information security certification expected by enterprise HR buyers when evaluating SaaS vendors. Requires a documented ISMS covering access controls, data classification, incident response, and supplier risk. All major recognition platforms cite ISO 27001 compliance in their security pages. An AI-native open-source platform should document its alignment with this standard to unblock enterprise procurement.

**ISO/IEC 27701:2019 — Privacy Information Management (extension to ISO 27001/27002)**
- URL: https://www.iso.org/standard/71670.html
- Extends ISO 27001 to cover personally identifiable information (PII) management, directly relevant to employee data (names, job titles, tenure, recognition events, reward redemptions, demographic attributes). Aligns with GDPR accountability requirements.

**ISO/IEC 42001:2023 — Artificial Intelligence Management Systems**
- URL: https://www.iso.org/standard/81230.html
- The first international standard for AI governance. Relevant to any platform using AI for recognition coaching, attrition prediction, or DEI analytics. Enterprise HR buyers in regulated industries are beginning to require AI management system documentation. Workhuman and peers reference ISO 42001 readiness in their 2026 compliance posture pages.

---

### W3C & IETF Standards

**RFC 6749 — The OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- The standard for delegated API authorisation. All major recognition platforms (Achievers, Motivosity, Bonusly, Workhuman) use OAuth 2.0 for their developer APIs. An open-source platform should support both `client_credentials` (system-to-system integrations) and `authorization_code` (user-delegated access) flows.

**RFC 8414 — OAuth 2.0 Authorization Server Metadata**
- URL: https://datatracker.ietf.org/doc/html/rfc8414
- Discovery document format for OAuth 2.0 servers. Allows API clients to discover token, authorisation, and JWKS endpoints automatically. Recommended for any platform publishing an OAuth-protected API.

**OpenID Connect Core 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- The de-facto single sign-on standard for enterprise SaaS. Recognition platforms must support OIDC (and typically SAML 2.0 as a fallback) to pass enterprise IT procurement. Okta, Azure AD, and Google Workspace are the dominant enterprise identity providers.

**RFC 7644 — System for Cross-domain Identity Management: Protocol (SCIM 2.0)**
- URL: https://datatracker.ietf.org/doc/html/rfc7644
- SCIM 2.0 is the standard for automated employee provisioning and de-provisioning across SaaS applications. When a new hire is added in Workday or BambooHR, SCIM pushes the employee record automatically to the recognition platform. SCIM also handles termination (account suspension) and attribute updates (department, manager). Implementing SCIM is a hard requirement for enterprise HR procurement.

**RFC 7643 — System for Cross-domain Identity Management: Core Schema (SCIM 2.0)**
- URL: https://datatracker.ietf.org/doc/html/rfc7643
- Defines the JSON data model for User and Group resources exchanged via SCIM. The `User` schema maps directly to the employee profile data consumed by a recognition platform (display name, email, manager, department, start date).

**RFC 7519 — JSON Web Token (JWT)**
- URL: https://datatracker.ietf.org/doc/html/rfc7519
- JWT is used for secure API tokens and SSO assertions in virtually all modern HR SaaS platforms. Relevant for API authentication, session management, and webhook payload verification.

**RFC 8288 — Web Linking**
- URL: https://datatracker.ietf.org/doc/html/rfc8288
- Defines the `Link` header for pagination in REST APIs. Recognition platforms returning lists of recognition events, users, or redemptions should implement cursor-based or page-based pagination using RFC 8288 Link headers.

**SAML 2.0 (OASIS Standard)**
- URL: https://docs.oasis-open.org/security/saml/v2.0/saml-core-2.0-os.pdf
- Still required by many enterprise identity providers as a fallback or primary SSO protocol. A production recognition platform must support SAML 2.0 SP-initiated SSO alongside OIDC.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1 (OAS 3.1)**
- URL: https://spec.openapis.org/oas/v3.1.0.html
- The standard format for documenting REST APIs. Achievers publishes its recognition API as a fully annotated OpenAPI/Swagger spec. An open-source platform should publish an OAS 3.1 document as the primary developer reference, enabling code generation (SDKs), automated testing, and API gateway integration.

**HR Open Standards — HR-JSON (v4.3)**
- URL: https://www.hropenstandards.org/standards
- The HR Open Standards Consortium maintains JSON and XML schemas for HR data exchanges across recruiting, payroll, benefits, compensation, screening, and timecard domains. While no dedicated recognition schema exists in v4.3, the `Person` and `Employment` schemas inform how employee identity and tenure data should be modelled in a recognition system. Free to download.

**JSON Schema (Draft 2020-12)**
- URL: https://json-schema.org/specification
- Used to validate the structure of API request and response payloads. Recognition event objects, user profiles, reward redemptions, and analytics responses should be defined with JSON Schema for machine-readable validation, documentation generation, and SDK support.

**Webhook Event Standard (CloudEvents v1.0)**
- URL: https://cloudevents.io/
- A CNCF specification for describing event data in a common format. Recognition events (bonus created, award approved, milestone triggered) are natural webhook payloads. Adopting CloudEvents format makes the platform's event stream composable with event-driven architectures, Zapier, and enterprise integration platforms.

---

### Security & Authentication Standards

**OWASP Top 10 (2021)**
- URL: https://owasp.org/www-project-top-ten/
- The baseline web application security checklist. Particularly relevant controls: broken access control (recognition events visible to wrong users), injection (recognition message text passed to AI models), security misconfiguration (HRIS API keys stored insecurely), and insufficient logging (recognition and redemption events must be auditable).

**OWASP API Security Top 10 (2023)**
- URL: https://owasp.org/www-project-api-security/
- Specific to API security posture. Key risks for a recognition API: Broken Object Level Authorization (accessing another employee's recognition history), Broken Function Level Authorization (non-admin triggering award approvals), Mass Assignment (overwriting points balances via API), and Unrestricted Resource Consumption (bulk API scraping of recognition data).

**NIST Cybersecurity Framework (CSF) 2.0**
- URL: https://www.nist.gov/cyberframework
- Widely adopted by US enterprise buyers as a security maturity benchmark. Recognition platforms handling reward financials (points with real-world monetary value) and employee PII must demonstrate alignment with CSF's Identify, Protect, Detect, Respond, and Recover functions.

**EU General Data Protection Regulation (GDPR)**
- URL: https://gdpr-info.eu/
- Applies to any platform processing personal data of EU employees. Key implications: legal basis for processing recognition data (legitimate interest or consent), right to erasure (deleting an employee's recognition history on request), data portability (exporting an employee's recognition record), and data minimisation (not storing demographic data beyond what is needed). All commercial platforms cite GDPR compliance.

**SOC 2 Type II**
- URL: https://us.aicpa.org/intl/soc/socsecurity
- The US enterprise procurement standard for SaaS security attestation, covering Security, Availability, Processing Integrity, Confidentiality, and Privacy. Expected by mid-market and enterprise HR buyers alongside ISO 27001. Overlaps >90% in control requirements with ISO 27001.

**EU AI Act (2024) — High-Risk AI Systems in Employment**
- URL: https://artificialintelligenceact.eu/
- The EU AI Act classifies AI systems used in employment contexts (hiring, performance evaluation, work monitoring) as high-risk, requiring conformity assessments, transparency obligations, and human oversight. An AI-native recognition platform using attrition prediction or DEI bias detection in EU deployments must document AI Act compliance, including logging, explainability, and human-in-the-loop requirements.

---

### MCP Server Specifications

**Model Context Protocol (MCP) v1.0**
- URL: https://modelcontextprotocol.io/
- Anthropic's open protocol for connecting AI agents to external data sources and tools via a standardised server interface. An AI-native recognition platform could expose an MCP server enabling AI assistants (Claude, Copilot, Gemini) to: query an employee's recognition history, trigger a recognition event, surface recognition gap alerts, or retrieve team culture analytics in response to natural language prompts. Relevant for the AI coaching and manager nudge features in the recommended feature scope.

---

## Similar Products — Developer Documentation & APIs

### Bonusly

- **Description:** SMB/mid-market peer recognition and micro-bonus platform with the highest adoption rates in the category. Full REST API with webhook support.
- **API Documentation:** https://docs.bonus.ly/reference
- **SDKs/Libraries:** Community Node.js SDK: https://github.com/jhgaylor/bonusly-node
- **Developer Guide:** https://help.bonus.ly/en/articles/1258685-getting-started-with-the-bonusly-api
- **Standards:** REST/JSON, API key + Bearer token authentication
- **Authentication:** Bearer token (API key passed as `Authorization: Bearer <token>` header or `access_token` query param)
- **Key Endpoints:** `GET/POST /api/v1/bonuses`, `GET /api/v1/analytics`, `GET /api/v1/users`, `POST /api/v1/webhooks`
- **Webhook Events:** `bonus.created`, `achievement_event.created`

---

### Achievers

- **Description:** Enterprise peer recognition and rewards platform, highest-ranked in G2's 2026 Best Software Products. Deep Workday HCM integration. Full OpenAPI 3.x documented developer portal.
- **API Documentation:** https://developer.achievers.com/docs
- **API Reference:** https://developer.achievers.com/reference/postachievement
- **Developer Guide:** https://developer.achievers.com/
- **Standards:** REST/JSON; OpenAPI/Swagger annotated (v5); OAuth 2.0
- **Authentication:** OAuth 2.0 — `client_credentials` for system integrations; `authorization_code` for user-delegated access
- **Test Environment:** https://example.uat.achievers.com
- **Key Endpoints:** `/api/v5/users`, `/api/v5/recognitions`, `/achievements`

---

### Motivosity

- **Description:** Mid-market recognition + continuous performance management platform with 500M+ global reward options and ThanksMatters Visa card. Public OAuth2 REST API with demo app on GitHub.
- **API Documentation:** https://help.motivosity.com/en/articles/9044579-motivosity-api
- **SDKs/Libraries:** Community Ruby client: https://github.com/jstanley0/mvclient; Demo app: https://github.com/motivosity-inc/Motivosity-Demo-app
- **Developer Guide:** https://www.motivosity.com/integrations/mv-api/
- **Standards:** REST/JSON; OAuth 2.0
- **Authentication:** OAuth 2.0 (standard authorisation code flow)
- **Base URL:** `https://app.motivosity.com/api/v2`
- **Key Endpoints:** Appreciations (recognition events), Users, Kiosk terminal

---

### Awardco

- **Description:** Enterprise recognition platform with exclusive Amazon Business partnership, offering the largest reward network in the world at zero markup. API key–scoped REST API.
- **API Documentation:** https://api.awardco.com/api and https://code.awardco.com/api
- **Standards:** REST/JSON; API key authentication
- **Authentication:** API key in request header; permission scoped per key; `X-Partner-Id` header for white-label/reseller integrations
- **Amazon Business Integration:** https://www.awardco.com/integrations/amazon-business

---

### Nectar HR

- **Description:** Simple, values-centric peer recognition platform for remote and hybrid SMB/mid-market teams. Open API with limited endpoints.
- **API Documentation:** https://help.nectarhr.com/en/articles/10770969-open-api
- **Standards:** REST/JSON
- **Authentication:** API key
- **Note:** API is currently limited in endpoint coverage; not suitable for deep custom integrations.

---

### O.C. Tanner Culture Cloud

- **Description:** Enterprise recognition platform with the longest heritage in the category (since 1927). Deepest native HRIS integrations (Workday, SAP SuccessFactors, Oracle HCM, UKG, ADP, DayForce). New developer portal in 2026.
- **API Documentation:** https://www.octanner.com/products/integrations (Developer Portal)
- **Standards:** REST/JSON; open API with integration-as-a-service model
- **Authentication:** Not publicly documented; enterprise onboarding required
- **Notable Integrations:** Workday, SAP SuccessFactors, Oracle Cloud HCM, UKG, ADP, DayForce, Paychex, Paylocity, Microsoft Teams, Slack, Outlook, Gmail, SharePoint, Intune SDK

---

### Vantage Circle

- **Description:** Global employee engagement suite (recognition, wellness, surveys, perks) with a Microsoft 365 Copilot agent integration and native ADP Workforce Now connector.
- **API Documentation:** Not prominently publicly documented; contact vendor
- **Notable Integration:** Microsoft 365 Copilot agent (recognition recommendations embedded in Copilot workflows)
- **Standards:** REST/JSON; ADP Marketplace certified
- **Authentication:** Not publicly documented

---

### Meeds DAO (Open Source Reference)

- **Description:** Apache 2.0 open-source employee recognition platform with blockchain-based reward wallets (ERC-20 tokens). Technology stack: Vue.js, Vuetify, Java, Docker. Only meaningful open-source option in the category.
- **API Documentation:** https://docs.exoplatform.org/guide/openapi/kudos (ExoPlatform variant)
- **Source Code:** https://github.com/Meeds-io/meeds
- **SDKs/Libraries:** Docker-deployable; REST API built in
- **Standards:** REST/JSON; OpenAPI; ERC-20 (Ethereum token standard)
- **Authentication:** Standard session/token auth; blockchain wallet for token operations
- **Connectors:** GitHub, Slack, Twitter/X, Salesforce

---

### Workday HCM (HRIS Reference)

- **Description:** The dominant enterprise HRIS platform. Recognition platforms must integrate with Workday to access and sync the employee directory and trigger milestone automation. The Workday Marketplace lists certified recognition platform connectors.
- **API Documentation:** https://developer.workday.com/
- **Marketplace:** https://marketplace.workday.com/
- **Standards:** REST/JSON and SOAP; OAuth 2.0; SCIM 2.0 provisioning
- **Authentication:** OAuth 2.0 with Workday-issued client credentials
- **Notable Integrations Listed:** Workhuman, Achievers, O.C. Tanner, Motivosity, Awardco

---

### BambooHR (HRIS Reference)

- **Description:** The dominant HRIS for SMB/mid-market organisations. Most recognition platforms list BambooHR as their first or primary HRIS integration. Employee directory, start dates, and manager relationships are synced to power recognition automation.
- **API Documentation:** https://documentation.bamboohr.com/docs
- **Standards:** REST/JSON; API key authentication
- **Authentication:** Basic auth with API key
- **Webhook Support:** Yes — employee lifecycle events (hire, termination, field change)

---

## Notes

**Emerging: MCP Servers for HR Systems**
As of early 2026, multiple HRIS vendors are beginning to publish MCP servers (Anthropic's Model Context Protocol) to allow AI agents to query employee data. A recognition platform with a published MCP server would be natively composable with AI assistant workflows in Claude, Copilot, and other agentic frameworks — this is a meaningful differentiation opportunity that no current recognition platform has implemented at depth.

**Gap: No Industry-Standard Recognition Event Schema**
The HR Open Standards Consortium's v4.3 specification covers recruiting, payroll, benefits, compensation, and timecard data but does not include a standard schema for recognition events or reward redemptions. An open-source platform that publishes a well-designed recognition event JSON Schema and contributes it to HR Open Standards could become the de-facto standard for the category.

**Gap: CloudEvents Adoption in HR SaaS**
Recognition platforms uniformly use proprietary webhook payload formats. Adopting the CloudEvents 1.0 specification for outbound webhook events would make a recognition platform's event stream natively composable with enterprise integration platforms (MuleSoft, Boomi, Zapier) and serverless event routers (AWS EventBridge, Azure Event Grid) without custom adapter work.
