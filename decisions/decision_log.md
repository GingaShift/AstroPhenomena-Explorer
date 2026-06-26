## Decision — Scientific Map v0.2 validated

**Date:** 2026-06-26  
**Status:** Accepted  

`docs/03_Scientific_Map.md` v0.2 is accepted as the official scientific mapping document for AstroPhenomena Explorer.

It defines the mapping between:

- Course Cards;
- scientific concepts;
- project axes;
- software modules;
- calculations;
- visualizations;
- priorities.

---

## Decision — Course Cards as scientific knowledge inputs

**Date:** 2026-06-26  
**Status:** Accepted  

Course Cards stored in `knowledge/course_cards/` are the official scientific knowledge inputs for the project.

They summarize scientific sources but are not implementation specifications.

---

## Decision — Axe 1 as first implementation foundation

**Date:** 2026-06-26  
**Status:** Accepted  

Axe 1 — Sky coordinates, time, observer location, Alt/Az and visibility — is the first scientific implementation foundation.

The first technical architecture must support the Sky Coordinates Explorer before broader modules are implemented.

---

## Decision — Axis 4 stratification

**Date:** 2026-06-26  
**Status:** Accepted  

Axis 4 is split into:

- Tier 4a — local geometric simulations;
- Tier 4b — abstract astrophysical simulations.

Tier 4a can be developed earlier. Tier 4b belongs to advanced or future phases.

---

## Decision — Feature Brief format

**Date:** 2026-06-26  
**Status:** Accepted  

All future Feature Briefs must follow the template defined in the Master Brief.

No coding agent should implement a serious feature without a Feature Brief.

Astropy-first
dataclasses for core models
type annotations required in stable code
object protocol with get_equatorial_position(time)
UI-agnostic visualization layer
no top-level explanations package
phenomena namespace reserved
Prototype 001 before stable implementation
