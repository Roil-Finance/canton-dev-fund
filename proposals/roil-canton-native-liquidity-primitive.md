# Roil: Canton-Native Liquidity Primitive & Reference Implementation

## Project Information

**Project Name:** Roil

**SIG:** `defi-liquidity`

**Champion:** **Seeking a Champion**

**Funding Requested:** **800,000 CC**

**Project Duration:** **16 Weeks**

**Website:** roil.app

**GitHub Organization:** github.com/Roil-Finance

**Technical Demo:** youtube.com/watch?v=_MagWXLwyiw

---

# Executive Summary

Roil proposes to develop an open-source, reusable Canton-native liquidity primitive together with a Roil reference implementation demonstrating how the infrastructure can be integrated into a real Canton application.

The proposal consists of two connected workstreams.

### Workstream A: Reusable Canton-Native Liquidity Primitive

A reusable public-good infrastructure layer covering:

* liquidity state management;
* pool and reserve accounting;
* asset integration boundaries;
* liquidity provision;
* quote calculation;
* authorization-controlled swap execution;
* settlement;
* validation;
* automated testing;
* developer documentation;
* security hardening.

### Workstream B: Roil Reference Implementation

A practical implementation demonstrating how the reusable infrastructure can be integrated into real portfolio and treasury workflows on Canton.

The objective is not to fund a closed application feature. The primary ecosystem output is reusable, open-source infrastructure that other Canton builders can inspect, adapt, and build upon.

Roil will serve as the reference implementation demonstrating the primitive in a practical application workflow.

The total funding request is **800,000 CC** over **16 weeks**, distributed across four milestones.

---

# Problem Statement

Builders developing programmable liquidity or asset-exchange functionality on Canton may otherwise need to independently design and validate significant application infrastructure, including:

* pool and reserve accounting;
* liquidity state management;
* quote calculation;
* fee and configuration logic;
* asset integration boundaries;
* authorization-controlled transaction execution;
* settlement;
* state consistency and stale-state handling;
* concurrent transaction and contention behavior;
* automated testing and reproducible validation;
* technical documentation and integration guidance.

When these components are developed separately by each application team, engineering effort and validation work can be repeated across the ecosystem.

The gap is therefore not only source code.

Builders also benefit from reusable implementation patterns, automated tests, technical documentation, integration guidance, reproducible build instructions, and a practical reference integration.

Roil aims to address this by developing reusable Canton-native liquidity infrastructure and demonstrating its practical use through an open reference implementation.

---

# Proposed Solution

## Workstream A: Reusable Canton-Native Liquidity Primitive

The primary public-good deliverable is an open-source, reusable Canton-native liquidity primitive.

The work includes the following components.

### Liquidity Core

* pool and reserve accounting;
* fee and configuration logic;
* liquidity state management;
* core transaction rules;
* validation logic.

### Asset Integration

* clear boundaries for supported asset interactions;
* asset validation;
* liquidity provision workflows;
* reusable asset interaction flows.

### Swap Execution and Settlement

* quote calculation;
* authorization-controlled execution;
* input and output validation;
* settlement;
* state and quote validation;
* quote validity handling;
* configurable slippage controls.

### Validation and Hardening

* automated tests;
* concurrent transaction tests;
* contention scenarios;
* Canton network validation;
* independent security review;
* remediation of applicable findings;
* regression testing;
* final open-source release.

The exact implementation parameters will be finalized through the design, development, and validation process rather than presenting undeveloped configuration choices as completed production components.

---

# Architectural Alignment

The proposed architecture separates reusable ecosystem infrastructure from the application-specific reference implementation:

**Reusable Canton-Native Liquidity Primitive → Roil Reference Integration → Portfolio and Treasury Workflows**

The liquidity primitive is intended to provide reusable implementation patterns for liquidity-related state, accounting, asset interaction, transaction execution and settlement.

Roil consumes this infrastructure as a reference implementation rather than treating the reusable primitive as a closed application component.

This separation is intended to ensure that the primary Development Fund output remains reusable by other Canton builders while also being validated through a practical end-to-end application context.

The implementation will use Canton and Daml-native application patterns for relevant authorization, party and role modelling, contract lifecycle and state-transition workflows.

---

# Existing Progress and Evidence

Roil is not being presented as a project starting from zero.

The team has an existing Canton and Daml application development foundation and has already developed application-level workflows, backend and frontend infrastructure, testing, and related technical components.

Existing work includes:

* Canton and Daml application development;
* portfolio and treasury workflows;
* authorization-oriented transaction flows;
* backend and API infrastructure;
* frontend application infrastructure;
* automated testing and development workflows;
* technical development documentation.

These existing components establish a starting point for the proposed work.

However, the reusable Canton-native liquidity primitive requested under this proposal is a **new workstream** to be designed, developed, tested, validated, security-reviewed, remediated where necessary, and released as open source.

**Roil GitHub:** github.com/Roil-Finance

**Technical Demo:** youtube.com/watch?v=_MagWXLwyiw

The distinction between prior work and Development Fund work is explicit:

> Existing Roil development provides an application and engineering foundation. The reusable liquidity primitive funded by this proposal is a new open-source deliverable, and Roil will act as the reference implementation for that new infrastructure.

---

# Scope

## In Scope

### Workstream A

* liquidity core;
* pool and reserve accounting;
* fee and configuration logic;
* liquidity state management;
* asset integration boundaries;
* liquidity provision flows;
* quote calculation;
* authorization-controlled swap execution;
* settlement;
* state and quote validation;
* quote validity handling;
* configurable slippage controls;
* concurrent transaction and contention testing;
* Canton network validation;
* automated test suite;
* technical and developer documentation;
* reproducible build and deployment instructions;
* independent security review;
* remediation and regression testing;
* final open-source release.

### Workstream B

* Roil reference integration;
* portfolio and treasury workflow integration;
* asset and pool interactions;
* swap and settlement integration;
* updated application state workflows;
* end-to-end demonstration.

---

## Out of Scope

The following are not deliverables of this proposal:

* a smart order router across multiple liquidity sources;
* undefined or general-purpose smart routing;
* a general-purpose compound engine;
* undefined yield products;
* a separate liquidity-capital allocation;
* an unconditional liquidity transfer;
* undefined product features not described in the milestone deliverables.

The **800,000 CC** request is for the defined development, testing, security, remediation, documentation, and release program.

It is not a separate request for liquidity capital.

---

# Milestones, Funding and Acceptance Criteria

## MS1: Technical Design & Liquidity Core

**Duration:** 3 Weeks
**Timeline:** Weeks 1-3
**Funding:** **180,000 CC**

### Scope

* technical design;
* liquidity core implementation;
* pool and reserve accounting;
* fee and configuration logic;
* initial liquidity state structure;
* initial automated tests;
* technical design documentation.

### Acceptance Criteria and Evidence

* source code for the liquidity core is available in the project repository;
* pool, reserve and relevant configuration logic is implemented and documented;
* automated tests covering the delivered core functionality are available and passing;
* technical design documentation explains the delivered component boundaries and workflow;
* reviewers can reproduce the documented build and test process.

---

## MS2: Asset Integration & Swap Execution

**Duration:** 4 Weeks
**Timeline:** Weeks 4-7
**Funding:** **180,000 CC**

### Scope

* asset integration boundaries;
* liquidity provision flows;
* quote calculation;
* authorization-controlled swap execution;
* settlement;
* state and quote validation;
* quote validity handling;
* configurable slippage controls;
* expanded automated testing.

### Acceptance Criteria and Evidence

* asset interaction and liquidity provision flows are implemented and documented;
* quote, execution, settlement and validation flows are available in source code;
* automated tests cover normal and relevant invalid or edge execution paths;
* test results and build instructions are provided so the delivered functionality can be reproduced;
* the milestone does not depend on undisclosed functionality outside the documented scope.

---

## MS3: Performance, TestNet & Roil Reference Integration

**Duration:** 3 Weeks
**Timeline:** Weeks 8-10
**Funding:** **160,000 CC**

### Scope

* validation of the implemented liquidity state approach;
* concurrent transaction tests;
* contention scenarios;
* retry and error behavior testing;
* Canton network validation;
* Roil reference integration;
* end-to-end tests;
* technical and developer documentation updates.

### Acceptance Criteria and Evidence

* concurrent transaction and contention scenarios are implemented as reproducible tests;
* relevant Canton network validation is demonstrated through documented test or deployment evidence;
* the Roil reference integration exercises the delivered primitive through an end-to-end workflow;
* source code, test results and documentation for the integration are publicly available;
* reviewers can reproduce the documented validation workflow from the released instructions.

---

## MS4: Independent Audit, Remediation & Final Release

**Duration:** 6 Weeks
**Timeline:** Weeks 11-16
**Funding:** **280,000 CC**

### Scope

1. audit preparation and code freeze;
2. independent security review;
3. review and triage of findings;
4. applicable remediation work;
5. regression testing;
6. re-testing or validation where appropriate;
7. final open-source release;
8. publication of the final audit and remediation status, subject to responsible disclosure requirements.

### Acceptance Criteria and Evidence

* an independent security review has been completed for the agreed delivered scope;
* applicable findings are documented and remediated or otherwise dispositioned with an explanation;
* regression tests pass for the final release;
* final source code, documentation, build instructions and release information are publicly available;
* audit and remediation status is published, except for temporary limitations required to avoid exposing an unresolved active security risk.

---

# Milestone Summary

| Milestone                                                  |     Duration | Timeline    |        Funding |
| ---------------------------------------------------------- | -----------: | ----------- | -------------: |
| **MS1: Technical Design & Liquidity Core**                 |      3 Weeks | Weeks 1-3   | **180,000 CC** |
| **MS2: Asset Integration & Swap Execution**                |      4 Weeks | Weeks 4-7   | **180,000 CC** |
| **MS3: Performance, TestNet & Roil Reference Integration** |      3 Weeks | Weeks 8-10  | **160,000 CC** |
| **MS4: Independent Audit, Remediation & Final Release**    |      6 Weeks | Weeks 11-16 | **280,000 CC** |
| **Total**                                                  | **16 Weeks** |             | **800,000 CC** |

Funding is requested on a milestone basis.

Release of subsequent funding is subject to the applicable Development Fund milestone assessment and continuation process.

---

# Canton Ecosystem Impact

## Reusable Open-Source Infrastructure

The primary ecosystem output is a reusable Canton-native liquidity primitive.

Other builders will be able to inspect, adapt, extend and, where appropriate, reuse the open-source deliverables under the applicable project license.

## Developer Experience

The project aims to reduce repeated implementation work around:

* liquidity accounting;
* transaction execution;
* authorization;
* settlement;
* state consistency;
* concurrent transaction behavior;
* testing;
* reproducible validation.

The contribution is broader than source code and includes automated tests, technical documentation, integration guidance, reproducible build and deployment instructions, and a practical reference implementation.

## Canton-Specific Implementation Knowledge

The project will document relevant implementation experience around:

* authorization-controlled execution;
* contract and workflow visibility;
* asset interaction boundaries;
* settlement;
* concurrent transactions and contention;
* state consistency;
* stale or changed state handling.

## Security as a Shared Output

Where appropriate, the project will publish:

* the audit scope;
* final audit results or an equivalent public summary;
* remediation status;
* relevant fixes;
* re-test or validation status.

Temporary disclosure limitations may be used only where needed to avoid exposing an unresolved active security issue.

---

# Adoption and Distribution

The primary distribution channel for the reusable deliverables will be open-source publication.

The project will support adoption through:

* public source code;
* technical design documentation;
* developer integration guidance;
* automated test examples;
* reproducible build and validation instructions;
* the Roil reference implementation;
* end-to-end demonstration of the implemented workflows.

Roil will provide a practical application context demonstrating how the reusable primitive can be integrated into portfolio and treasury workflows.

The objective is to make the project useful not only as a reference codebase but also as a documented implementation pattern that other Canton builders can evaluate and adapt.

---

# Expected Ecosystem Deliverables

| Deliverable                     | Ecosystem Value                                |
| ------------------------------- | ---------------------------------------------- |
| Reusable liquidity primitive    | Shared infrastructure for Canton builders      |
| Asset integration boundaries    | Clearer reusable integration patterns          |
| Swap and settlement workflows   | Tested transaction execution patterns          |
| Concurrent and contention tests | Reproducible evidence for concurrency behavior |
| Canton network validation       | Practical implementation validation            |
| Automated tests                 | Reusable testing reference                     |
| Technical documentation         | Shared design and implementation knowledge     |
| Integration guidance            | Lower integration friction                     |
| Roil reference implementation   | End-to-end practical example                   |
| Audit and remediation status    | Shared security and hardening knowledge        |

---

# Risks and Mitigations

## Concurrent Transaction and Contention Risk

**Risk:** Concurrent updates to liquidity-related state may create contention or affect execution behavior.

**Mitigation:**

* implement and validate an appropriate state management approach;
* test concurrent transaction scenarios;
* test contention behavior;
* document retry and error behavior;
* validate state consistency through automated tests.

---

## Smart Contract and Security Risk

**Risk:** Errors in reserve accounting, authorization, validation or settlement could affect application integrity.

**Mitigation:**

* automated tests;
* invalid-input and edge-case testing;
* authorization testing;
* state and quote validation;
* regression testing;
* independent security review;
* remediation and follow-up validation.

---

## CC Volatility Risk

The project duration is less than six months.

Funding is requested in CC on a milestone basis, and no automatic price-adjustment mechanism is assumed.

The recipient carries the applicable CC volatility risk unless the Tech & Ops Committee decides otherwise under the Development Fund process.

---

## Oracle or Reference Data Risk

Where external or reference pricing is used by an implemented workflow, relevant controls may include data freshness checks, stale-data rejection, deviation limits and defined error behavior.

The final scope of such integrations will be documented based on the implemented design.

---

## Key-Person Risk

Technical knowledge concentrated in a small team can affect continuity.

**Mitigation:**

* open-source code;
* technical documentation;
* reproducible build instructions;
* automated tests;
* documented team responsibilities;
* independent security review.

---

# Sustainability

The proposal does not assume permanent dependence on Development Fund financing.

## Open-Source Maintenance

After delivery, the reusable infrastructure is intended to remain available as open source.

Maintenance may include:

* bug fixes;
* dependency updates;
* security updates;
* regression testing;
* documentation updates;
* issue and pull-request review.

## Roil as an Ongoing Reference Implementation

Roil provides an ongoing application context for exercising the reusable primitive, identifying integration needs, testing changes and improving developer documentation.

## Longer-Term Sustainability

Potential future sustainability paths may include:

* application-level services;
* advanced portfolio and treasury workflows;
* distribution and ecosystem opportunities;
* other applicable Canton ecosystem programs.

These are not presented as guaranteed revenues and are not required to justify the requested Development Fund funding.

The requested **800,000 CC** is for the defined 16-week development, validation, security, remediation, documentation and release program rather than indefinite operational funding.

---

# Open Source and Audit Commitment

The outputs funded under this proposal will be released as open source under the applicable license published with the project repository and release artifacts.

Public deliverables will include, as applicable:

* source code;
* automated tests;
* technical design documentation;
* developer integration guidance;
* build and deployment instructions;
* release information;
* audit and remediation status, subject to responsible disclosure requirements.

The exact license will be stated in the relevant project repository before final release.

---

# Funding Request

## Total Funding Requested: 800,000 CC

| Milestone                                              |        Funding |
| ------------------------------------------------------ | -------------: |
| MS1: Technical Design & Liquidity Core                 | **180,000 CC** |
| MS2: Asset Integration & Swap Execution                | **180,000 CC** |
| MS3: Performance, TestNet & Roil Reference Integration | **160,000 CC** |
| MS4: Independent Audit, Remediation & Final Release    | **280,000 CC** |
| **Total**                                              | **800,000 CC** |

The request is milestone-based.

It does not include a separate liquidity-capital allocation or an unconditional transfer of funds for liquidity provision.

---

# Team

## Seyfettin Çelik

**Role:** Ecosystem and Product Lead

**Email:** [syftneth@roil.app](mailto:syftneth@roil.app)

### Responsibilities

* product vision and roadmap;
* Canton ecosystem use-case alignment;
* coordination between Workstream A and Workstream B;
* product requirements for the reusable liquidity primitive;
* product requirements for the Roil reference implementation;
* milestone and deliverable coordination;
* coordination between technical development and product requirements;
* ecosystem positioning and potential integration assessment.

Seyfettin's focus is ensuring that the public-good deliverable is aligned with practical Canton application needs while Roil provides a concrete reference context for adoption and integration.

---

## Semih Civelek

**Role:** Technical and Daml Architect

**Email:** [himess@roil.app](mailto:himess@roil.app)

**GitHub:** github.com/Himess

### Responsibilities

* Canton and Daml technical architecture;
* Daml contract and domain-model development;
* contract lifecycle and state-transition design;
* authorization and party and role modeling;
* technical delivery of Workstream A;
* technical delivery of the Workstream B reference integration;
* Daml testing infrastructure;
* build and test process coordination;
* technical documentation;
* open-source release preparation.

Semih's public development background includes work and contributions across financial application infrastructure, payment systems, AI agent tooling, zero-knowledge proving operations and developer tooling, alongside his responsibility for the Roil technical architecture and Canton/Daml implementation.

---

# Final Deliverables

At the end of the 16-week program, the project targets the delivery of:

* a reusable Canton-native liquidity primitive;
* open-source source code;
* liquidity and pool-management components;
* asset integration boundaries;
* swap and settlement workflows;
* authorization-controlled execution patterns;
* concurrent transaction and contention validation;
* automated tests;
* technical design documentation;
* developer integration guidance;
* reproducible build and deployment instructions;
* Canton network validation;
* a Roil reference integration;
* independent security review;
* remediation and validation status;
* a final open-source release.

---

# Conclusion

The proposal is designed to fund a shared Canton ecosystem contribution rather than only a closed application feature.

Workstream A creates reusable open-source infrastructure.

Workstream B demonstrates how that infrastructure can be integrated into a real Canton application through Roil.

The central value proposition is:

> Build a reusable Canton-native liquidity component that ecosystem developers can inspect and build upon, validate it through tests and security hardening, and demonstrate its practical use through an open Roil reference implementation.
