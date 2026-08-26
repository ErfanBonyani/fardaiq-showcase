# Product case study

## Context

Service businesses often divide their public website, sales intake, client communication, project tracking, and educational products across unrelated tools. That fragmentation creates repeated data entry, incomplete briefs, unclear project status, and difficult handoffs.

FardaIQ was designed as one multilingual product surface that connects discovery, structured ordering, delivery, support, and learning.

## Product goals

1. Make complex AI and software services understandable to non-technical customers.
2. Convert an initial idea into a structured and actionable project brief.
3. Give customers one workspace for progress, messages, files, decisions, and learning.
4. Give operators controlled workflows without exposing administrative capabilities to customers.
5. Support Persian-first RTL presentation while retaining complete English and German experiences.
6. Keep privacy, accessibility, security, and maintainability part of the architecture from the beginning.

## Core user journeys

### Public visitor

- Discovers AI, automation, web, and software services.
- Reviews selected work and educational content.
- Changes language without losing the current context.
- Starts a guided order instead of submitting an unstructured contact message.

### Prospective customer

- Selects a service and completes a conditional six-step brief.
- Saves progress and resumes the draft later.
- Provides requirements, budget, timing, integrations, and files.
- Reviews a final summary before submission.

### Active customer

- Sees orders and project milestones in one dashboard.
- Exchanges messages and controlled files.
- Reviews proposals and records explicit approvals.
- Tracks course enrollment and learning progress.

### Operator and administrator

- Processes incoming orders through defined states.
- Creates proposals and projects with traceable transitions.
- Manages course content and operational records.
- Uses server-side authorization rather than relying on hidden interface elements.

## Product and engineering decisions

- **Progressive disclosure:** users answer only questions relevant to their selected service.
- **Recoverable drafts:** complex briefs can be resumed instead of restarted.
- **Server-authoritative decisions:** sensitive access and state transitions are validated on the server.
- **Localized information architecture:** translations, metadata, canonical paths, and layout direction are treated as one system.
- **Migration-controlled data evolution:** relational changes are reviewed and verified rather than applied informally.
- **Pull-request delivery:** changes are validated by CI before entering the main branch.
- **Private implementation, public case study:** employers can review product and engineering thinking without exposing proprietary source.

## My contribution

I translated the product idea into requirements and user flows, structured the public, customer, academy, and administrative experiences, coordinated implementation, reviewed security and privacy boundaries, performed acceptance testing, managed branch and pull-request delivery, investigated CI and Linux compatibility problems, and prepared the system for production deployment.

The implementation process used AI-assisted engineering tools. My responsibility remained the definition of correct behaviour, architectural and product decisions, review of generated changes, integration, testing, troubleshooting, security evaluation, and release readiness.

## Validation and delivery discipline

- Main-branch CI is passing.
- Pull requests are used to isolate and review changes.
- Dependency and security monitoring are enabled.
- Build, lint, migration, and rendered-output checks are part of the verification direction.
- Secrets and hosting-account configuration are excluded from source control.
- Production hosting and final external-provider configuration are reported as pending rather than already live.

## Outcome

The result is more than a landing page: it is a cohesive product foundation spanning acquisition, structured ordering, customer operations, learning, administration, and governance. The project demonstrates product analysis, multilingual UX, web application architecture, relational data thinking, security awareness, Git-based delivery, CI troubleshooting, and production-readiness planning.

## Honest scope boundary

The private implementation and public showcase are active, but the public live environment is the next milestone. Hosting-dependent integrations, production payment and email providers, operational analytics, consent configuration, and final legal review remain part of deployment and operational readiness. No external compliance certification is claimed.
