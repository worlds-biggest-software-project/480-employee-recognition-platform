# Employee Recognition Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source platform for peer-to-peer recognition, reward points, manager spotlights, and culture analytics that delivers enterprise-grade people insights at mid-market pricing.

Employee Recognition Platform gives organisations a structured way for peers, managers, and executives to acknowledge contributions, distribute reward points redeemable for tangible benefits, and generate engagement and culture analytics. It targets HR leaders, engineering managers, and people operations teams who need recognition data that connects to performance, skills intelligence, and retention outcomes. The core problem it solves: frequent, meaningful recognition drives lower attrition and stronger culture, but existing tools either cost too much or lack the analytical depth to prove it.

---

## Why Employee Recognition Platform?

- **Enterprise analytics are locked behind enterprise pricing.** Workhuman's Human Intelligence engine delivers recognition-to-attrition modelling and skills insights, but its price point effectively excludes SMBs and mid-market organisations from accessing these capabilities.
- **Mid-market leaders lack analytical depth.** Bonusly achieves high adoption rates but offers no recognition-to-attrition modelling, no DEI analytics, and no skills intelligence -- leaving HR teams without the data they need to justify recognition spend.
- **No serious open-source alternative exists.** Meeds DAO is the only open-source recognition platform, but its blockchain/token model creates regulatory barriers for enterprises, and its analytics, milestone automation, and HRIS integrations are significantly underdeveloped.
- **Recognition equity and bias detection are underserved across the category.** Most platforms flag recognition gaps but few provide statistical rigour or actionable bias detection on recognition language and participation patterns.
- **Frontline and deskless workers are an afterthought.** Only Motivosity offers kiosk-based recognition for workers without Slack or Teams access; most platforms assume desk-based employees.

---

## Key Features

### Peer and Manager Recognition

- Peer-to-peer recognition with public social feed, values/category tagging, and emoji/comment reactions
- Manager-to-employee recognition and structured nomination workflows
- Points-based micro-bonus system with configurable monthly allowances per employee
- Service milestone and work anniversary automation triggered from HRIS data

### Rewards and Fulfilment

- Gift card reward catalogue via third-party fulfilment API (e.g. Runa/WeGifts or Tango Card)
- Multi-currency point budgets and country-aware reward catalogue
- Birthday and work anniversary automated celebrations with personalised messages

### AI Recognition Coach

- AI-generated recognition message quality suggestions and rewrite recommendations
- Appropriate point value recommendations based on contribution context and historical benchmarks
- Manager nudge notifications when team members are overdue for recognition
- Sentiment analysis on recognition text to detect language bias and DEI patterns

### Analytics and Intelligence

- Participation and recognition trend dashboards (volume, participation rate, recognition gaps by team)
- Skills tagging on recognition events with a crowd-sourced skills map view for HR
- Organisational network analysis (ONA) showing recognition network maps and team-level culture scores
- Predictive attrition and engagement risk modelling from recognition signals (backlog)

### Integrations and Platform

- Slack and Microsoft Teams integrations with in-channel recognition and feed notifications
- HRIS connectors (BambooHR, Workday, ADP) for employee directory sync and milestone automation
- SSO via SAML/OIDC and SCIM-based employee provisioning
- Mobile app for iOS and Android

---

## AI-Native Advantage

AI capabilities set this platform apart from incumbents in three areas. First, recognition message quality scoring and rewrite suggestions eliminate the bland, generic praise that undermines recognition culture -- something only Workhuman currently addresses with its proprietary LLM. Second, automatic skills extraction from recognition text builds a real-time, crowd-sourced skills inventory without requiring manual tagging, giving HR teams data that most skills management platforms cannot generate organically. Third, recognition-pattern-based attrition risk modelling correlates recognition frequency, participation rate, and tenure to predict flight-risk employees before they disengage -- closing an analytics gap that exists in every mid-market competitor.

---

## Tech Stack & Deployment

The platform targets self-hosted and cloud deployment modes. HRIS integration follows the SCIM standard for employee provisioning alongside direct connectors for BambooHR, Workday, and ADP. Authentication uses SAML/OIDC for SSO. Reward fulfilment is handled through third-party APIs (Runa/WeGifts or Tango Card) rather than a proprietary catalogue, keeping fulfilment costs transparent and globally extensible. Slack and Microsoft Teams integrations deliver recognition inside existing collaboration workflows. A REST API supports custom integrations and white-label packaging for PEO and HR outsourcing providers.

---

## Market Context

The employee recognition software market is well-established with strong demand across all organisation sizes. Enterprise incumbents like Workhuman use opaque enterprise pricing, while mid-market leaders like Bonusly charge $3-$5 per employee per month and Nectar HR charges $5-$6 PEPM with a $4,000 annual minimum. The primary buyers are HR leaders, people operations teams, and engineering managers seeking to reduce attrition and strengthen culture. Domain availability is high, with no patent barriers identified in the competitive landscape and the only open-source entrant (Meeds DAO, Apache 2.0) providing a reference architecture without IP concerns.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
