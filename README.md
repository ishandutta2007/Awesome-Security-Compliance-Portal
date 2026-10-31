# Awesome-Security-Compliance-Portal

## Top Security & Compliance Portal Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Trust Center Publishing, Compliance Automation & Self-Hosted GRC Portals*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Security & Compliance Portals**. These tools enable organizations to publish a public-facing Trust Center that showcases security posture, compliance certifications, and subprocessors—while automating the internal GRC work (evidence collection, control tracking, audit readiness) that makes those public claims credible.



**Examples** include Atlassian Trust Center, SafeBase, Conveyor, TrustCloud, Vanta Trust Center, Drata Trust Center, Whistic, OneTrust, Secureframe Trust Center, and RegScale (the category leaders).



**Open-source emphasis**: Security & Compliance Portals is a domain where open-source tooling is **genuinely emerging but fragmented across two distinct layers**. The **public Trust Center layer** is served by **Kodus Trust Center** (a YAML-driven, self-hosted trust portal with compliance badges, document requests, subprocessors, and FAQs) and **Probo's compliance page** (a public portal with NDA management, certification publishing, and custom domain support) . The **internal GRC automation layer** is served by **Probo** (full GRC lifecycle with 270+ MCP tools for AI agents) , **Openlane** (SOC 2, ISO 27001, NIST 800-53 automation with SSO on every tier) , and **QuickTrust** (AI-agent-first SOC 2 automation) . The critical caveat: **no single open-source project matches the full SafeBase or Vanta experience**—you either assemble a trust portal (Kodus) with a separate GRC backend (Probo/Openlane), or accept that Probo's public compliance page is less customizable than dedicated trust center tools .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Atlassian Trust Center](https://www.atlassian.com/)**  

  Atlassian's public trust portal showcasing compliance certifications, security practices, and subprocessors for Jira, Confluence, and Bitbucket.



- **[SafeBase](https://safebase.io/)**  

  The leading Trust Center platform; automates security questionnaire responses, manages NDA-gated document access, and provides a customizable public trust portal.



- **[Conveyor](https://conveyor.com/)**  

  Trust Center and security questionnaire automation platform; focused on reducing sales friction by answering buyer security questions instantly.



- **[TrustCloud](https://trustcloud.ai/)**  

  GRC and Trust Center platform combining compliance automation with a public trust portal for demonstrating security posture.



- **[Vanta Trust Center](https://www.vanta.com/)**  

  Public trust portal integrated with Vanta's compliance automation platform; publishes certifications and security posture to buyers.



- **[Drata Trust Center](https://drata.com/)**  

  Trust Center within Drata's compliance automation platform; showcases compliance status and automates evidence collection.



- **[Whistic](https://www.whistic.com/)**  

  Vendor security assessment and Trust Center platform; enables organizations to publish a trust profile and respond to assessments.



- **[OneTrust](https://www.onetrust.com/)**  

  GRC platform with Trust Center capabilities for privacy, security, and third-party risk; broad enterprise coverage.



- **[Secureframe Trust Center](https://secureframe.com/)**  

  Trust Center within Secureframe's compliance platform; publishes certifications and automates questionnaire responses.



- **[RegScale](https://regscale.com/)**  

  Continuous controls monitoring platform with compliance-as-code foundation; provides trust portal capabilities alongside GRC automation.



## Open-Source GitHub Projects



### Public Trust Centers (Standalone)



- **[Kodus Trust Center](https://github.com/kodustech/trust-center)**  

  The most focused open-source **standalone Trust Center** available—a self-hosted, YAML-driven builder that renders a polished public trust portal from a single YAML document . Features: **compliance badges**, **document requests** (email + admin review), **subprocessors** listing, FAQs accordion, policies, infrastructure/monitoring sections, theming (light/dark), company logo, and hero commitments . **Admin dashboard** with GitHub SSO (NextAuth) and a YAML editor with live preview . **Tech stack**: Next.js 16, Supabase for storage, Shadcn/ui + Tailwind CSS v4 . **Deploy anywhere** (Vercel, Fly, Render) with no vendor lock-in . **Best for organizations wanting a simple, self-hosted public trust portal** without the weight of a full GRC platform—but it is trust-center-only, not a GRC automation backend.



- **[TrustSite (defentorretrustsite)](https://github.com/defentorretrustsite/TrustSite)**  

  Self-hosted Trust Center on GitHub with **default-deny network policy** and no secrets in the repo . Features: **approved answer bank** with citations back to source policies, private document request-and-approve flow (not open links), **immediate revocation** on next click, download logging, and multi-product trust pages per org with scoped team members . Self-hosted with your database and AI key (including local models). **Early-stage**—verify production readiness, but the architecture (answer reuse with citations, revocation, audit logging) addresses real gaps in trust center workflows .



### GRC Platforms with Public Compliance Pages



- **[Probo](https://github.com/getprobo/probo)**  

  The most comprehensive open-source **GRC platform** with a **public compliance portal** built in . Covers the full lifecycle: risk register with inherent/residual scoring, controls with maturity levels, vendor risk, data privacy (DPIA/TIA), access reviews, audit programs, and document approval workflows . **Public compliance page** features: NDA management, certification publishing, and custom domain support . **AI-native**: 270+ MCP tools expose every entity for AI agent automation; `prb` CLI (44+ command groups), GraphQL API, and n8n community node . **ISC licensed**, self-hostable with Docker, audit-ready with policy-based RBAC and immutable audit logs . **Best for teams wanting an integrated GRC backend with a public trust page**—the public page is less customizable than Kodus's dedicated trust center, but the GRC depth is unmatched in open source.



- **[Openlane](https://github.com/theopenlane/core)**  

  Open-source **compliance automation** alternative to Vanta, Drata, and Secureframe (Apache-2.0) . Supports **SOC 2, GDPR, ISO 27001, NIST 800-53**, and more . **Security features like SSO and 2FA ship with every module** rather than sitting behind an enterprise tier—a direct contrast to commercial platforms . Runs on Go, PostgreSQL, Redis, and OpenFGA without a pile of SaaS dependencies . **Trust Center and vanity domains** are on the roadmap (not yet shipped) . **Best for teams wanting Vanta-like automation with fully permissive licensing**—but the public Trust Center layer requires a separate tool until it ships.



- **[QuickTrust](https://github.com/allgpt-co/quicktrustfinal)**  

  Open-source, **AI-agent-first GRC platform** focused on making SOC 2, ISO 27001, HIPAA, and PCI DSS accessible (AGPL) . Features: **SOC 2 Type II framework** with 9 domains, 33 requirements, and control objectives fully seeded; 25 control templates across 8 security domains; 20 evidence templates; **AI controls generation agent** (Amazon Bedrock Claude Sonnet via LiteLLM) that tailors draft controls to your tech stack; multi-tenant architecture with RBAC; compliance dashboard with scoring . **Best for startups wanting AI-assisted SOC 2 readiness**—but it is early-stage and the Trust Center layer is not yet built (roadmap item).



### Additional Strong Open-Source Options



- **Unicis Platform CE** — Open-source GRC platform (Beta) positioned as a competitor to Vanta and Drata; covers privacy, security, risk, and compliance . **Early-stage**—verify production readiness before adoption .

- **VerifyWise** — Open-source **AI governance** platform (365 GitHub stars) with a central repository for AI systems, risk assessments, and framework mapping across EU AI Act, ISO/IEC 42001, and NIST AI RMF . **AI-specific**—not a general security trust center, but relevant for organizations needing AI compliance assurance .

- **@mdxui/soc2** — NPM package providing **SOC 2 compliance components** for building trust centers (public) and compliance portals (internal); integrates with Payload CMS . **Developer library**—for teams building custom trust center UIs, not a deployable platform .



**Frameworks for building custom systems**: The choice depends on which layer you need. For a **standalone public Trust Center**, Kodus Trust Center provides the most focused, deployable option with YAML-driven configuration . For **integrated GRC automation with a public compliance page**, Probo offers the deepest open-source GRC lifecycle with 270+ MCP tools . For **Vanta-like automation with permissive licensing**, Openlane (Trust Center on roadmap) . For **AI-assisted SOC 2 readiness**, QuickTrust . No single open-source project matches SafeBase's **questionnaire automation and NDA-gated document workflows** combined with Vanta's **continuous evidence collection**—you either assemble Kodus + Probo, or accept feature gaps.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Trust Center and GRC platforms handling security posture and compliance evidence must comply with organizational security policies; **public trust portals publishing certification claims must ensure accuracy**—misrepresenting compliance status creates legal and reputational risk.

- **Open-source security & compliance portals are emerging but fragmented**—Kodus Trust Center provides a standalone public trust portal , Probo provides integrated GRC with a public compliance page , and Openlane/QuickTrust provide Vanta-like automation . However, **no single open-source project matches SafeBase's questionnaire automation and NDA-gated document workflows combined with Vanta's continuous evidence collection**—organizations requiring the full commercial experience should evaluate SaaS platforms or plan for assembly.

- Verify license terms for commercial use; Kodus Trust Center is open-source (check repository) , Probo uses ISC , Openlane uses Apache-2.0 , and QuickTrust uses AGPL .



---



**Made for security leaders, compliance managers, and teams building trust with buyers.**  

Let's make security and compliance portals more open, but with clear eyes about the questionnaire automation and evidence collection gaps that commercial platforms still fill.
