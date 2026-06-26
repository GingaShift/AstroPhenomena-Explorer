## Patch for `docs/03_Scientific_Map.md` — v0.2 Updates

### Update document header

Replace the current header metadata with:

```md
**Version:** v0.2  
**Status:** Reviewed by Gemini and Claude; minor corrections integrated  
**Language:** English-first, bilingual-ready later  
**Document role:** Map scientific concepts from the Knowledge Base to project axes, software modules, calculations, visualizations and development priorities.
```

---

## 2.2 Status of Course Cards

Add this section after the Source Base tables.

````md
## 2.2 Status of Course Cards

The Course Cards referenced in this document are part of the project Knowledge Base and should be stored in:

```txt
knowledge/course_cards/
````

They provide the course-level scientific summaries used to build this Scientific Map.

For the Scientific Map to claim full traceability, the relevant Course Cards must be committed to the repository alongside this document.

If a reviewer or AI agent does not have access to `knowledge/course_cards/`, the Scientific Map should still be treated as a valid project-level synthesis, but not as independently source-verifiable.

The Course Cards are not implementation specifications. They are scientific knowledge inputs.

The Scientific Map transforms them into project axes, modules, calculations, visualizations and development priorities.

````

---

## 3.3 Axis Dependency Graph

Add this section after the current five-axis sequence.

```md
## 3.3 Axis Dependency Graph

The five axes are not a strictly linear waterfall.

Some simulation and visualization modules can depend directly on Axe 1 foundations without waiting for the full completion of Axe 3.

The dependency structure is closer to a graph:

```txt
Axe 1 — Coordinates, time, local sky
        ↓
        ├── Axe 2 — Observation and visibility
        │          ↓
        │          Axe 3 — Phenomena prediction
        │                    ↓
        │                    Axe 4a — Phenomena geometry simulations
        │
        ├── Axe 4a — Local geometric simulations
        │
        └── Axe 5 — Scientific data foundations
                   ↑
                   └── Later enriched by Axes 2, 3 and 4

Axe 4b — Abstract astrophysical simulations
        depends on specialized later modules and is not part of the early MVP.
````

[DIAGRAM NEEDED — Scientific Axis Dependency Graph]

This distinction prevents the project from blocking all simulation work until every prediction module is complete.

For example:

* a coordinate transformation simulator can be built from Axe 1;
* a Moon phase geometry simulator can be built from basic Sun-Earth-Moon geometry;
* a full eclipse prediction module depends on more advanced Axe 3 foundations.

````

---

## 5.4 Axis 4 Stratification: Geometry vs Astrophysics

Replace or extend Section 5.4 with this clarification.

```md
## 5.4 Axis 4 — Simuler les phénomènes

### Core purpose

Axe 4 answers:

> **Why does this phenomenon happen, geometrically or physically?**

This axis turns calculations into visual intuition.

However, not all simulations have the same complexity.

Axis 4 is therefore split into two tiers.

---

## 5.4.1 Tier 4a — Local Geometric Simulations

Tier 4a contains simulations that directly support the early platform.

These are mostly geometric, topocentric or Solar System-based simulations.

They are prioritized earlier because they help users understand what they see in their sky.

| Concept | Role | Priority |
|---|---|---|
| Coordinate transformation | Explain RA/Dec to Alt/Az | Must-have |
| Local sky dome | Show horizon, altitude, azimuth and meridian | Must-have |
| Moon phases | Explain Sun-Earth-Moon geometry | Important |
| Eclipse geometry | Explain shadow, penumbra and alignment | Important |
| Occultation geometry | Explain observer-dependent hiding | Important |
| Keplerian orbit | Show elliptical motion and changing speed | Important |
| Orbital inclination | Explain nodes and rare alignments | Important |
| Apparent diameter | Explain total, annular and transit events | Important |

Possible early modules:

| Module | Purpose | Priority |
|---|---|---|
| Coordinate Transformation Simulator | Explain RA/Dec to Alt/Az | Must-have |
| Local Sky Dome Simulator | Show object movement across local sky | Must-have |
| Moon Phase Simulator | Explain lunar phases | Important |
| Eclipse Geometry Simulator | Explain eclipse conditions | Important |
| Basic Orbit Simulator | Explain Keplerian motion | Important |

---

## 5.4.2 Tier 4b — Abstract Astrophysical Simulations

Tier 4b contains simulations that require deeper physical models, external datasets or more advanced scientific assumptions.

These are part of the long-term scientific ambition, but they should not block the early roadmap.

| Concept | Role | Priority |
|---|---|---|
| HR diagram | Explain stellar classification and evolution | Advanced |
| Stellar evolution | Show mass-dependent stellar futures | Advanced |
| Galaxy rotation curves | Explain dark matter evidence | Advanced |
| Solar magnetism | Explain active regions and space weather | Advanced |
| Tidal heating | Explain Io, Europa and Enceladus activity | Advanced |
| AGN jet beaming | Explain relativistic orientation effects | Future |
| Gravitational-wave chirp | Explain inspiral and merger signal | Future |

Possible later modules:

| Module | Purpose | Priority |
|---|---|---|
| HR Diagram Explorer | Stellar populations and evolution | Advanced |
| Galaxy Rotation Curve Explorer | Dark matter intuition | Advanced |
| Solar Activity Visualizer | Magnetism and space weather | Advanced |
| Tidal Heating Simulator | Active icy worlds | Advanced |
| High-Energy Phenomena Lab | Jets, GRBs and gravitational waves | Future |

This split ensures that early geometric simulations remain feasible while preserving the long-term astrophysical scope of the project.
````

---

## 7.1.bis Progressive Disclosure UI Layout Schema

Add this after Section 7.1.

````md
## 7.1.bis Progressive Disclosure UI Layout Schema

Every must-have scientific visual linked to an interactive module should follow a progressive disclosure structure.

The user should first see the phenomenon, then progressively access the quantities, concepts and formulas behind it.

The standard interaction model is:

```txt
Phenomenon
   ↓
Observable quantity
   ↓
Conceptual geometry
   ↓
Scientific formula / model
````

This maps to four UI layers:

| UI layer          | Role                                       | Example                                             |
| ----------------- | ------------------------------------------ | --------------------------------------------------- |
| Phenomenon Canvas | Shows what is happening visually           | A star moving across the local sky                  |
| Observable Metric | Shows the immediate measurable quantity    | Current altitude: 45°                               |
| Conceptual Grid   | Reveals the geometry behind the phenomenon | Horizon, meridian, RA/Dec grid, Alt/Az grid         |
| Science Core      | Opens the underlying formula or model      | Hour angle relation, RA/Dec → Alt/Az transformation |

[DIAGRAM NEEDED — Progressive Disclosure UI Template]

This layout prevents the interface from becoming either too magical or too academic.

The user should be able to stay at the visual level, but also open the scientific layers when ready.

````

---

## 9.5 Naming Convention for Modules

Add this after the Priority Matrix.

```md
## 9.5 Naming Convention for Modules

Some names in this document refer to different abstraction levels.

To avoid duplicate implementation, the following distinction must be respected:

| Level | Meaning | Example |
|---|---|---|
| User-facing feature | What the user sees and uses | Sky Coordinates Explorer |
| Calculation engine / service | Internal scientific capability | Local Sky Engine, Visibility Engine |
| Utility layer | Shared lower-level logic | Time utilities, coordinate utilities |
| Package / folder | Code organization | `coordinates/`, `time/`, `visibility/` |

Example:

```txt
Sky Coordinates Explorer
    uses Local Sky Engine
        uses Time Engine / time utilities
        uses coordinate transformation utilities
````

The Architecture Document must define these layers precisely.

Until then, the names in this Scientific Map should be treated as conceptual module names, not final package names.

````

---

## 12. Scientific Map to Feature Brief Bridge

Replace the example Feature Brief in Section 12 with the following version.

```md
Example future Feature Brief:

```text
Feature name:
Sky Coordinates Explorer — Prototype 001

Scientific concept:
RA/Dec to Alt/Az transformation using observer location and local sidereal time.

User question:
Where is this object in my sky right now?

Input / Output:
Input:
- object right ascension;
- object declination;
- observer latitude;
- observer longitude;
- date and time.

Output:
- altitude;
- azimuth;
- visibility status;
- basic scientific explanation.

Target tier:
Prototype (`prototypes/`)

Target location:
`prototypes/sky_coordinates_001/`

Constraints:
- use Astropy only for astronomical calculations;
- no atmospheric refraction;
- no proper motion correction;
- no weather integration;
- no telescope simulation;
- document time and coordinate assumptions.

Expected output:
- function returning altitude, azimuth and visibility status;
- basic explanation string;
- local sky dome visualization;
- altitude-through-time curve.

Out of scope:
- full Observation Planner;
- weather and seeing;
- advanced Moon brightness modeling;
- telescope field-of-view simulation;
- high-precision precession/nutation handling;
- production-ready UI.

Linked decision:
`decisions/0001-astropy-as-calculation-library.md`  
or equivalent decision-log entry to create before implementation.
````

This example follows the same Feature Brief structure required by the Master Brief.

````

---

## 13.1 Recommended visuals

Update the Section 13.1 table by adding these rows.

```md
| Visual | Purpose | Status |
|---|---|---|
| Scientific Axis Dependency Graph | Show real dependencies between axes, not only a linear sequence | Needed |
| Progressive Disclosure UI Template | Show how a scientific module reveals phenomenon, metric, concept and formula | Needed |
````

---

## 15. What Every AI Must Remember from This Scientific Map

Add this reminder to the list.

```md
14. Axis 4 is split into early local geometric simulations and later abstract astrophysical simulations.
15. User-facing feature names, internal engines and package names are not the same thing; the Architecture Document must define their mapping.
16. Feature Briefs must follow the exact template defined in the Master Brief.
```
