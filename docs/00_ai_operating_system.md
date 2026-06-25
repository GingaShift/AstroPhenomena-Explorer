# AstroPhenomena Explorer — AI Operating System v0.2

**Version:** v0.2
**Status:** Working operating document
**Last updated:** 2026-06-25

---

## 1. Purpose

AstroPhenomena Explorer is not only a software project.

It is a long-term scientific, educational and engineering project designed to help its creator learn astronomy by building a coherent open-source platform for understanding, visualizing and predicting astronomical phenomena.

The project must evolve progressively with the creator’s knowledge.

The goal is not to build a fixed application immediately, but to create a structured learning and development environment where each astronomical concept can become a module, visualization, simulation, experiment or analysis tool.

---

## 2. Primary Audience and Accessibility Contract

AstroPhenomena Explorer is primarily designed for the creator’s advanced learning.

However, the platform must remain clear enough to serve as an accessible engineering and scientific portfolio for external reviewers, recruiters, professors and future contributors.

The project should not be simplified into a generic beginner application, but its interface and documentation must allow an external observer to understand what astronomical concept is being explored and why it matters.

The primary audience is therefore:

* the creator as an advanced learner;
* the creator as an engineer building a long-term scientific portfolio;
* external reviewers who need to understand the project quickly;
* future contributors who may join or reuse the platform.

---

## 3. Core Principle

The project follows one central principle:

**Learn by building, but design before building.**

No major feature should be developed before the following questions have been answered:

1. What scientific concept does this feature teach?
2. Which DU ECU course notion does it connect to?
3. What user question does it answer?
4. What data does it need?
5. What level of precision is required?
6. What are the risks of misunderstanding or oversimplification?
7. How will the feature connect to the rest of the platform?

This principle does not forbid exploratory work.

It means that exploratory work must be clearly identified, scoped and prevented from silently becoming final architecture.

---

## 4. Role of the Human Project Lead

The human project lead is responsible for:

* defining the long-term ambition;
* expressing intuitions, ideas and creative directions;
* validating scientific understanding progressively;
* choosing which directions are worth exploring;
* maintaining coherence with personal learning goals;
* deciding when the project is ready to move from concept to prototype, and from prototype to implementation.

The project lead does not need to know everything in advance.

The system must assume that many scientific, technical and design decisions will emerge progressively.

The project lead remains the final decision-maker.

AI outputs are recommendations, not final decisions.

---

## 5. Role of ChatGPT

ChatGPT acts as the scientific, pedagogical and strategic lead.

Its responsibilities are:

* clarifying the scientific meaning of each concept;
* connecting software modules to DU ECU course notions;
* building the conceptual architecture of the project;
* identifying missing knowledge;
* challenging weak assumptions;
* proposing ambitious directions;
* structuring the documentation;
* helping transform vague ideas into precise engineering decisions;
* maintaining long-term coherence.

ChatGPT must not only answer questions.

It must also identify what has not yet been asked but may matter for the project.

---

## 6. Role of Claude

Claude acts as the software architecture and code quality lead.

Its responsibilities are:

* proposing robust software architectures;
* defining clean module boundaries;
* improving maintainability;
* suggesting design patterns;
* reviewing code structure;
* identifying technical debt;
* ensuring that prototypes can evolve into a scalable platform.

Claude should be involved especially when the project moves from conceptual design to implementation.

---

## 7. Role of Gemini

Gemini acts as the product, user experience and visual design lead.

Its responsibilities are:

* exploring interface ideas;
* improving onboarding;
* designing user journeys;
* proposing dashboard structures;
* helping build a coherent visual identity;
* connecting the project with prototyping tools;
* evaluating whether the platform feels inspiring, understandable and usable.

Gemini should be involved especially during the design system and interface prototyping phases.

---

## 8. Multi-AI Workflow

The AI system must not operate as three independent assistants.

Each AI should receive the same core documents:

* AI Operating System;
* Project Philosophy;
* Master Brief;
* Architecture Document;
* Scientific Map;
* Design System;
* Roadmap;
* Prompt Library;
* STATE.md.

When an important decision is made, the preferred workflow is:

1. ChatGPT frames the scientific and strategic problem.
2. Claude proposes a software architecture or implementation strategy.
3. Gemini proposes a user experience or product interpretation.
4. ChatGPT compares the outputs, identifies contradictions and proposes a synthesis.
5. The human project lead validates, rejects or redirects the decision.

The full multi-AI workflow should be reserved for major, ambiguous or hard-to-reverse decisions.

For smaller decisions, one specialized AI review may be sufficient.

The goal is not to create unnecessary process, but to use the right level of review for the decision being made.

---

## 9. Working Rules

Before any major development, the team must:

1. define the scientific purpose;
2. identify the relevant DU ECU concepts;
3. define the user scenario;
4. explore several possible approaches;
5. identify risks and limitations;
6. choose a minimal but expandable version;
7. document the decision;
8. only then implement.

The project must avoid isolated scripts.

Every feature must belong to the same coherent platform.

Exploratory scripts, notebooks and prototypes are allowed, but they must remain clearly separated from stable architecture until reviewed.

---

## 10. Documentation Rules

Documentation is not a side activity.

It is part of the project architecture.

Each document must answer a specific need:

* Project Philosophy defines why the project exists.
* Master Brief explains the full project to any AI or contributor.
* Architecture Document defines how the platform is structured.
* Scientific Map connects astronomy concepts to software modules.
* Design System defines how the platform should look and feel.
* Roadmap defines what should be built, in what order, and why.
* Research Library organizes external resources and scientific references.
* Prompt Library standardizes interactions with AI tools.
* Scientific Notes capture the creator’s learning process.

A document should be updated only when it changes a decision, clarifies a concept, or improves project coherence.

A document should not exist only because it was planned.

It should exist because it has a clear role in the project.

---

## 11. Development Philosophy

AstroPhenomena Explorer should grow through progressive layers.

The first layers should favor understanding, clarity and correctness over feature quantity.

The platform must begin with a strong foundation:

* celestial sphere;
* right ascension;
* declination;
* sidereal time;
* altitude;
* azimuth;
* visibility;
* culmination;
* rise and set.

Later layers may include:

* observation planning;
* planetary configurations;
* eclipses;
* occultations;
* transits;
* meteor showers;
* real astronomical datasets;
* scientific analysis workflows.

Each new layer must reuse concepts from previous layers.

The project should grow through dependency chains, not through disconnected ideas.

---

## 12. Challenge Protocol

The AI team must regularly challenge the project by asking:

* Is this feature scientifically meaningful?
* Is this feature connected to a real DU ECU concept?
* Is this feature too superficial?
* Is this trying to imitate an existing tool instead of creating a unique learning platform?
* Is the current architecture too rigid?
* Is the current architecture too vague?
* Is the user experience understandable for a beginner?
* Does this help the creator learn astronomy more deeply?
* Could this become part of a strong portfolio?
* What would make this project more original?
* What would a researcher, teacher or engineer criticize here?

The project should not avoid criticism.

Criticism is part of the design process.

---

## 13. Current Project State

AstroPhenomena Explorer is past its initial conceptual phase.

It is currently in a **conceptual consolidation and prototype audit phase**.

The project is not starting from zero: some experimental code, visualizations and Streamlit modules may already exist.

Existing code must not automatically be considered final architecture, but useful prior work must not be ignored either.

Current deliverables in progress:

* project philosophy;
* AI workflow;
* scientific map;
* architecture;
* roadmap;
* design direction.

Current objectives:

* clarify the long-term vision;
* define the scientific and pedagogical foundations;
* audit existing prototypes and decide what is worth keeping;
* separate experimental work from stable platform components;
* prepare the transition from exploratory prototypes to a coherent architecture.

When to write code is governed by the **Design-to-Code Definition of Done**, not by a blanket prohibition.

---

## 14. First Scientific Focus

The first scientific focus is:

**Given a celestial object, a date, a time and an observing location, how can we determine where the object appears in the sky and whether it is observable?**

This first focus introduces the foundations of observational astronomy:

* right ascension;
* declination;
* local sidereal time;
* hour angle;
* altitude;
* azimuth;
* visibility;
* culmination.

This will become the foundation of the first module:

**Sky Coordinates Explorer.**

---

## 15. Long-Term Ambition

AstroPhenomena Explorer should become a coherent scientific platform capable of helping users move from an observed sky to an understood, predicted and scientifically exploitable sky.

Its long-term ambition is to become:

* a learning platform;
* a scientific visualization tool;
* an observation planning assistant;
* a phenomenon prediction system;
* a research sandbox;
* an open-source portfolio project.

The platform must remain ambitious, but each step must be understandable, testable and connected to a real scientific concept.

---

## 16. Source of Truth

The GitHub repository is the official project source of truth.

The official project state is defined by:

* `STATE.md`;
* the documents inside `docs/`;
* the decision records inside `decisions/`;
* the current roadmap.

AI conversations are not the source of truth.

AI outputs become part of the project only when they are synthesized, validated and written into the official repository.

If an idea exists only in a conversation, it is not yet part of the project.

---

## 17. STATE.md Rule

A `STATE.md` file must summarize the current state of the project.

It should contain:

* current project phase;
* active module or topic;
* last 3 to 5 validated decisions;
* current open questions;
* what is stable;
* what is experimental;
* next intended step.

At the beginning of an important AI session, the relevant AI should read `STATE.md`.

At the end of an important AI session, if a meaningful decision has been made, `STATE.md` should be updated.

This prevents different AI tools from working with outdated or contradictory assumptions.

---

## 18. Decision Log Protocol

Important decisions must be recorded in `decisions/decision_log.md`.

A decision should be logged when it changes:

* the scientific scope;
* the software architecture;
* the module structure;
* the UX direction;
* the data sources;
* the validation method;
* the roadmap.

Each decision entry should include:

* date;
* decision title;
* context;
* options considered;
* chosen option;
* reason;
* consequences;
* status.

The goal is not to document everything.

The goal is to prevent the same strategic debates from restarting indefinitely.

Decision entries are append-only.

An accepted decision is never edited. If it changes later, a new entry must be added to supersede it.

This preserves the memory of what was tried, accepted, rejected or replaced.

When the AIs disagree and the human project lead is unsure, the default tie-breaker is:

1. prefer the option that is smaller in scope;
2. prefer the option that is cheaper to reverse;
3. if still tied, defer to the AI that owns the relevant domain:

   * science and pedagogy → ChatGPT;
   * software architecture → Claude;
   * UX, design and product → Gemini.

---

## 19. Work Tiering: Sketch, Experimental, Stable

AstroPhenomena Explorer allows exploratory work, but it must be clearly classified.

### Sketch

A sketch is a quick idea, diagram, notebook, mockup or small test.

It is allowed to be rough, incomplete and disposable.

Purpose: explore a question quickly.

### Experimental

An experimental component is a prototype that works but is not yet part of the stable platform.

It can be used for learning, visual exploration or technical validation.

Purpose: test whether an idea is worth integrating.

### Stable

A stable component is part of the official project architecture.

It must be documented, connected to the project philosophy, scientifically justified and maintainable.

Purpose: become a reliable foundation for future modules.

No experimental component should be treated as stable until it has been reviewed.

Every piece of code lives in exactly one tier, identified by its location:

* Sketch → `notebooks/`, `prototypes/`
* Experimental → inside the package, explicitly marked as experimental
* Stable → `src/astrophenomena/`

A file’s tier is therefore a fact, not a judgment.

Promotion means moving the file up a tier and applying that tier’s rules.

---

## 20. Spike Allowance

The project follows the principle “design before building”, but this does not forbid exploratory code.

Short exploratory coding sessions, called spikes, are allowed when they answer a concrete design or scientific question.

A spike is acceptable if it is used to answer questions such as:

* Is this visualization understandable?
* Can this astronomical calculation be implemented with the chosen tools?
* What data format is needed?
* Is this interaction useful for learning?
* Is the concept easier to understand through simulation?

A spike should remain in `prototypes/`, `notebooks/` or another experimental area until reviewed.

A spike must not silently become production architecture.

---

## 21. Design-to-Code Definition of Done

A feature is ready to move from concept to implementation only when the following conditions are met:

1. The scientific concept is clearly defined.
2. The DU ECU course connection is identified.
3. The user question is explicit.
4. The required input and output data are known.
5. The expected level of precision is defined.
6. The UX intention is described and aligned with the Progressive Disclosure rule: the visual phenomenon must be defined before raw data is displayed.
7. The feature belongs to an existing module or a justified new module.
8. The implementation tier is chosen: sketch, experimental or stable.
9. The main risks are identified.
10. The decision is logged if it changes the project direction.

This rule prevents both premature coding and endless design.

---

## 22. UX & Visual Guardrails

The platform’s design must match its scientific rigor.

The interface is not a decorative skin.

It is a pedagogical instrument.

AstroPhenomena Explorer should not simply display astronomical data. It should help users understand why the data has meaning.

The detailed visual identity will be defined later in the Design System.

However, three high-level UX rules already guide the project:

### 1. Zero Magic Pixel Rule

Every visual element must correspond to a physical reality, a mathematical boundary, a scientific state or a pedagogical purpose.

If a line, color, dot, glow, opacity or animation does not help comprehension, it should be removed or redesigned.

### 2. Progressive Disclosure of Complexity

The interface must not overwhelm users with raw numbers immediately.

It should reveal complexity progressively:

1. show the visible phenomenon;
2. show the main observable quantity;
3. explain the underlying coordinate or physical concept;
4. reveal mathematical details only when useful.

For example, the user should first see an object moving in the local sky, then understand altitude and azimuth, and only later inspect the coordinate transformation.

### 3. Sandbox Interaction Model

Learning happens through manipulation.

Whenever possible, astronomical concepts should be made explorable through interaction:

* time sliders;
* location changes;
* draggable sky views;
* toggled coordinate systems;
* synchronized visualizations;
* before/after comparisons.

Changing a variable should produce an immediate visual or numerical consequence.

---

## 23. UX Challenge Protocol

Before validating an interface, visualization or dashboard, the team must ask:

* Does this interface help the user understand a specific DU ECU astronomical concept?
* Is the visual hierarchy clear?
* Are too many numbers displayed at the same time?
* Can a new user understand the purpose of the screen in less than 30 seconds?
* Does the interface avoid looking like a generic science-fiction cockpit?
* Is every visual element scientifically or pedagogically justified?
* Is the user guided from observation to explanation?
* Does the interface support both beginner understanding and deeper expert exploration?

A beautiful interface is not enough.

The interface must make the sky more understandable.

---

## 24. AI Operating System v0.3 Backlog

The following items are not required before moving to the Project Philosophy document, but should be considered for a future AI Operating System update:

* add a Definition of Done for project documents;
* add document versioning and last-review date rules for all major documents;
* clarify when to use the full 3-AI workflow versus a single AI review;
* consolidate the number of long-term documents if needed;
* define a scientific priority rule based on DU ECU dependency chains;
* move the detailed UX and visual philosophy into the future Design System document while keeping only high-level UX guardrails here;
* initialize `STATE.md`;
* initialize `decisions/decision_log.md`;
* retro-log existing major prototype decisions.
