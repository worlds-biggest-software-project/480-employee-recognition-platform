# Employee Recognition Platform — Feature & Functionality Survey

> Candidate #480 · Researched: 2026-05-07

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Workhuman Social Recognition | Enterprise SaaS | Commercial (subscription, enterprise pricing) | https://www.workhuman.com/platform/social-recognition/ |
| Bonusly | SMB/mid-market SaaS | Commercial ($3–$5 PEPM) | https://bonusly.com/ |
| Achievers | Enterprise SaaS | Commercial (enterprise pricing) | https://www.achievers.com/ |
| O.C. Tanner Culture Cloud | Enterprise SaaS | Commercial (enterprise pricing) | https://www.octanner.com/products/culture-cloud |
| Kudos | Mid-market SaaS | Commercial (subscription) | https://www.kudos.com/ |
| Motivosity | Mid-market SaaS | Commercial (~$2–$5 PEPM) | https://www.motivosity.com/ |
| Nectar HR | SMB/mid-market SaaS | Commercial ($5–$6 PEPM, $4k annual minimum) | https://nectarhr.com/ |
| Awardco | Mid-market/enterprise SaaS | Commercial (subscription) | https://www.awardco.com/ |
| Matter | SMB Slack/Teams-native SaaS | Commercial (freemium; paid per active user) | https://matterapp.com/ |
| Assembly | SMB/mid-market SaaS | Commercial (freemium; $2.80–$4.50 PEPM) | https://joinassembly.com/ |
| Vantage Circle | Mid-market/enterprise SaaS | Commercial (subscription) | https://www.vantagecircle.com/ |
| Meeds DAO | Open-source / Web3 | Open source (Apache 2.0 / ERC-20 token model) | https://github.com/Meeds-io/meeds |

---

## Feature Analysis by Solution

### Workhuman Social Recognition

**Core features**
- Peer-to-peer and manager-to-employee recognition with social feed, badges, and point awards
- Public social recognition feed mimicking social media, supporting text, images, video, and badges
- Global reward catalogue (gift cards, merchandise, experiences, charitable donations)
- Service milestone and anniversary automation with personalised messages
- Culture, participation, and DEI analytics dashboards

**Differentiating features**
- Human Intelligence engine: the only platform to have built a recognition-specific large language model trained on 25+ years of recognition data
- Skills-linked recognition insights — surfaces what skills employees are being recognised for and how skill signals evolve over time
- Attrition and retention risk prediction derived from recognition frequency and pattern data
- Conversational AI assistant (Workhuman iQ) for real-time CHO and HR queries about skills, DEI, engagement
- Recognition-to-performance correlation analytics tied directly to business outcome data

**UX patterns**
- Enterprise portal with dedicated mobile app (iOS/Android)
- Slack, Teams, and Outlook plugins bring recognition into existing workflow without app switching
- Progressive disclosure: surface-level recognition requires minimal clicks; deep analytics are behind a separate iQ console
- Admin-configurable recognition categories aligned to company values

**Integration points**
- Bidirectional certified Workday HCM connector
- Slack, Microsoft Teams, Outlook integrations
- HRIS connectors: BambooHR, ADP, Oracle, SAP SuccessFactors
- Open API for custom integrations
- Workday Marketplace listed partner

**Known gaps**
- Very high price point, effectively locking out SMB/mid-market
- Onboarding complexity and implementation timelines reported as long (enterprise-grade)
- Some users report the reward catalogue redemption UX is cumbersome compared to simpler competitors
- Non-enterprise analytics features are not available in lower tiers

**Licence / IP notes**
- Proprietary commercial SaaS. Human Intelligence engine and iQ LLM are Workhuman IP. No open-source components exposed.

---

### Bonusly

**Core features**
- Micro-bonus peer-to-peer recognition with configurable monthly point allowances
- Public recognition feed with emoji reactions and social commenting
- Broad reward catalogue: gift cards, charitable donations, prepaid Visa/Mastercard, cash, swag
- HRIS sync (BambooHR, Workday, ADP) for employee directory and milestone automation
- Birthday and work anniversary automatic recognitions

**Differentiating features**
- Highest adoption rates in category (cited in multiple comparison reviews) driven by frictionless micro-bonus UX
- AI-powered dashboards surfacing recognition quality, trends, and participation gaps
- Smart coaching prompts for managers surfaced during 1:1 meeting workflows
- Zapier integration enabling low-code automation of recognition triggers from third-party events
- Sandbox/test environment available to developers via public REST API

**UX patterns**
- Conversational, micro-transaction UX: sending a bonus feels like a social media post
- Deep Slack and Teams integration so recognition happens inside chat without context switching
- Manager coaching prompts are surfaced in-app during 1:1 check-in workflows
- Simple onboarding; no dedicated implementation team required for SMB deployments

**Integration points**
- REST API at `https://bonus.ly/api/v1/` with full CRUD for bonuses, users, analytics, redemptions
- Webhooks: `bonus.created` and `achievement_event.created` event types
- Slack, Microsoft Teams, Google Chat native integrations
- HRIS: BambooHR, Workday, ADP, Zenefits, Okta/OneLogin for SSO
- Zapier for no-code automation

**Known gaps**
- Analytics depth is limited compared to Workhuman — no recognition-to-attrition modelling
- No performance management or check-in features natively (relies on integrations)
- Reward catalogue is US-centric; global reward fulfilment is weaker than Awardco or Motivosity
- No built-in DEI analytics or recognition equity reporting

**Licence / IP notes**
- Proprietary commercial SaaS. Public REST API is available; no open-source SDK published.

---

### Achievers

**Core features**
- Peer-to-peer and manager-to-employee recognition
- Structured nomination and awards programmes
- Points-based reward catalogue (gift cards, experiences, merchandise)
- AI-driven personalisation that adapts recognition prompts and feed ranking
- Engagement pulse surveys integrated with recognition data

**Differentiating features**
- Built directly into Workday HCM (April 2026 partnership), so every recognition event adds to the employee's permanent HCM record
- Frontline-focused feedback with built-in AI support for field and deskless workers
- Highest G2 ranking in Best Software Products 2026
- Open REST API (v5, OpenAPI/Swagger annotated) with a dedicated developer portal at `developer.achievers.com`
- Two OAuth flows: `client_credentials` for system integrations and `authorization_code` for user-delegated access

**UX patterns**
- Enterprise admin portal with configurable values, budget controls, and programme rules
- Mobile-first for deskless and frontline recognition
- Dedicated developer sandbox at `example.uat.achievers.com`

**Integration points**
- OpenAPI v5 REST API documented at `developer.achievers.com`
- Native Workday HCM connector (embedded, bidirectional)
- Slack, Teams integrations
- HRIS connectors: SAP SuccessFactors, ADP, Oracle HCM

**Known gaps**
- AI personalisation is newer and less mature than Workhuman's iQ engine
- Less SMB-friendly pricing and onboarding than Bonusly or Matter
- No open-source SDK; API documentation is comprehensive but developer community is small

**Licence / IP notes**
- Proprietary commercial SaaS. API documentation is public and the spec is annotated with Swagger/OpenAPI.

---

### O.C. Tanner Culture Cloud

**Core features**
- Peer-to-peer recognition, manager spotlight, and nomination programmes
- Yearbook celebrations for milestones (printed and digital, with curated gift selections)
- Multiple Stores feature: separate storefronts with own points banks for lifestyle, company, holiday, and manager stores
- AI Insights (Beta): manager-facing AI-generated pattern analysis highlighting cross-team connections and recognition gaps
- LinkedIn social sharing for public milestone recognition

**Differentiating features**
- Longest-tenured enterprise recognition vendor (physical awards heritage since 1927)
- Yearbook milestone product is unique: teammates contribute personalised notes, produced as printed keepsakes
- Deepest native integrations with enterprise HR stacks: Workday, SAP SuccessFactors, Oracle HCM, UKG, ADP, DayForce, Paychex, Paylocity
- Culture Cloud for Intune SDK enabling BYOD mobile access under corporate MAM policies
- New Developer Portal (2026) with case studies, sample code, and testing tools

**UX patterns**
- Enterprise-grade, configurable recognition categories tied to organisational values
- Mobile app re-designed for ease of use (employees 4x more likely to recognise peers with mobile access)
- Dedicated Intune SDK for healthcare and regulated industry deployments
- 0.45-year average ROI reported from client data

**Integration points**
- Open API with integration-as-a-service model for custom connectors
- Developer Portal at octanner.com
- Native HRIS integrations: Workday, SAP SuccessFactors, Oracle Cloud HCM, UKG, ADP, DayForce, Paychex, Paylocity
- Microsoft Teams, Slack, Outlook, Gmail, SharePoint, browser extension

**Known gaps**
- Physical awards heritage can make the platform feel heavy for organisations that want lightweight digital-only recognition
- AI Insights is still in Beta — less mature than Workhuman iQ
- Pricing is enterprise-tier; not suitable for SMB

**Licence / IP notes**
- Proprietary commercial SaaS. O.C. Tanner's Yearbook product and related physical award fulfilment are proprietary. Developer portal documentation is public.

---

### Kudos

**Core features**
- Social-style peer recognition feed with values/category tags
- Manager-driven awards and nomination programmes
- Milestone celebrations with virtual cards
- Incentive programmes to promote targeted behaviours
- Optional points-based reward catalogue

**Differentiating features**
- Organisational network analysis (ONA): recognition network maps showing which teams interact and recognise each other, revealing collaboration patterns
- Culture scoring: team-level culture health scores derived from recognition and sentiment signals
- Early warning indicators for disengagement, surfaced to HR leaders and managers
- Clean, training-free UX cited as key adoption driver
- AI recognition assistant for message suggestions

**UX patterns**
- Lightweight, social-media-style feed requires no training for employees
- Recognition messages enriched with tags, values, or categories
- Deep analytics console for HR business partners distinct from the employee-facing feed
- Available on mobile, Slack, and Microsoft Teams

**Integration points**
- Slack and Teams integrations
- HRIS integrations for employee directory sync
- UKG Marketplace listed partner (native UKG integration)
- API available for custom integrations (documentation via docs.exoplatform.org for ExoPlatform variant)

**Known gaps**
- Reward catalogue is optional and less developed than Bonusly or Awardco
- API documentation for the main Kudos.com product is not publicly detailed (partner integrations require vendor engagement)
- No native performance management or survey features

**Licence / IP notes**
- Proprietary commercial SaaS. UKG Marketplace integration is certified. No open-source components.

---

### Motivosity

**Core features**
- Peer-to-peer and manager-to-employee recognition
- Milestone automation for birthdays and anniversaries
- ThanksMatters Visa prepaid card as a universal reward vehicle
- Continuous performance management tools: feedback, goal-setting, manager 1:1 check-ins
- Kiosk integration for deskless/frontline workers

**Differentiating features**
- Largest global reward ecosystem: 500 million+ reward options in 200+ countries
- ThanksMatters Visa card allows employees to spend recognition points anywhere Visa is accepted — eliminating catalogue limitations
- Integrated continuous performance management (not just recognition), including OKRs, manager check-ins, and real-time feedback
- 100/100 score for dashboards and reporting in independent benchmarks
- Kiosk API endpoint enabling tablet-based recognition terminals in factories, warehouses, and hospitals

**UX patterns**
- Modular platform: organisations can deploy recognition, performance, or surveys independently
- Slack and Teams integrations for in-chat recognition
- Manager coaching prompts surfaced in dashboard when team engagement drops
- Kiosk mode for frontline workers who lack desk or mobile access

**Integration points**
- OAuth2 REST API at `https://app.motivosity.com/api/v2`
- GitHub demo application published at `github.com/motivosity-inc/Motivosity-Demo-app`
- HRIS integrations: BambooHR, Workday, ADP
- Slack, Teams integrations
- Kiosk terminal endpoint for hardware-based recognition

**Known gaps**
- Platform breadth (performance + recognition + surveys) can make initial configuration complex
- Some user reviews cite UI density as a drawback for employees who only want simple recognition
- No native DEI analytics comparable to Workhuman

**Licence / IP notes**
- Proprietary commercial SaaS. Public API with OAuth2; demo app on GitHub under open licence.

---

### Nectar HR

**Core features**
- Peer-to-peer recognition tied to company values
- Manager-to-employee recognition
- Birthday and work anniversary automation
- HRIS integration for directory sync
- Nominations programme and swag store (Premium tier)

**Differentiating features**
- High-adoption, values-centric recognition with the simplest interface in the category
- Organisational network analysis showing which teams recognise each other most
- Internal communications tool bundled alongside recognition
- Multi-language support (Premium tier)

**UX patterns**
- Minimal, high-speed recognition UX — designed for sub-30-second recognition events
- Clean interface with low configuration burden — suitable for remote and hybrid teams
- Account manager included even at the base Plus plan

**Integration points**
- Open API (limited endpoints; documentation at `help.nectarhr.com/en/articles/10770969-open-api`)
- HRIS: BambooHR, Workday, ADP, Gusto, Rippling
- Slack, Teams integrations
- SSO via Okta, Azure AD, Google

**Known gaps**
- Analytics depth explicitly called out as a gap in user reviews — no recognition-to-attrition modelling
- API has limited endpoints; not suitable for complex custom integrations
- No performance management, survey, or continuous feedback features
- Minimum annual spend of $4,000 limits micro-SMB adoption
- Manager-driven recognition and nomination workflows less developed than enterprise competitors

**Licence / IP notes**
- Proprietary commercial SaaS. API is public but documented as limited. No open-source exposure.

---

### Awardco

**Core features**
- Peer-to-peer and manager-to-employee recognition
- Amazon Business integration: access to the full Amazon product catalogue as reward fulfilment (zero markup, free shipping)
- Points-based reward system with eCards
- Workday native bidirectional integration
- Slack and Teams integrations

**Differentiating features**
- First and only employee recognition platform with an Amazon Business partnership (since 2017), offering the world's largest reward network with no catalogue markup
- Real-time order tracking and delivery updates for Amazon-fulfilled rewards
- Partner ID system for white-label and reseller deployments
- API key–based authentication with permission scoping at the key level

**UX patterns**
- Reward redemption through familiar Amazon shopping experience reduces friction versus proprietary catalogues
- Admin portal for budget management and programme configuration
- Mobile accessible

**Integration points**
- REST API at `https://api.awardco.com/api` with JSON responses; API key authentication
- Partner header (`X-Partner-Id`) for reseller/white-label scenarios
- Workday certified bidirectional connector
- Slack, Teams integrations
- Amazon Business fulfilment API (proprietary partnership)

**Known gaps**
- Amazon-centric reward model does not suit markets where Amazon is not dominant or delivers poorly
- Recognition and analytics features are less differentiated than Workhuman or Achievers
- No AI recognition coaching or predictive analytics
- No built-in survey or performance management tools

**Licence / IP notes**
- Proprietary commercial SaaS. Amazon Business partnership is exclusive and proprietary. API documentation public.

---

### Matter

**Core features**
- Peer-to-peer kudos recognition via Slack and Teams bots
- Customisable kudos card templates for different recognition contexts
- Feedback Friday: automated weekly recognition prompt encouraging end-of-week kudos
- Coin-based reward system resetting weekly to encourage habitual use
- Birthday and work anniversary automation with self-service employee information updates

**Differentiating features**
- Billing is per channel member, not workspace headcount — reduces cost for partial rollouts
- Incentivised pulse surveys with rewards to drive survey participation
- Recognition analytics automatically pulled into Slack/Teams without leaving the chat interface
- Notable enterprise customers despite SMB positioning (Sephora, Petco, Shell, Siemens, Microsoft)
- 30-day free trial with full feature access

**UX patterns**
- Entirely Slack/Teams-native: no separate app login required
- Feedback Friday creates a ritual, habit-forming recognition cadence
- Weekly coin reset prevents point hoarding and drives ongoing participation
- Minimal setup for IT; no enterprise implementation timeline

**Integration points**
- Native Slack Marketplace and Teams app integrations
- Gift card and prepaid Visa/Mastercard reward fulfilment
- Custom-branded rewards for company-specific incentives
- No published public REST API; platform is primarily channel-native

**Known gaps**
- No standalone web app — entirely dependent on Slack/Teams
- Limited analytics depth compared to enterprise platforms
- No HRIS integration beyond basic employee profile sync
- No performance management, goal-setting, or survey features beyond incentivised pulse questions
- No public developer API

**Licence / IP notes**
- Proprietary commercial SaaS. No open-source components. API is not publicly documented.

---

### Assembly

**Core features**
- Peer-to-peer shoutouts, badges, and nomination programmes
- Automated birthday and work anniversary celebrations
- Points-based rewards: gift cards, swag, and custom branded rewards
- Pulse surveys, eNPS tracking, and manager 1:1 templates
- Dora Hub: AI layer analysing recognition patterns and nudging managers when engagement drops

**Differentiating features**
- Highest G2 rating in the employee recognition category (4.9/5 from 3,000+ reviews)
- AI nudges proactively alert managers before disengagement becomes visible
- Global customer gifting capability (separate from internal recognition) on the same platform
- Free gifting plan allowing gift cards and perks before committing to full recognition subscription
- Support for both employee recognition and customer gifting in one product

**UX patterns**
- Slack/Teams bot plus standalone web portal — not exclusively channel-dependent like Matter
- Automated onboarding check-in sequences for new hires
- Manager 1:1 templates integrated into the recognition and feedback flow
- Clean, modern UI with AI prompts surfaced as notifications

**Integration points**
- Slack and Teams integrations
- HRIS integrations for directory sync and milestone automation
- Zapier for no-code automation
- No detailed public REST API documentation found

**Known gaps**
- Free tier reportedly removed or limited; conflicting information in reviews
- AI nudge features (Dora Hub) are less mature than Workhuman iQ
- No performance management or advanced DEI analytics
- API documentation not publicly available

**Licence / IP notes**
- Proprietary commercial SaaS. No open-source components.

---

### Vantage Circle

**Core features**
- Peer-to-peer recognition and rewards (Vantage Recognition)
- Employee wellness (Vantage Fit)
- Pulse surveys (Vantage Pulse)
- Employee perks and discount marketplace (Vantage Perks)
- HRIS integration for directory sync

**Differentiating features**
- Broadest HR engagement suite: recognition, wellness, surveys, and perks in one platform
- Microsoft 365 Copilot integration via embedded Vantage Circle agent — AI identifies who deserves recognition and what to recognise them for, inside Microsoft Copilot workflows
- ADP Workforce Now native integration (ADP Marketplace listed)
- Strong APAC and emerging-market presence with global reward catalogue
- Brandon Hall Excellence Awards 2026 winner

**UX patterns**
- Modular suite: organisations can adopt recognition, wellness, or perks independently
- M365 Copilot agent surfaces recognition prompts inside everyday Microsoft productivity workflows
- Admin console for programme configuration and analytics

**Integration points**
- Microsoft 365 Copilot agent integration
- ADP Workforce Now native integration
- Slack, Teams integrations
- HRIS connectors: Workday, SAP SuccessFactors, Oracle HCM
- REST API (publicly documented scope unclear)

**Known gaps**
- Recognition module, while comprehensive, lacks the depth of Workhuman's AI analytics
- Wellness module (Vantage Fit) is a separate product with its own pricing
- No recognition-to-performance or attrition prediction analytics
- API documentation not prominently public

**Licence / IP notes**
- Proprietary commercial SaaS. M365 Copilot integration uses Microsoft's certified agent framework.

---

### Meeds DAO (Open Source)

**Core features**
- Open-source peer recognition with points, badges, and on-chain rewards
- Contribution tracking via automated rules and external integrations (GitHub, Twitter/X, Slack)
- Blockchain-secured employee wallets (ERC-20 Meeds token)
- Self-hosted deployment via Docker
- Community-driven governance via DAO structure

**Differentiating features**
- Only meaningful open-source employee recognition platform in the category
- Blockchain-native rewards: recognition points can be converted to Meeds ERC-20 tokens tradeable on Ethereum
- GitHub and Slack connectors for automated contribution recognition
- Full API for custom integrations; can be embedded into existing enterprise software

**UX patterns**
- eXo Platform-style social intranet as the UX foundation
- Vue.js/Vuetify front end is modern but requires self-hosting expertise
- DAO governance means community contributions drive feature roadmap
- No native mobile app beyond browser-responsive UI

**Integration points**
- REST API (documented at `docs.exoplatform.org/guide/openapi/kudos`)
- GitHub, Slack, Twitter/X connectors for automated contribution recognition
- Salesforce connector
- Full source code on GitHub at `github.com/Meeds-io/meeds`

**Known gaps**
- Blockchain/token model is a barrier to enterprise adoption (regulatory, financial, and IT security concerns)
- No commercial support, SLA, or implementation services
- Reward catalogue, milestone automation, and analytics are significantly less developed than commercial platforms
- Community is small; bus-factor risk for maintenance
- No HRIS integration with major HR systems

**Licence / IP notes**
- Apache 2.0 licence for the core platform. ERC-20 token model introduces separate regulatory considerations. No IP concerns for building on or learning from this codebase.

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Peer-to-peer recognition with public social feed and emoji/comment reactions
- Manager-to-employee recognition and structured nomination workflows
- Points-based rewards with at least a basic gift card catalogue
- Birthday and work anniversary automation triggered from HRIS data
- Slack and/or Microsoft Teams integration for in-workflow recognition
- HRIS connector (at minimum BambooHR, Workday, or ADP) for employee directory sync
- Mobile app or mobile-responsive interface
- Basic participation and recognition trend analytics dashboard
- SSO support (Okta, Azure AD, Google)

### Differentiating Features
- AI-generated recognition message suggestions and coaching prompts
- Predictive attrition and engagement risk signals derived from recognition patterns
- Skills-linked recognition that builds a crowd-sourced skills map
- Organisational network analysis (ONA) revealing team collaboration and recognition equity
- Global reward fulfilment with no markup (Awardco via Amazon) or 500M+ options (Motivosity via ThanksMatters)
- Physical milestone awards and yearbook products (O.C. Tanner)
- Blockchain-based on-chain reward ledger (Meeds DAO)
- Embedded agent in M365 Copilot or Workday HCM workflows (Vantage Circle, Achievers)
- Kiosk terminal integration for deskless/frontline workers (Motivosity)

### Underserved Areas / Opportunities
- **Recognition equity and DEI analytics**: most platforms flag gaps but few provide statistical rigour or actionable bias detection
- **Skills intelligence from recognition**: only Workhuman does this at depth — it is data most HR systems desperately need
- **Manager effectiveness scoring**: coaching signals exist in several products but are not consolidated into a single managerial health KPI
- **White-label and PEO packaging**: reseller or white-label capability is sparse (only Awardco's partner header hints at this)
- **Frontline and deskless recognition**: kiosk integration is Motivosity-only; most platforms assume desk workers with Slack/Teams access
- **Open-source alternative to commercial platforms**: Meeds DAO exists but is immature; no serious OSS competitor to Bonusly/Workhuman exists
- **Performance management integration depth**: most platforms bolt on 1:1 templates; none (except Motivosity) offer native goal-setting and performance feedback loops

### AI-Augmentation Candidates
- Recognition message quality scoring and AI-rewrite suggestions to reduce bland or generic praise
- Automatic recognition gap detection with manager nudge notifications (timing, frequency, team coverage)
- Sentiment analysis on recognition text to detect language bias, micro-aggressions, and DEI patterns
- Contribution clustering to suggest appropriate point values based on impact context and historical benchmarks
- Attrition risk modelling correlating recognition frequency, participation rate, and tenure to predict flight-risk employees
- Skills extraction from recognition text to build a real-time, crowd-sourced skills inventory without manual tagging

---

## Legal & IP Summary

All major commercial platforms (Workhuman, Bonusly, Achievers, O.C. Tanner, Kudos, Motivosity, Nectar, Awardco, Matter, Assembly, Vantage Circle) are proprietary SaaS products with no open-source components. Their APIs are documented for integration use but the underlying platforms are closed. No patented features were identified in public sources, though Workhuman's Human Intelligence engine is a defensible proprietary asset. The only open-source platform, Meeds DAO, is licensed under Apache 2.0 with no IP concerns for learning from or building on its codebase. An AI-native open-source alternative would face no copyright or patent barriers from surveying this competitive landscape.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Peer-to-peer recognition with public social feed, values/category tagging, and emoji/comment reactions
- Manager-to-employee recognition and simple nomination workflow
- Points-based micro-bonus system with monthly allowances per employee
- Gift card reward catalogue (via a third-party fulfilment API such as Runa/WeGifts or Tango Card)
- Birthday and work anniversary automation from an HRIS sync (BambooHR, Workday, or SCIM)
- Slack and Microsoft Teams integrations with in-channel recognition and recognition feed notifications
- Basic participation and recognition trend analytics dashboard (recognition volume, participation rate, recognition gaps by team)
- SSO via SAML/OIDC and SCIM-based employee provisioning

**Should-have (v1.1)**
- AI recognition coach: message quality suggestions, appropriate point value recommendations, manager nudge notifications for recognition gaps
- Skills tagging on recognition events with a crowd-sourced skills map view for HR
- Organisational network analysis (ONA) showing recognition network maps and team-level culture scores
- Mobile app (iOS and Android)
- Multi-currency point budgets and country-aware reward catalogue

**Nice-to-have (backlog)**
- Predictive attrition and engagement risk modelling from recognition signals
- DEI analytics: recognition equity by demographic group with bias detection on message language
- White-label packaging for PEO/HR outsourcing resellers
- Kiosk/tablet integration for deskless and frontline recognition scenarios
- Physical milestone award ordering (printed yearbooks, branded merchandise)
- Manager effectiveness scoring dashboard combining recognition frequency, message quality, and team engagement
