# AstroPhenomena Explorer — Architecture Document v0.2

**Version:** v0.2
**Status:** Reviewed by Gemini and Claude; architecture blockers integrated
**Document role:** Define the software architecture that transforms the Scientific Map into a maintainable Python project.
**Main focus:** Prepare the first implementation layer for the Sky Coordinates Explorer.

---

## 1. Purpose of This Document

This Architecture Document defines how AstroPhenomena Explorer should be structured technically.

It answers the question:

> **How should the project be organized so that scientific concepts become reliable, testable, visual and extensible software modules?**

This document translates the validated scientific foundations into:

* repository structure;
* Python package structure;
* module boundaries;
* public API rules;
* data models;
* calculation engines;
* visualization responsibilities;
* testing strategy;
* prototype workflow;
* coding-agent constraints.

This document does **not** implement features.

It prepares the project so that future implementation can happen safely, progressively and without architectural chaos.

---

## 2. Source Documents

This architecture is based on the currently validated project documents:

| Document                    | Role                                                                                    |
| --------------------------- | --------------------------------------------------------------------------------------- |
| `00_AI_Operating_System.md` | Defines AI roles, workflow rules, decision process and prototype/stable separation      |
| `01_Project_Philosophy.md`  | Defines vision, product identity and scientific-design philosophy                       |
| `02_Master_Brief.md`        | Defines operational project brief, axes, workflow and document hierarchy                |
| `03_Scientific_Map.md`      | Defines scientific concepts, axes, modules, calculations, visualizations and priorities |
| `knowledge/course_cards/`   | Provides course-level scientific source summaries                                       |

The Architecture Document must remain consistent with these documents.

If there is a conflict:

```txt
AI Operating System
   ↓
Project Philosophy
   ↓
Master Brief
   ↓
Scientific Map
   ↓
Architecture Document
   ↓
Feature Briefs
   ↓
Code
```

The Architecture Document does not override the scientific or strategic documents.

It translates them into technical structure.

---

## 3. Architectural Philosophy

AstroPhenomena Explorer must be designed as a scientific platform, not as a collection of disconnected scripts.

The architecture must support five principles:

1. science-first architecture;
2. engines before interface;
3. prototype before stable implementation;
4. modular and reversible growth;
5. type-safe stable code.

---

## 3.1 Science-First Architecture

Every serious feature must be connected to:

* a scientific concept;
* a user question;
* a calculation or dataset;
* a visualization;
* a traceability note;
* a validation path.

A feature that cannot identify its scientific basis is not ready for implementation.

A scientific module should always be able to answer:

| Question                           | Example                                             |
| ---------------------------------- | --------------------------------------------------- |
| What concept does it implement?    | RA/Dec to Alt/Az conversion                         |
| What user question does it answer? | Where is this object in my sky?                     |
| What inputs does it require?       | Object coordinates, time, observer location         |
| What outputs does it produce?      | Altitude, azimuth, visibility status                |
| What assumptions does it make?     | No refraction, no weather, fixed horizon            |
| How is it validated?               | Compared against Astropy / Stellarium / known cases |

---

## 3.2 Engines Before Interface

The first stable layers should be calculation and data engines.

The UI should consume scientific results.

The UI should not own the scientific logic.

Correct pattern:

```txt
scientific engine
      ↓
typed result object
      ↓
visualization layer
      ↓
user interface
```

Wrong pattern:

```txt
Streamlit page
      ↓
hidden calculations inside UI callbacks
      ↓
unusable outside the page
```

The project must avoid locking science inside Streamlit components.

Scientific logic belongs in:

```txt
src/astrophenomena/
```

Streamlit rendering belongs in:

```txt
app/streamlit/
```

---

## 3.3 Prototype Before Stable Implementation

The project may use prototypes, notebooks and experiments.

However, prototypes do not automatically become stable code.

A prototype may test:

* a calculation;
* a UI layout;
* a visual interaction;
* a scientific explanation;
* a dataset;
* a workflow.

Stable code belongs in:

```txt
src/astrophenomena/
```

Prototype code belongs in:

```txt
prototypes/
```

Notebook exploration belongs in:

```txt
notebooks/
```

A successful prototype should be reviewed before any logic is promoted into the stable package.

---

## 3.4 Modular, Reversible Growth

The architecture should allow the project to grow from:

```txt
Axe 1 — Sky coordinates
```

toward:

```txt
observation planning
phenomena prediction
simulation
real data analysis
hardware-assisted observation
```

without requiring a complete rewrite.

Each module should have clear boundaries and should be replaceable if better scientific methods are adopted later.

Example:

```txt
Sky Coordinates Explorer
    uses Local Sky Engine
        uses time/
        uses coordinates/
        uses observers/
        uses objects/
```

The user-facing feature can evolve without rewriting the lower-level engines.

---

## 3.5 Type Annotation Policy

All stable code in `src/astrophenomena/` must use Python type annotations.

This is not optional.

Type annotations are required because they:

* improve output quality from coding agents;
* prevent interface mismatches between modules;
* make public APIs self-documenting;
* support future static checking with tools such as `mypy` or `pyright`;
* reduce ambiguity between scientific engines.

Prototype code in `prototypes/` and exploratory notebooks in `notebooks/` are exempt from this strict requirement.

The use of `Any` is discouraged and must be justified with a short comment when unavoidable.

---

## 4. Target Repository Structure

The recommended repository structure is:

```txt
AstroPhenomena-Explorer/
│
├── README.md
├── STATE.md
│
├── docs/
│   ├── 00_AI_Operating_System.md
│   ├── 01_Project_Philosophy.md
│   ├── 02_Master_Brief.md
│   ├── 03_Scientific_Map.md
│   ├── 04_Architecture_Document.md
│   ├── 05_Design_System.md
│   ├── 06_Roadmap.md
│   └── ...
│
├── decisions/
│   ├── decision_log.md
│   └── open_questions.md
│
├── knowledge/
│   ├── README.md
│   └── course_cards/
│       ├── du_ecu_celestial_sphere_astrometry.md
│       ├── du_ecu_time_calendars.md
│       ├── du_ecu_celestial_mechanics.md
│       └── ...
│
├── ai_reviews/
│   ├── chatgpt/
│   ├── claude/
│   └── gemini/
│
├── assets/
│   ├── master_brief/
│   ├── scientific_map/
│   └── design/
│
├── prototypes/
│   └── sky_coordinates_001/
│
├── notebooks/
│   ├── coordinates/
│   ├── visibility/
│   ├── phenomena/
│   └── data_analysis/
│
├── src/
│   └── astrophenomena/
│       ├── __init__.py
│       ├── time/
│       ├── coordinates/
│       ├── observers/
│       ├── objects/
│       ├── visibility/
│       ├── phenomena/
│       ├── visualizations/
│       └── data/
│
├── tests/
│   ├── test_time/
│   ├── test_coordinates/
│   ├── test_observers/
│   ├── test_objects/
│   ├── test_visibility/
│   ├── test_phenomena/
│   ├── test_visualizations/
│   ├── test_data/
│   └── conftest.py
│
├── app/
│   └── streamlit/
│
├── pyproject.toml
├── requirements.txt
└── .gitignore
```

---

## 5. Repository Layer Responsibilities

| Folder                | Responsibility                                             |
| --------------------- | ---------------------------------------------------------- |
| `docs/`               | Official project documents                                 |
| `decisions/`          | Accepted decisions and open questions                      |
| `knowledge/`          | Scientific knowledge base derived from courses and sources |
| `ai_reviews/`         | Reviews from ChatGPT, Claude and Gemini                    |
| `assets/`             | Diagrams, images, visual references                        |
| `prototypes/`         | Structured experimental prototypes                         |
| `notebooks/`          | Exploratory scientific notebooks                           |
| `src/astrophenomena/` | Stable Python package                                      |
| `tests/`              | Unit tests and scientific validation tests                 |
| `app/`                | User interfaces, including Streamlit                       |
| `resources_private/`  | Local private raw course files, not committed              |

---

## 6. Private Resources Policy

Raw course PDFs and copyrighted educational material should not be committed to the public repository unless explicit permission exists.

Private resources should remain local:

```txt
resources_private/
└── raw_courses/
```

The `.gitignore` should include:

```txt
resources_private/
```

The public repository should contain:

* personal summaries;
* Course Cards;
* diagrams created for the project;
* scientific notes;
* code;
* tests;
* documentation.

The public repository should not contain:

* raw private course PDFs;
* copyrighted lecture slides;
* copied course diagrams without permission;
* long verbatim course extracts.

---

## 7. Python Package Architecture

The stable package should live in:

```txt
src/astrophenomena/
```

The package should separate scientific logic from interface code.

Recommended first package structure:

```txt
src/astrophenomena/
├── __init__.py
│
├── time/
│   ├── __init__.py
│   ├── models.py
│   ├── scales.py
│   ├── sidereal.py
│   └── julian.py
│
├── coordinates/
│   ├── __init__.py
│   ├── models.py
│   ├── equatorial.py
│   ├── horizontal.py
│   ├── transforms.py
│   └── frames.py
│
├── observers/
│   ├── __init__.py
│   ├── models.py
│   └── validation.py
│
├── objects/
│   ├── __init__.py
│   ├── models.py
│   ├── protocols.py
│   ├── fixed.py
│   ├── catalog.py
│   └── solar_system.py
│
├── visibility/
│   ├── __init__.py
│   ├── models.py
│   ├── status.py
│   ├── windows.py
│   └── constraints.py
│
├── phenomena/
│   └── __init__.py
│
├── visualizations/
│   ├── __init__.py
│   ├── sky_dome.py
│   ├── altitude_curve.py
│   └── diagrams.py
│
└── data/
    ├── __init__.py
    ├── sources.py
    └── loaders.py
```

This is a candidate structure.

It may be refined during implementation, but coding agents must not invent new top-level packages without review.

---

## 7.1 Public API Rule for Subpackages

Each subpackage must explicitly define its public API in its `__init__.py`.

External callers should import from the subpackage public API, not from internal implementation files.

Preferred pattern:

```python
from astrophenomena.coordinates import ra_dec_to_alt_az
```

Discouraged pattern:

```python
from astrophenomena.coordinates.transforms import _internal_transform_helper
```

Rules:

* `__init__.py` should export only the stable public API of the subpackage.
* Internal helpers should remain private.
* Other packages should not depend on private implementation details.
* Coding agents must not expose all internal functions automatically.

Example:

```python
# src/astrophenomena/coordinates/__init__.py

from .models import EquatorialCoordinates, HorizontalCoordinates
from .transforms import ra_dec_to_alt_az

__all__ = [
    "EquatorialCoordinates",
    "HorizontalCoordinates",
    "ra_dec_to_alt_az",
]
```

---

## 7.2 Initial `phenomena/` Placeholder Rule

The `phenomena/` package is reserved for later Axe 3 and Axe 4 work.

It should not be populated with implementation files too early.

Initial structure:

```txt
src/astrophenomena/
└── phenomena/
    └── __init__.py
```

Initial content of `phenomena/__init__.py`:

```python
"""
Namespace reserved for Axe 3 — Phenomena Prediction
and Axe 4 — Phenomena Simulation.

Do not implement phenomena modules until the following foundations are stable:
- time/
- coordinates/
- observers/
- objects/
- visibility/

See docs/03_Scientific_Map.md Sections 5.3 and 5.4.
"""
```

This prevents coding agents from prematurely implementing eclipses, occultations, meteor showers or conjunctions before the foundations are stable.

---

## 7.3 No Generic `utils/` by Default

The first stable architecture should avoid a generic top-level `utils/` package.

Generic utility folders tend to become unstructured containers.

Instead:

* validation logic belongs close to the model being validated;
* coordinate helpers belong in `coordinates/`;
* observer validation belongs in `observers/`;
* unit handling should use `astropy.units` where possible;
* shared helpers should only become a package when repeated use justifies it.

A future `utils/` or `core/` package may be introduced only if there is a clear architectural need.

---

## 8. Architecture Layers

The project should distinguish between four abstraction levels.

| Level               | Meaning                        | Example                                |
| ------------------- | ------------------------------ | -------------------------------------- |
| User-facing feature | What the user sees             | Sky Coordinates Explorer               |
| Scientific engine   | Internal scientific capability | Local Sky Engine                       |
| Utility layer       | Shared lower-level logic       | Time utilities, coordinate conversions |
| Package / folder    | Code organization              | `coordinates/`, `time/`, `visibility/` |

Example:

```txt
Sky Coordinates Explorer
    uses Local Sky Engine
        uses coordinates/
        uses time/
        uses observers/
        uses objects/
    uses Visibility Engine
        uses visibility/
```

This distinction prevents duplicate modules.

For example, `Sky Coordinates Explorer` and `Local Sky Engine` are not two independent product features.

The first is user-facing.

The second is a scientific calculation capability.

---

## 9. First Implementation Target

The first implementation layer should support:

```txt
Sky Coordinates Explorer
```

The first scientific question is:

> **Given an object, a time and an observing location, where is the object in the local sky and is it observable?**

This requires:

* time handling;
* observer model;
* object coordinates;
* coordinate transformation;
* visibility logic;
* basic visualization;
* traceable assumptions.

---

## 10. First Stable Scientific Pipeline

The first scientific pipeline should be:

```txt
Object identifier / RA-Dec
        ↓
Observer location
        ↓
Date and time
        ↓
Time handling
        ↓
Local sidereal time
        ↓
Coordinate transformation
        ↓
Altitude / azimuth
        ↓
Visibility status
        ↓
Explanation and visualization
```

The first architecture must support this pipeline before adding more advanced features.

---

## 11. Core Data Models

The first implementation should use explicit typed data objects.

These objects should be simple, testable and independent from UI frameworks.

---

## 11.0 Data Model Implementation Pattern

All core data models in `src/astrophenomena/` should use Python `dataclasses` with explicit type annotations.

Plain dictionaries must not be used for core scientific result objects.

Recommended pattern:

```python
from dataclasses import dataclass

@dataclass(frozen=True)
class SkyPosition:
    altitude_deg: float
    azimuth_deg: float
    hour_angle_deg: float
    local_sidereal_time_hours: float
    is_above_horizon: bool
    calculated_at_utc: str
```

Rationale:

* lightweight standard-library solution;
* readable by any Python developer;
* improves coding-agent output quality;
* easy to test;
* explicit enough for early architecture;
* avoids premature dependency on heavier validation frameworks.

`pydantic` may be introduced later if validation, JSON serialization or API boundaries become more complex.

Until then, dataclasses are the default for stable internal models.

---

## 11.1 Observer

Represents the observing location.

Suggested dataclass:

```python
from dataclasses import dataclass
from typing import Optional

@dataclass(frozen=True)
class Observer:
    name: str
    latitude_deg: float
    longitude_deg: float
    elevation_m: float = 0.0
    timezone: Optional[str] = None
```

Role:

* provide observer location;
* support local sky calculations;
* support future observation planning.

Validation rules:

* latitude must be between `-90°` and `+90°`;
* longitude must be between `-180°` and `+180°`;
* elevation may be optional for early prototypes.

---

## 11.2 CelestialObject and Astrometric Abstraction

A celestial object must not be modeled only as a static pair of `ra` and `dec` fields.

This would work for fixed stars or deep-sky objects, but it would break as soon as the project introduces dynamic Solar System bodies such as:

* the Moon;
* planets;
* asteroids;
* comets.

The architecture must therefore distinguish between:

| Object category          | Coordinate behavior                                                       |
| ------------------------ | ------------------------------------------------------------------------- |
| Fixed celestial object   | Returns catalog coordinates, usually J2000 or another reference epoch     |
| Dynamic celestial object | Computes or retrieves time-dependent coordinates from an ephemeris source |

The common architectural contract is:

```txt
Celestial object
      ↓
get_equatorial_position(time)
      ↓
EquatorialCoordinates
```

Suggested fixed-object data model:

```python
from dataclasses import dataclass
from typing import Optional

@dataclass(frozen=True)
class EquatorialCoordinates:
    ra_deg: float
    dec_deg: float
    epoch: str = "J2000"

@dataclass(frozen=True)
class FixedCelestialObject:
    name: str
    object_type: str
    coordinates: EquatorialCoordinates
    magnitude: Optional[float] = None
    catalog_id: Optional[str] = None

    def get_equatorial_position(
        self,
        time: "ObservationTime",
    ) -> EquatorialCoordinates:
        return self.coordinates
```

For early versions, fixed objects may ignore the `time` parameter.

Dynamic Solar System objects will later implement the same method by querying an ephemeris engine.

This prevents the Visibility Engine from needing special cases such as:

```python
if object_type == "planet":
    ...
```

The engine should only ask:

```python
coordinates = celestial_object.get_equatorial_position(time)
```

---

## 11.3 ObservationTime

Represents the time of observation.

Suggested dataclass:

```python
from dataclasses import dataclass
from datetime import datetime
from typing import Optional

@dataclass(frozen=True)
class ObservationTime:
    input_datetime: datetime
    utc_datetime: datetime
    timezone: Optional[str] = None
    julian_day: Optional[float] = None
    time_scale: str = "UTC"
```

Role:

* normalize user time input;
* expose astronomical time values;
* support local sidereal time;
* document assumptions.

Initial scope:

* local datetime input;
* UTC conversion;
* optional Julian Day;
* explicit time scale label.

Advanced time scales such as TT, TDB and UT1 are future work.

---

## 11.4 SkyPosition

Represents the local sky result.

Suggested dataclass:

```python
from dataclasses import dataclass

@dataclass(frozen=True)
class SkyPosition:
    altitude_deg: float
    azimuth_deg: float
    hour_angle_deg: float
    local_sidereal_time_hours: float
    is_above_horizon: bool
    calculated_at_utc: str
```

Role:

* return local sky position;
* support visualization;
* support visibility status.

Validation rules:

* altitude should normally be between `-90°` and `+90°`;
* azimuth convention must be documented;
* azimuth should normally be represented within `[0°, 360°)`.

---

## 11.5 VisibilityResult

Represents observability.

Suggested dataclass:

```python
from dataclasses import dataclass, field
from typing import Optional

@dataclass(frozen=True)
class VisibilityResult:
    is_visible: bool
    quality_label: str
    altitude_deg: float
    altitude_threshold_deg: float
    magnitude: Optional[float] = None
    limiting_magnitude: Optional[float] = None
    reasons: tuple[str, ...] = field(default_factory=tuple)
    assumptions: tuple[str, ...] = field(default_factory=tuple)
```

Example `quality_label` values:

```txt
not_visible
low
acceptable
good
excellent
```

The first version may use simple altitude thresholds only.

Later versions can include:

* Moon brightness;
* twilight;
* atmospheric extinction;
* local horizon obstruction;
* weather;
* telescope aperture;
* seeing.

---

## 11.6 ComputationResult Metadata

Every serious calculation result should include metadata.

Suggested dataclass:

```python
from dataclasses import dataclass, field

@dataclass(frozen=True)
class ComputationMetadata:
    created_at_utc: str
    library_used: str
    model_level: str
    assumptions: tuple[str, ...] = field(default_factory=tuple)
    warnings: tuple[str, ...] = field(default_factory=tuple)
    source_notes: tuple[str, ...] = field(default_factory=tuple)
```

Example:

```txt
library_used: Astropy
model_level: simplified_topocentric
assumptions:
  - no atmospheric refraction
  - no weather
  - horizon threshold = 10 degrees
warnings:
  - visibility does not account for Moon brightness
```

This supports scientific traceability.

---

## 12. Time Architecture

Time is a core dependency.

The architecture should isolate time logic in:

```txt
src/astrophenomena/time/
```

Responsibilities:

* parse user date/time;
* convert local time to UTC;
* expose Julian Day when needed;
* compute or delegate sidereal time calculation;
* document time scale assumptions;
* prepare future support for TT, TDB, UT1 and leap seconds.

Initial scope:

| Feature                     | Status                           |
| --------------------------- | -------------------------------- |
| Local datetime input        | Required                         |
| UTC conversion              | Required                         |
| Julian Day                  | Useful                           |
| Local sidereal time         | Required                         |
| Time zone handling          | Required                         |
| Leap second manual handling | Out of scope for first prototype |
| TT / TDB precise handling   | Advanced                         |

Recommended first approach:

> Use Astropy for astronomical time calculations in prototypes and early stable engines.

This should be recorded in the decision log before implementation.

---

## 13. Coordinate Architecture

Coordinate logic should live in:

```txt
src/astrophenomena/coordinates/
```

Responsibilities:

* represent equatorial coordinates;
* represent horizontal coordinates;
* convert RA/Dec to Alt/Az;
* expose hour angle where educationally useful;
* support coordinate assumptions;
* prepare future frame handling.

Initial scope:

| Capability                                  | Status                      |
| ------------------------------------------- | --------------------------- |
| RA/Dec input                                | Required                    |
| Alt/Az output                               | Required                    |
| Hour angle                                  | Required educational output |
| Local sidereal time use                     | Required                    |
| Azimuth convention                          | Must be documented          |
| Atmospheric refraction                      | Out of scope for prototype  |
| Precession / nutation custom implementation | Out of scope                |
| Proper motion                               | Out of scope                |

Implementation rule:

> Prefer trusted astronomy libraries for coordinate transformation. Do not manually implement high-precision spherical astronomy before the scientific validation strategy exists.

---

## 14. Observer Architecture

Observer logic should live in:

```txt
src/astrophenomena/observers/
```

Responsibilities:

* define observing location;
* validate latitude and longitude;
* support common saved locations;
* expose location to coordinate and visibility engines.

Initial example observers:

```txt
Meudon
Paris
Greenwich
Mauna Kea
```

Observer location must always include:

* latitude;
* longitude;
* elevation if available;
* timezone if needed for user-facing display.

Longitude sign convention must be documented.

Validation belongs in the `observers/` package, not in a generic `utils/validation.py`.

---

## 15. Object Architecture

Object logic should live in:

```txt
src/astrophenomena/objects/
```

Responsibilities:

* represent object identity;
* provide coordinates through a stable protocol;
* provide magnitude when available;
* later support Solar System ephemerides;
* later connect to catalogues.

Initial object types:

```txt
star
deep_sky_object
planet
moon
asteroid
comet
meteor_shower
galaxy
```

Initial stable scope should focus on:

```txt
fixed RA/Dec objects
```

such as stars or deep-sky objects.

Solar System objects require ephemerides and should be integrated carefully later.

---

## 15.1 CelestialObject Protocol

Fixed objects and Solar System objects have different coordinate behavior, but scientific engines should interact with them through the same interface.

All celestial objects used by coordinate or visibility engines must satisfy the following protocol:

```python
from typing import Protocol

class CelestialObjectProtocol(Protocol):
    @property
    def name(self) -> str:
        ...

    def get_equatorial_position(
        self,
        time: ObservationTime,
    ) -> EquatorialCoordinates:
        """Return RA/Dec for a given observation time.

        Fixed objects may ignore the time parameter.
        Dynamic objects use the time parameter to query ephemerides.
        """
        ...
```

Implementation rule:

* fixed stars, galaxies and deep-sky objects return catalog coordinates;
* planets, Moon, asteroids and comets later compute time-dependent coordinates;
* engines must accept `CelestialObjectProtocol`, not a concrete `CelestialObject` class.

Solar System ephemeris integration is out of scope for Prototype 001.

However, the protocol must be defined now to prevent a major refactor later.

---

## 16. Visibility Architecture

Visibility logic should live in:

```txt
src/astrophenomena/visibility/
```

Responsibilities:

* determine if an object is above the horizon;
* apply altitude threshold;
* assign visibility quality label;
* explain why an object is or is not visible;
* prepare future observation-window computation.

Initial visibility logic:

```txt
if altitude < 0°:
    not visible

if 0° <= altitude < 10°:
    very low / poor

if 10° <= altitude < 30°:
    acceptable

if altitude >= 30°:
    good
```

These thresholds are project defaults and must be configurable.

Future visibility logic may include:

* twilight;
* Moon phase;
* Moon altitude;
* object magnitude;
* limiting magnitude;
* atmospheric extinction;
* weather;
* seeing;
* local horizon profile;
* telescope constraints.

The Visibility Engine should consume typed result objects, not raw dictionaries.

Example responsibility boundary:

```txt
coordinates/ produces SkyPosition
visibility/ consumes SkyPosition
visibility/ produces VisibilityResult
```

---

## 17. Phenomena Architecture

Phenomena logic should live in:

```txt
src/astrophenomena/phenomena/
```

This is not the first implementation target.

Initial rule:

> `phenomena/` is a reserved namespace only until the foundational engines are stable.

Responsibilities later:

* conjunction detection;
* opposition detection;
* elongation calculation;
* eclipse logic;
* occultation logic;
* transit logic;
* meteor shower windows.

No complex phenomena detector should be implemented before:

* Time Engine;
* Coordinate Engine;
* Observer model;
* Object protocol;
* Visibility Engine;
* basic ephemeris strategy.

---

## 18. Visualization Architecture

Visualization logic should live in:

```txt
src/astrophenomena/visualizations/
```

Responsibilities:

* create scientific plots;
* create local sky dome visualizations;
* create altitude curves;
* create diagrams or data structures for UI rendering;
* avoid embedding business logic.

Recommended first visualizations:

| Visualization                    | Purpose                            |
| -------------------------------- | ---------------------------------- |
| Local sky dome                   | Show altitude and azimuth          |
| Altitude-through-time curve      | Show visibility through the night  |
| Meridian / horizon diagram       | Explain culmination and visibility |
| Coordinate explanation schematic | Explain RA/Dec vs Alt/Az           |

Visualization functions should consume result objects.

They should not recompute scientific logic independently.

Correct pattern:

```txt
SkyPosition result
      ↓
visualization function
      ↓
figure / data for UI
```

Wrong pattern:

```txt
visualization function
      ↓
recomputes coordinates internally
      ↓
duplicated scientific logic
```

---

## 18.1 Visualization Layer Boundary

Visualization functions in `src/astrophenomena/visualizations/` must remain UI-agnostic.

They may produce:

* framework-agnostic data structures, preferred when practical;
* or fully configured figure objects such as `plotly.graph_objects.Figure` or `matplotlib.figure.Figure`.

They must never import or call Streamlit-specific rendering functions.

Forbidden inside `src/astrophenomena/visualizations/`:

```python
import streamlit as st
st.write(...)
st.plotly_chart(...)
st.pyplot(...)
```

Correct boundary:

```txt
src/astrophenomena/visualizations/sky_dome.py
        ↓
returns Plotly Figure or structured visual data
        ↓
app/streamlit/pages/01_Sky_Coordinates_Explorer.py
        ↓
renders with st.plotly_chart(...)
```

The presentation layer owns rendering.

The visualization layer owns figure construction.

The scientific engine owns calculations.

These boundaries must not be crossed.

---

## 18.2 Progressive Disclosure Rendering Contract

The Progressive Disclosure UI Pattern requires four layers:

```txt
Phenomenon Canvas
      ↓
Observable Metric
      ↓
Conceptual Grid
      ↓
Science Core
```

Architectural implications:

| UI layer          | Architecture responsibility                                                                 |
| ----------------- | ------------------------------------------------------------------------------------------- |
| Phenomenon Canvas | Usually rendered from a figure object or structured visual data                             |
| Observable Metric | Rendered by the UI from result objects                                                      |
| Conceptual Grid   | Should be produced as an overlay or toggleable layer in the same visual space as the canvas |
| Science Core      | Rendered by the UI as a collapsed panel, drawer or expander                                 |

For Streamlit prototypes:

* Canvas and grid may share the same Plotly figure.
* Metrics may use Streamlit metric cards or Markdown.
* Science Core may use `st.expander`, collapsed by default.
* Scientific formulas should not dominate the initial interface.

---

## 19. Explanation Architecture

The project needs explanations, but explanations should not become a vague global package.

Initial decision:

> Do not create a top-level `explanations/` package in the first stable architecture.

Instead, explanations should be colocated with the relevant scientific module or returned as structured metadata.

Example:

```txt
visibility/
├── status.py
└── explanations.py
```

or:

```txt
VisibilityResult
└── reasons
```

The Architecture Document reserves the right to define a dedicated explanation system later if needed.

For now:

* short explanations can be returned by engines;
* long educational text belongs in documentation or UI content;
* formulas belong in scientific notes or interactive “Science Core” panels;
* repeated explanation templates should be handled carefully to avoid a text dump.

---

## 20. Data Architecture

Data logic should live in:

```txt
src/astrophenomena/data/
```

Initial responsibilities:

* load local sample object data;
* define adapters for future catalogues;
* keep data access separate from calculations;
* avoid hardcoding scientific data inside UI pages.

Initial data strategy:

```txt
small curated local dataset first
external catalogues later
```

Possible early local dataset:

```txt
data/objects_basic.csv
```

Example fields:

```txt
name
object_type
ra_deg
dec_deg
magnitude
catalog_id
epoch
notes
```

Future data sources:

* SIMBAD;
* Gaia;
* Minor Planet Center;
* JPL Horizons;
* NASA APIs;
* IMO meteor shower data;
* public solar image datasets.

External APIs should not become core dependencies too early.

---

## 21. UI Architecture

The first UI may be Streamlit, but Streamlit should remain a presentation layer.

Recommended structure:

```txt
app/
└── streamlit/
    ├── Home.py
    ├── pages/
    │   ├── 01_Sky_Coordinates_Explorer.py
    │   ├── 02_Observation_Planner.py
    │   └── ...
    └── components/
```

UI responsibilities:

* collect user input;
* call stable scientific engines;
* display outputs;
* render visualizations;
* expose explanations progressively.

UI should not:

* define core scientific formulas;
* own coordinate transformations;
* duplicate visibility logic;
* hardcode object data beyond demo examples;
* import internal implementation helpers directly;
* bypass typed result objects.

Streamlit-specific rendering must stay in:

```txt
app/streamlit/
```

---

## 22. Progressive Disclosure UI Pattern

Every interactive scientific module should follow this layered structure:

```txt
Phenomenon Canvas
      ↓
Observable Metric
      ↓
Conceptual Grid
      ↓
Science Core
```

---

## 22.1 Phenomenon Canvas

Shows what is happening visually.

Example:

* object moving across local sky dome;
* Moon phase geometry;
* eclipse alignment;
* meteor radiant map.

---

## 22.2 Observable Metric

Shows the immediate measurable output.

Example:

```txt
Altitude: 42°
Azimuth: 031°
Visible: yes
Culmination: 23:12
```

---

## 22.3 Conceptual Grid

Reveals geometric reference structures.

Example:

* horizon;
* zenith;
* meridian;
* RA/Dec grid;
* Alt/Az grid;
* ecliptic;
* nodes.

---

## 22.4 Science Core

Shows the underlying scientific relation.

Example:

```txt
H = LST - RA
```

or:

```txt
RA/Dec + observer location + time → Alt/Az
```

The user should never be forced into formulas immediately.

The formula layer should be available, not dominant.

---

## 23. Prototype Architecture

Prototypes should be isolated and structured.

Example:

```txt
prototypes/
└── sky_coordinates_001/
    ├── README.md
    ├── prototype.py
    ├── requirements.txt
    ├── notes.md
    └── outputs/
```

Each prototype should include:

| File           | Role                               |
| -------------- | ---------------------------------- |
| `README.md`    | What the prototype tests           |
| `prototype.py` | Minimal runnable code              |
| `notes.md`     | Findings, assumptions, limitations |
| `outputs/`     | Generated figures or screenshots   |

A prototype should answer:

* what is being tested?
* what scientific concept is used?
* what is out of scope?
* what would be needed to make it stable?
* should it be promoted, rewritten or discarded?

Prototype code is exempt from strict stable-code architecture rules, but it should still document scientific assumptions.

---

## 24. Notebook Architecture

Notebooks should be used for exploration, not production.

Recommended structure:

```txt
notebooks/
├── coordinates/
├── visibility/
├── phenomena/
├── meteor_science/
├── solar_system/
├── stars/
└── galaxies/
```

Notebook use cases:

* learning;
* quick tests;
* formula exploration;
* data visualization;
* course-based experiments;
* validation against known examples.

Notebook rules:

* do not import notebooks into stable code;
* do not treat notebook logic as production;
* extract useful validated logic into `src/astrophenomena/` only after review.

---

## 25. Testing Strategy

Scientific software must be tested.

The first testing layer should include:

```txt
tests/
├── test_time/
├── test_coordinates/
├── test_observers/
├── test_objects/
├── test_visibility/
├── test_phenomena/
├── test_visualizations/
├── test_data/
└── conftest.py
```

---

## 25.1 Test Types

| Test type               | Purpose                                      |
| ----------------------- | -------------------------------------------- |
| Unit tests              | Check individual functions                   |
| Known-case tests        | Compare against trusted expected results     |
| Regression tests        | Prevent future changes from breaking results |
| Boundary tests          | Check edge cases                             |
| Scientific sanity tests | Catch physically impossible outputs          |

---

## 25.2 Early Test Examples

| Module         | Test                                                  |
| -------------- | ----------------------------------------------------- |
| Observer       | Latitude must be between -90° and +90°                |
| Observer       | Longitude must be between -180° and +180°             |
| Time           | Local time converts to UTC correctly                  |
| Coordinates    | Altitude remains between -90° and +90°                |
| Coordinates    | Azimuth remains within defined convention             |
| Visibility     | Object below horizon is not visible                   |
| Visibility     | Object above threshold is visible                     |
| Objects        | Fixed object returns coordinates through protocol     |
| Visualizations | Sky dome figure is returned without Streamlit imports |

---

## 25.3 Validation Against Trusted Tools

Early results should be checked against at least one trusted reference such as:

* Astropy examples;
* Stellarium;
* Skyfield;
* IMCCE / ephemeris references;
* JPL Horizons for Solar System objects later.

The validation reference must be noted in prototype or test documentation.

---

## 25.4 Test Folder Mirroring Rule

The `tests/` structure should mirror the stable package structure.

Recommended test structure:

```txt
tests/
├── test_time/
├── test_coordinates/
├── test_observers/
├── test_objects/
├── test_visibility/
├── test_phenomena/
├── test_visualizations/
├── test_data/
└── conftest.py
```

Rules:

* empty placeholder test folders are acceptable for reserved packages;
* `conftest.py` should contain shared fixtures such as:

  * a default observer, e.g. Meudon;
  * a default observation time;
  * a fixed test object;
* visualization tests should at minimum verify that figure objects are returned without errors;
* scientific engine tests should verify numerical sanity and known cases.

---

## 26. Dependency Strategy

Initial likely dependencies:

| Library    | Role                                   | Status                            |
| ---------- | -------------------------------------- | --------------------------------- |
| Astropy    | Coordinates, time, units               | Preferred first astronomy library |
| NumPy      | Numerical operations                   | Required                          |
| Pandas     | Tabular data                           | Useful                            |
| Matplotlib | Static plots                           | Useful                            |
| Plotly     | Interactive plots                      | Useful for early UI               |
| Streamlit  | Web application interface              | UI layer                          |
| Skyfield   | Ephemerides and Solar System positions | Possible later                    |
| pytest     | Testing                                | Required                          |

---

## 26.1 Astropy-First Decision

The first prototype should use Astropy for:

* time handling;
* coordinate frames;
* RA/Dec to Alt/Az;
* units.

Reason:

* reliable;
* widely used;
* scientifically appropriate;
* avoids fragile custom astronomy formulas too early.

This decision should be recorded in:

```txt
decisions/decision_log.md
```

or as a specific decision file:

```txt
decisions/0001-astropy-as-calculation-library.md
```

---

## 26.2 Minimal `pyproject.toml` Requirement

Because the project uses a `src/` layout, `pyproject.toml` must explicitly configure package discovery.

Minimum required configuration:

```toml
[build-system]
requires = ["setuptools>=61"]
build-backend = "setuptools.build_meta"

[project]
name = "astrophenomena"
version = "0.1.0"
requires-python = ">=3.10"

[tool.setuptools.packages.find]
where = ["src"]
```

Without this configuration, `import astrophenomena` may fail after installation.

The exact dependency list can evolve, but the `src/` package discovery rule must be present from the beginning.

---

## 27. Coding-Agent Rules

Any coding agent working on this project must follow these rules.

---

## 27.1 Before Coding

The agent must read:

```txt
STATE.md
docs/00_AI_Operating_System.md
docs/02_Master_Brief.md
docs/03_Scientific_Map.md
docs/04_Architecture_Document.md
```

For feature-specific work, the agent must also read the relevant Feature Brief.

---

## 27.2 During Coding

The agent must:

* stay within the target tier;
* use the requested target location;
* not promote prototypes to stable code without review;
* not invent new architecture;
* not create duplicate modules;
* not hide scientific assumptions;
* not mix Streamlit UI and scientific core logic;
* document limitations;
* add tests when working in stable code;
* use type annotations on all functions and class fields in `src/astrophenomena/`;
* do not use plain dictionaries for core scientific result objects;
* do not use `Any` unless explicitly justified;
* preserve public API boundaries defined in each subpackage `__init__.py`;
* do not import Streamlit inside `src/astrophenomena/`;
* keep Streamlit rendering inside `app/streamlit/`.

---

## 27.3 After Coding

The agent must report:

* files changed;
* scientific assumptions;
* tests added;
* how to run the result;
* limitations;
* whether the result is prototype, experimental or stable.

---

## 28. First Feature Brief Candidate

The first coding target should be a controlled prototype.

Suggested Feature Brief:

```txt
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
```

---

## 29. Immediate Architecture Decisions to Log

The following decisions should be recorded before implementation.

---

### Decision 1 — Astropy-First Calculation Library

Astropy is the preferred first calculation library for time, coordinates and units.

---

### Decision 2 — Stable Scientific Logic Belongs in `src/astrophenomena/`

Scientific calculation logic should not live inside Streamlit pages.

---

### Decision 3 — First Implementation Target Is Sky Coordinates Explorer

The first implementation layer targets Axe 1.

---

### Decision 4 — Prototype Before Stable

The first build should be a prototype under:

```txt
prototypes/sky_coordinates_001/
```

---

### Decision 5 — No Top-Level `explanations/` Package Yet

Explanations should initially be colocated with scientific modules or returned as metadata.

---

### Decision 6 — Dataclasses for Core Data Models

Core scientific data models in `src/astrophenomena/` should use Python dataclasses with type annotations.

Plain dictionaries should not be used for stable scientific result objects.

---

### Decision 7 — Celestial Object Protocol

All coordinate-dependent engines should consume a celestial object protocol exposing:

```txt
get_equatorial_position(time)
```

This allows fixed and dynamic celestial objects to share one interface.

---

### Decision 8 — UI-Agnostic Visualization Layer

Visualization functions in `src/astrophenomena/visualizations/` must not import or invoke Streamlit.

They return figure objects or structured data.

Rendering belongs to `app/streamlit/`.

---

### Decision 9 — Type Annotations Required in Stable Code

All stable code in `src/astrophenomena/` must use type annotations.

Prototypes and notebooks are exempt.

---

### Decision 10 — Reserved `phenomena/` Namespace

The `phenomena/` package is reserved for later Axe 3 and Axe 4 work.

It should not be populated before foundational engines are stable.

---

## 30. Immediate Next Steps

After this Architecture Document v0.2:

```txt
1. Confirm validation with Claude.
2. Confirm Gemini’s two UX architecture notes are resolved.
3. Log architecture decisions in decisions/decision_log.md.
4. Create Feature Brief 001.
5. Start Prototype 001.
```

The first build target should remain limited:

```txt
Object + time + observer location
      ↓
Altitude / azimuth
      ↓
Visibility status
      ↓
Simple explanation
      ↓
Basic visual
```

---

## 31. Closing Statement

The architecture of AstroPhenomena Explorer must let the project grow without losing scientific rigor.

The first priority is not to build every astronomy feature.

The first priority is to build a clean, trustworthy foundation:

```txt
time
coordinates
observer
object protocol
visibility
visual explanation
typed results
scientific traceability
```

Once these foundations are stable, the project can expand toward observation planning, phenomena prediction, simulations, real data analysis and future hardware-assisted observation.

This architecture should keep the project ambitious, but technically controlled.

Before any coding agent starts implementing Prototype 001, the project must have:

* validated architecture boundaries;
* typed dataclass-based core models;
* a celestial object coordinate protocol;
* a UI-agnostic visualization boundary;
* a Feature Brief following the Master Brief template;
* architecture decisions logged in `decisions/`.

Only then should implementation begin.
