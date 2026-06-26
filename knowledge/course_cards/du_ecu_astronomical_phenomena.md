# Course Card — Astronomical Phenomena, Eclipses and Occultations

## 1. Source Identity

| Field | Value |
|---|---|
| Course name | Astronomical Phenomena, Eclipses and Occultations |
| Source type | DU ECU lecture slides |
| Origin | DU Explorer et Comprendre l’Univers — Observatoire de Paris / PSL, J. Vaubaillon, inspired by J.-E. Arlot and P. Rocher |
| Language | French |
| Scientific domain | Astronomical phenomena, eclipses, occultations, transits, ephemerides, observational geometry |
| Priority for AstroPhenomena Explorer | Core foundation for phenomena prediction and scientific observation |
| Related project axes | Axe 2 — Observer le ciel; Axe 3 — Prédire les phénomènes; Axe 4 — Simuler les phénomènes; Axe 5 — Produire de la science; support for Axe 1 |
| Public sharing status | Summary only; raw PDF should not be committed to the public repository |

---

## 2. Course Summary

This course explains what an astronomical phenomenon is and how rare celestial configurations can be predicted, observed and scientifically exploited.

Its central question is:

**How can special geometrical configurations of celestial bodies produce observable events, and how can those events be predicted and used scientifically?**

The course defines an astronomical phenomenon as a particular configuration of the Solar System that can lead to an observation that is rare, spectacular and/or scientifically useful. Examples include eclipses, occultations, conjunctions, oppositions, elongations, transits, rises and sets. A key principle is that these phenomena are predicted using **ephemerides**, because they depend on the changing positions of Solar System bodies in time.

The course first clarifies a crucial distinction:

- an **eclipse** is a real shadow phenomenon, where a body passes into the shadow of another body and is deprived of its usual light source;
- an **occultation** is observer-dependent, where one body hides another body from a particular line of sight.

This distinction is central for AstroPhenomena Explorer. What is commonly called a “solar eclipse” is, strictly speaking, an occultation of the Sun by the Moon for an observer on Earth. A lunar eclipse is a true eclipse because the Moon enters Earth’s shadow.

The course then introduces the geometry of **shadow and penumbra**. A luminous source, an occulting body, a target body and an observer define regions of full shadow and partial shadow. This geometry explains why eclipses can be total, partial, annular or penumbral, and why visibility depends on location.

A major section focuses on solar and lunar eclipses. The course explains that eclipses do not happen at every new or full Moon because the Moon’s orbital plane is inclined by about 5° relative to the ecliptic. Eclipses occur only when the Sun, Earth and Moon are aligned close to the line of nodes. The precession of the lunar nodes also changes eclipse circumstances over time.

The course also explains why all eclipses are different. Apparent diameters of the Sun and Moon vary because Earth’s orbit and the Moon’s orbit are elliptical. This affects whether a solar event is total or annular, how long totality lasts, and how the shadow path moves across Earth.

The course then shows that predicting an eclipse visibility zone requires combining several motions and geometries:

- Earth’s revolution around the Sun;
- Moon’s revolution around Earth;
- Earth’s rotation;
- Earth’s spherical shape.

This connects directly to AstroPhenomena Explorer’s goal of moving from sky coordinates to phenomena prediction.

The course also emphasizes the scientific value of eclipses. Solar eclipses historically enabled observations of the solar corona and prominences, tests of general relativity, and searches for bodies near the Sun. Modern instruments such as coronographs, SOHO and Solar Orbiter extend this scientific tradition.

Lunar eclipses are introduced as true eclipses with three main types:

- penumbral lunar eclipses;
- partial lunar eclipses;
- total lunar eclipses.

The course also presents historical eclipse records, such as Babylonian eclipse observations, and explains that ancient eclipse data can reveal long-term changes in Earth’s rotation. This shows that astronomical phenomena are not only spectacular events; they are data sources for geophysics and celestial mechanics.

The second major part of the course covers **mutual phenomena** and **stellar occultations**. Mutual phenomena are eclipses and occultations involving planetary satellites. They can be observed by recording the light flux of a satellite as a function of time. Because many satellites have no atmosphere, the brightness drop can be sharp, making precise timing valuable.

The course highlights major scientific uses of mutual phenomena:

- demonstration that the speed of light is finite through Römer’s observations;
- determination of longitudes for navigation;
- constraints on satellite theories and planetary ephemerides;
- study of gravitational perturbations and internal structures;
- confirmation of orbital changes, such as DART’s impact on Dimorphos.

The course then expands to stellar occultations by satellites, trans-Neptunian objects, rings and asteroids. Stellar occultations are powerful because the disappearance and reappearance of a star can reveal:

- asteroid diameters and shapes;
- binary asteroids;
- rings around small bodies;
- atmospheres of planets or dwarf planets;
- stellar diameters through diffraction;
- pressure and density profiles of atmospheres.

The course also connects occultations to exoplanet transits. A transit is essentially a small occultation of a star by a planet. The shape and duration of the light curve reveal the planet’s size, orbital inclination and sometimes density when combined with radial velocity measurements.

For AstroPhenomena Explorer, this course is a direct foundation for the **Phenomena Detector** and for future scientific observation modules. It explains that predicting an event is not enough: the project must also determine whether it is visible from a given place, how it appears, what physical geometry causes it, what data should be collected, and what science can be extracted from the observation.

---

## 3. Key Scientific Concepts

| Concept | Short explanation | Importance for the project |
|---|---|---|
| Astronomical phenomenon | Special configuration of celestial bodies producing a rare, observable or scientifically useful event. | Direct foundation for the Phenomena Detector. |
| Ephemerides | Predicted positions and velocities of Solar System bodies over time. | Required for predicting eclipses, occultations, conjunctions and transits. |
| Eclipse | True shadow event where a body enters the shadow of another body. | Essential for lunar eclipses and shadow simulations. |
| Occultation | Observer-dependent hiding of one body by another along a line of sight. | Essential for solar “eclipses”, stellar occultations and transits. |
| Shadow / umbra | Region where direct light from a source is fully blocked. | Needed for eclipse classification and visualization. |
| Penumbra | Region where the light source is only partially blocked. | Needed for partial and penumbral eclipse modeling. |
| Transit | Passage of a smaller body in front of a luminous disk from the observer’s viewpoint. | Connects Mercury/Venus transits and exoplanet transits. |
| Conjunction | Configuration where two bodies appear close in the sky or aligned in longitude. | Useful for planetary configuration detection. |
| Opposition | Configuration where a body lies opposite the Sun in the sky, often favorable for observation. | Useful for observation planning and phenomena detection. |
| Elongation | Angular separation between a planet and the Sun as seen from Earth. | Important for Mercury/Venus visibility. |
| Inferior conjunction | Configuration where an inner planet lies between Earth and the Sun. | Necessary condition for Mercury and Venus transits. |
| Orbital node | Crossing point between an orbit and a reference plane. | Crucial for eclipses and transits. |
| Line of nodes | Intersection line between two orbital planes. | Explains why eclipses do not occur every lunar month. |
| Lunar orbital inclination | The Moon’s orbit is inclined relative to the ecliptic. | Explains eclipse seasons. |
| Node precession | Slow motion of the line of nodes. | Affects eclipse timing, duration and recurrence. |
| Apparent diameter | Angular size of a body as seen by the observer. | Determines total vs annular solar occultations. |
| Eclipse path | Ground track of the Moon’s shadow on Earth. | Key output for solar eclipse visibility maps. |
| Visibility map | Geographic map showing where an event can be observed. | Core for observation planning. |
| Eclipse magnitude | Measure related to how much of the solar diameter is covered. | Useful for classifying solar events. |
| Obscuration | Fraction of the solar disk area hidden during a solar occultation. | Useful for user-facing eclipse descriptions. |
| Solar corona | Outer solar atmosphere visible during total solar eclipses or through coronographs. | Scientific motivation for eclipse observations. |
| Lunar eclipse types | Penumbral, partial and total lunar eclipses. | Needed for event classification. |
| Mutual phenomena | Eclipses and occultations between satellites of planets. | Useful for timing-based science modules. |
| Light curve | Flux measured as a function of time during an event. | Central for occultations, transits and mutual phenomena. |
| Stellar occultation | A Solar System body temporarily hides a background star. | High-value scientific observation mode. |
| Occultation chord | Track across an occulting body sampled by one observer. | Used to reconstruct asteroid shapes. |
| Gaia astrometry | Precise star positions from Gaia improve occultation prediction. | Important for future occultation modules. |
| Atmospheric occultation | Occultation where gradual dimming probes an atmosphere. | Supports Pluto/Titan atmosphere examples. |
| Exoplanet transit | Planet passes in front of its star, causing a brightness dip. | Connects Solar System phenomena to exoplanet science. |
| Radial velocity | Spectroscopic method measuring stellar motion due to a planet. | Complements transit data to estimate planet mass and density. |

---

## 4. Important Formulas, Relations or Models

### 4.1 Phenomenon prediction model

```txt
Ephemerides + observer location + event geometry → observable astronomical phenomenon
```

**Meaning**

A phenomenon is predicted by combining body positions over time with the observer’s location and the geometrical condition for the event.

**Variables**

- Ephemerides: positions of the relevant bodies.
- Observer location: latitude, longitude, altitude.
- Time: event date and time.
- Geometry: alignment, shadow, occultation or angular separation condition.

**Use in AstroPhenomena Explorer**

This is the conceptual backbone of the Phenomena Detector. It supports:

- eclipse prediction;
- occultation prediction;
- conjunction/opposition detection;
- elongation calculation;
- local visibility checks.

**Scientific status**

Conceptually reliable. Precise implementation requires high-quality ephemerides, accurate time scales, Earth orientation and topocentric corrections.

---

### 4.2 Eclipse / occultation distinction

```txt
Eclipse: body enters another body’s shadow.
Occultation: body is hidden from a specific observer by another body.
```

**Meaning**

This is not a numerical formula but a classification model.

**Use in AstroPhenomena Explorer**

The project should use this distinction to explain:

- why a lunar eclipse is a true eclipse;
- why a “solar eclipse” is technically an occultation of the Sun by the Moon;
- why occultation visibility is strongly observer-dependent.

**Scientific status**

Conceptual definition. The project may still use common public vocabulary while adding a precise scientific note.

---

### 4.3 Solar transit condition

```txt
Inferior conjunction + near orbital node → possible transit
```

**Meaning**

Mercury or Venus transits require the planet to be between Earth and the Sun and close enough to the node of its orbit so that its apparent path crosses the solar disk.

**Variables**

- Inferior conjunction: inner planet aligned between Earth and Sun.
- Node proximity: planet close to the intersection of its orbital plane with the ecliptic.

**Use in AstroPhenomena Explorer**

Useful for:

- transit prediction;
- Mercury/Venus transit visualizer;
- explaining why transits are rare.

**Scientific status**

Simplified but accurate as a first condition. Precise prediction requires ephemerides and apparent angular geometry.

---

### 4.4 Eclipse season condition

```txt
New Moon or Full Moon + Sun near lunar line of nodes → possible eclipse
```

**Meaning**

Eclipses do not occur every new/full Moon because the Moon’s orbit is inclined relative to the ecliptic.

**Interpretation**

- New Moon near node: solar occultation / solar eclipse.
- Full Moon near node: lunar eclipse.
- Sun not near the line of nodes: no eclipse.

**Use in AstroPhenomena Explorer**

Useful for:

- eclipse season visualizer;
- Moon orbit inclination module;
- explaining eclipse rarity.

**Scientific status**

Simplified but foundational. Precise prediction needs angular thresholds and ephemerides.

---

### 4.5 Apparent diameter comparison

```txt
If apparent Moon diameter > apparent Sun diameter → total solar occultation possible.
If apparent Moon diameter < apparent Sun diameter → annular solar occultation possible.
```

**Meaning**

The type of solar event depends on the relative apparent diameters of the Sun and Moon.

**Variables**

- Apparent lunar diameter.
- Apparent solar diameter.
- Earth-Moon distance.
- Earth-Sun distance.

**Use in AstroPhenomena Explorer**

Useful for:

- total vs annular eclipse classification;
- apparent diameter simulator;
- explaining why each eclipse is different.

**Scientific status**

Conceptually reliable. Precise classification also depends on observer location and topocentric geometry.

---

### 4.6 Eclipse visibility model

```txt
Solar eclipse visibility depends on:
Earth revolution + Moon revolution + Earth rotation + spherical Earth geometry
```

**Meaning**

The path of a solar eclipse is not fixed only by alignment. It depends on the motion of Earth and Moon and the rotating spherical Earth.

**Use in AstroPhenomena Explorer**

Useful for:

- eclipse maps;
- path of totality animation;
- local circumstances calculation;
- observation planner.

**Scientific status**

Conceptual model. Real implementation requires precise shadow cone intersection with Earth ellipsoid.

---

### 4.7 Shadow cone speed

```txt
Typical lunar shadow speed on Earth ≈ 1 km/s
```

**Meaning**

The Moon’s shadow sweeps rapidly across Earth. Earth’s rotation partially compensates the motion depending on latitude.

**Use in AstroPhenomena Explorer**

Useful for:

- eclipse path animations;
- explaining why totality is brief;
- comparing aircraft eclipse chasing, such as the 1973 Concorde observation.

**Scientific status**

Approximate pedagogical value. Actual shadow speed varies with geometry and location.

---

### 4.8 Light curve model for occultations and transits

```txt
Flux(t) decreases when an object blocks part or all of the light source.
```

**Meaning**

A time series of brightness can reveal the geometry of an occultation or transit.

**Variables**

- \(F(t)\): flux as a function of time.
- Event duration.
- Depth of flux drop.
- Shape of ingress and egress.
- Observer location.

**Use in AstroPhenomena Explorer**

Useful for:

- mutual phenomena lab;
- stellar occultation lab;
- exoplanet transit simulator;
- DART/Dimorphos orbital change example.

**Scientific status**

Conceptually reliable. Real light-curve analysis requires noise modeling, calibration, exposure timing and sometimes diffraction or atmospheric modeling.

---

### 4.9 Exoplanet transit inference model

```txt
Transit period → orbital period and semi-major axis
Transit depth → planet/star size ratio
Transit duration and shape → inclination and geometry
Radial velocity → planet mass
Mass + radius → density
```

**Meaning**

A transit light curve, combined with stellar properties and radial velocities, can determine physical properties of an exoplanet.

**Use in AstroPhenomena Explorer**

Useful for:

- exoplanet transit demonstration;
- linking occultation geometry to astrophysics;
- showing how light curves produce physical measurements.

**Scientific status**

Simplified but scientifically meaningful. Real exoplanet modeling includes limb darkening, stellar activity, eccentricity, noise and degeneracies.

---

## 5. Relevance for AstroPhenomena Explorer

### Axe 1 — Comprendre le ciel

This course supports Axe 1 by showing that objects are not only located in the sky, but can also align, hide each other or enter shadows.

Relevant concepts:

- conjunction;
- opposition;
- elongation;
- apparent diameter;
- local visibility;
- observer dependence;
- ephemerides.

Possible uses:

- explain why some sky configurations are special;
- add event annotations to sky maps;
- show angular separations between objects;
- distinguish simple visibility from phenomenon visibility.

---

### Axe 2 — Observer le ciel

This course is highly relevant to observation planning.

Relevant concepts:

- visibility maps;
- local circumstances;
- Moon visibility for lunar eclipses;
- solar eclipse path;
- event timing;
- flux recording;
- occultation observation campaigns;
- observer location dependence.

Possible modules:

- Eclipse Observation Planner;
- Occultation Campaign Planner;
- Transit Observation Guide;
- Event Visibility Checker;
- Local Circumstances Generator.

The key operational idea is that an event may exist globally but not be observable from the user’s location.

---

### Axe 3 — Prédire les phénomènes

This is the most directly relevant course for Axe 3.

Relevant concepts:

- astronomical phenomena;
- ephemerides;
- conjunctions;
- oppositions;
- elongations;
- eclipses;
- occultations;
- transits;
- mutual phenomena;
- stellar occultations;
- event geometry.

Possible modules:

- Phenomena Detector;
- Eclipse Predictor;
- Transit Detector;
- Occultation Predictor;
- Planetary Configuration Explorer;
- Ephemeris-Based Event Search.

This course defines what the Phenomena Detector should actually detect.

---

### Axe 4 — Simuler les phénomènes

This course is a core source for visual simulations.

Relevant concepts:

- umbra and penumbra;
- shadow cones;
- apparent diameters;
- Moon orbital inclination;
- line of nodes;
- eclipse seasons;
- visibility path;
- light curves;
- occultation chords.

Possible simulations:

- Shadow and Penumbra Simulator;
- Solar Eclipse Geometry Simulator;
- Lunar Eclipse Simulator;
- Node-Line Eclipse Season Simulator;
- Transit of Mercury/Venus Simulator;
- Stellar Occultation Chord Simulator;
- Exoplanet Transit Light Curve Simulator.

---

### Axe 5 — Produire de la science

This course is extremely relevant for science-oriented modules.

Relevant concepts:

- mutual phenomena timing;
- light curves;
- stellar occultations;
- occultation chords;
- asteroid diameter measurements;
- atmosphere probing by occultation;
- ring detection;
- DART orbital change confirmation;
- exoplanet transits.

Possible science workflows:

- simulate and fit an occultation light curve;
- estimate asteroid size from occultation chords;
- infer an atmosphere from gradual flux decrease;
- compare predicted and observed occultation times;
- use transit depth to estimate exoplanet radius;
- use mutual phenomena to constrain satellite ephemerides.

This source is one of the strongest links between AstroPhenomena Explorer and real observational science.

---

## 6. Possible Software Modules

| Possible module | Purpose | Related concepts | Priority |
|---|---|---|---|
| Phenomena Detector | Detect special astronomical configurations from ephemerides. | Conjunction, opposition, elongation, eclipse, occultation, transit | Very high |
| Eclipse Geometry Simulator | Explain solar and lunar eclipse geometry. | Umbra, penumbra, shadow cones, apparent diameters | Very high |
| Eclipse Visibility Checker | Determine whether an eclipse is visible from a location. | Visibility maps, local circumstances, Earth rotation | Very high |
| Solar Eclipse Path Viewer | Display path of partiality, annularity or totality. | Shadow cone, Earth rotation, spherical Earth | High |
| Lunar Eclipse Viewer | Show lunar passage through penumbra and umbra. | Lunar eclipse types, Moon visibility | High |
| Eclipse Season Explorer | Explain why eclipses occur near nodes. | Lunar inclination, line of nodes, node precession | Very high |
| Transit of Mercury/Venus Simulator | Show inferior conjunction plus node condition. | Transit, apparent solar disk, orbital nodes | High |
| Planetary Configuration Explorer | Visualize conjunction, opposition and elongation. | Solar System geometry | High |
| Mutual Phenomena Light Curve Lab | Simulate flux drops between planetary satellites. | Mutual eclipses, occultations, timing | Medium to high |
| Stellar Occultation Planner | Predict and explain stellar occultations by small bodies. | Gaia, occultation path, observer location | High |
| Occultation Chord Reconstruction Lab | Reconstruct object shape from multiple observer chords. | Asteroid size, shape, timing | High |
| Atmosphere by Occultation Lab | Show gradual dimming caused by an atmosphere. | Pluto, Titan, pressure profile | Medium |
| Rings by Occultation Lab | Show secondary brightness dips caused by rings. | Ring detection, occultation light curves | Medium |
| DART Occultation Case Study | Explain how occultations confirmed orbital change. | Didymos, Dimorphos, timing | Medium |
| Exoplanet Transit Lab | Connect occultations to exoplanet detection. | Transit depth, duration, inclination, density | High |

---

## 7. Possible Visualizations and Interactions

| Visual / interaction | What it explains | Suggested form | Priority |
|---|---|---|---|
| Astronomical phenomenon configuration grid | Different event types: conjunction, opposition, elongation, transit. | Diagram set | High |
| Eclipse vs occultation comparison | Difference between shadow event and observer-dependent hiding. | Side-by-side diagram | Very high |
| Umbra and penumbra diagram | Full and partial shadow formation. | Interactive diagram | Very high |
| Solar eclipse geometry | Moon shadow intersecting Earth. | 3D animation | Very high |
| Lunar eclipse geometry | Moon crossing Earth’s penumbra and umbra. | Animation | High |
| Apparent diameter comparison | Total vs annular solar events. | Slider | Very high |
| Moon orbit inclination | Why eclipses do not happen every month. | 3D node-line animation | Very high |
| Eclipse season timeline | Sun crossing the lunar line of nodes. | Timeline + orbit diagram | High |
| Solar eclipse path map | Visibility zone and path of totality. | Map | High |
| Shadow speed animation | Motion of the shadow over rotating Earth. | Map animation | Medium |
| Concorde 1973 eclipse chase | Moving observer extends totality duration. | Story map | Medium |
| Lunar eclipse visibility map | Where the Moon is visible during an eclipse. | World map | Medium |
| Historical eclipse reconstruction | Babylonian eclipse and Earth rotation implications. | Timeline / case study | Medium |
| Mutual phenomena light curve | Flux drop during satellite occultation/eclipse. | Data plot | High |
| Stellar occultation chord diagram | Multiple observers reconstruct object shape. | Interactive map + object profile | Very high |
| Occultation atmosphere curve | Gradual dimming through an atmosphere. | Light curve simulation | High |
| Ring occultation light curve | Secondary dips from rings. | Light curve plot | Medium |
| Exoplanet transit light curve | Planet size/inclination from flux dip. | Interactive plot | High |

---

## 8. User Questions Enabled by This Course

| User question | Scientific concepts behind it | Possible module |
|---|---|---|
| What is an astronomical phenomenon? | Special Solar System configuration, ephemerides | Phenomena Detector |
| What is the difference between an eclipse and an occultation? | Shadow vs observer-dependent hiding | Eclipse vs Occultation Explainer |
| Why is a solar eclipse technically an occultation? | Moon hides Sun from an observer | Eclipse Geometry Simulator |
| Why do lunar eclipses happen only at full Moon? | Sun-Earth-Moon alignment, Earth shadow | Lunar Eclipse Viewer |
| Why is there not an eclipse every new Moon? | Lunar inclination, line of nodes | Eclipse Season Explorer |
| Why are some solar eclipses total and others annular? | Apparent diameters, Earth-Moon distance | Apparent Diameter Simulator |
| Where will an eclipse be visible? | Shadow path, Earth rotation, observer location | Eclipse Visibility Checker |
| Why does totality last only a few minutes? | Shadow cone speed, Earth rotation | Solar Eclipse Path Viewer |
| Why was the 1973 eclipse observed from Concorde? | Moving observer, shadow tracking | Concorde Eclipse Case Study |
| Why does the Moon turn red during a lunar eclipse? | Atmospheric refraction, wavelength dependence | Lunar Eclipse Viewer |
| How can ancient eclipses tell us about Earth’s rotation? | Historical timing, tidal slowing | Historical Eclipse Reconstruction |
| What are mutual phenomena? | Satellite eclipses and occultations | Mutual Phenomena Lab |
| How did Römer show that light has finite speed? | Timing of Jupiter satellite phenomena | Mutual Phenomena Case Study |
| How can an occultation measure an asteroid’s size? | Stellar occultation chords | Occultation Chord Lab |
| How can occultations reveal rings? | Secondary flux drops | Rings by Occultation Lab |
| How can an occultation reveal an atmosphere? | Gradual dimming, pressure profile | Atmosphere Occultation Lab |
| How did DART’s effect get confirmed? | Occultation timing, orbital period change | DART Case Study |
| How are exoplanets detected by transits? | Light curve depth, duration, period | Exoplanet Transit Lab |
| What can a transit light curve tell us? | Planet radius, inclination, orbital period | Exoplanet Transit Lab |

---

## 9. Pedagogical Risks and Misconceptions

| Risk / misconception | Why it is problematic | How to avoid it |
|---|---|---|
| Using “eclipse” and “occultation” interchangeably | The physical geometry is different. | Explain common vocabulary vs strict scientific meaning. |
| Thinking solar eclipses are true eclipses of the Sun | The Sun is not entering a shadow; it is hidden from a local observer. | Label solar events as “occultation of the Sun by the Moon” in precision notes. |
| Thinking eclipses should happen every month | The Moon’s orbit is inclined relative to the ecliptic. | Use node-line and inclination visualizations. |
| Forgetting observer dependence | Occultations and solar eclipse visibility depend strongly on location. | Always include observer location in event outputs. |
| Treating global event existence as local visibility | An event may occur but not be visible from the user’s site. | Separate “event exists” from “event visible here.” |
| Confusing magnitude and obscuration in solar eclipses | Magnitude is diameter-related; obscuration is area-related. | Explain both with diagrams. |
| Assuming all eclipse predictions are simple alignments | Visibility zones require Earth rotation, Moon motion and spherical geometry. | Use layered prediction model diagrams. |
| Thinking all shadows are sharp | Penumbra and atmospheric effects can create gradual transitions. | Show umbra vs penumbra and light curves. |
| Thinking lunar eclipse color is intrinsic to the Moon | Red color comes from Earth’s atmosphere filtering sunlight. | Add atmospheric refraction explanation. |
| Ignoring apparent diameter variation | Total vs annular depends on changing Earth-Moon and Earth-Sun distances. | Include apparent diameter sliders. |
| Thinking occultations only confirm disappearance | Timing and light-curve shape produce scientific measurements. | Show chord reconstruction and flux curves. |
| Assuming amateurs cannot contribute | Many occultation and mutual phenomena observations are accessible. | Include observation campaign examples. |
| Treating exoplanet transits as unrelated | They are conceptually occultations producing light curves. | Connect Solar System occultations to exoplanet detection. |
| Ignoring Gaia’s role | Precise star positions greatly improve occultation predictions. | Add Gaia traceability in occultation modules. |
| Presenting predictions without uncertainty | Occultation paths can shift if object/star positions are uncertain. | Add uncertainty bands to visibility maps. |

---

## 10. Scientific Traceability Notes

This source should be treated as a core reference for AstroPhenomena Explorer’s phenomena prediction and event-observation logic.

### Reliable foundations from this source

The following concepts can be treated as reliable foundations:

- astronomical phenomena as special configurations;
- eclipse vs occultation distinction;
- umbra and penumbra geometry;
- apparent diameter variation;
- lunar inclination and line of nodes;
- eclipse seasons;
- observer-dependent visibility;
- eclipse maps and local circumstances;
- scientific use of eclipses;
- mutual phenomena as flux-vs-time events;
- stellar occultations as scientific probes;
- exoplanet transits as occultation-like light curves.

### Concepts that need additional references before implementation

Before precise implementation, the project should validate:

- high-precision ephemerides;
- solar and lunar eclipse algorithms;
- Earth orientation parameters;
- topocentric corrections;
- Earth ellipsoid and terrain effects for eclipse paths;
- Gaia-based occultation prediction methods;
- timing standards for occultation observations;
- light-curve modeling for occultations and exoplanet transits;
- current event catalogs and prediction services.

### Concepts simplified for pedagogy

The following are simplified in the course:

- eclipse geometry diagrams;
- shadow cone speed;
- apparent diameter comparison;
- event visibility maps;
- transit conditions;
- occultation light curves;
- exoplanet inference from transits.

These are excellent for educational modules but should not be confused with production-level prediction algorithms.

### Formulas and models requiring validation before implementation

The event condition models are conceptually correct but simplified:

```txt
New/Full Moon + line of nodes → eclipse possibility
Inferior conjunction + node proximity → transit possibility
```

Precise prediction requires angular thresholds, ephemerides and topocentric geometry.

The exoplanet transit inference model should be treated as introductory. Real transit fitting requires limb darkening, stellar parameters, noise treatment and degeneracy handling.

### Future tests and calculations

Useful future validation tests:

- compare predicted eclipse dates with IMCCE/NASA data;
- verify local visibility of known lunar and solar eclipses;
- reproduce the geometry of a total vs annular solar event;
- simulate the Moon’s inclined orbit and show why monthly eclipses do not occur;
- generate simple light curves for total, partial and grazing occultations;
- reconstruct a simple asteroid shape from synthetic occultation chords;
- compare a basic exoplanet transit depth calculation with known examples;
- use Gaia star positions in a future occultation prediction workflow.

---

## 11. Links to Future Knowledge Files

```txt
knowledge/concepts/astronomical_phenomenon.md
knowledge/concepts/ephemerides.md
knowledge/concepts/eclipse.md
knowledge/concepts/occultation.md
knowledge/concepts/umbra_penumbra.md
knowledge/concepts/solar_eclipse.md
knowledge/concepts/lunar_eclipse.md
knowledge/concepts/eclipse_season.md
knowledge/concepts/line_of_nodes.md
knowledge/concepts/apparent_diameter.md
knowledge/concepts/solar_transit.md
knowledge/concepts/conjunction.md
knowledge/concepts/opposition.md
knowledge/concepts/elongation.md
knowledge/concepts/eclipse_visibility_map.md
knowledge/concepts/local_circumstances.md
knowledge/concepts/mutual_phenomena.md
knowledge/concepts/light_curve.md
knowledge/concepts/stellar_occultation.md
knowledge/concepts/occultation_chords.md
knowledge/concepts/atmospheric_occultation.md
knowledge/concepts/ring_occultation.md
knowledge/concepts/exoplanet_transit.md
knowledge/concepts/transit_depth.md
knowledge/concepts/radial_velocity.md
```

---

## 12. Notes for AI Tools

This course is mainly useful for designing AstroPhenomena Explorer’s **Phenomena Detector** and event-science modules.

Future AI assistants should remember that this course defines phenomena as geometric configurations that become observable only under the right conditions. Prediction must therefore combine ephemerides, geometry, observer location and visibility.

An AI should not assume that an event visible somewhere is visible for the user. It must distinguish:

- phenomenon exists globally;
- phenomenon is visible from a given location;
- phenomenon is scientifically observable with a given instrument;
- phenomenon produces usable data.

An AI should also preserve the conceptual distinction between eclipse and occultation. Public-facing language can use common terms like “solar eclipse,” but scientific explanations should clarify that this is an occultation of the Sun by the Moon.

This source is most connected to:

- Axe 3 — Prédire les phénomènes;
- Axe 4 — Simuler les phénomènes;
- Axe 5 — Produire de la science.

It also supports Axe 2 because event prediction is only useful if local observability and observation strategy are considered.

**AI takeaway:** This course is the core reference for turning AstroPhenomena Explorer from a sky-position tool into a true astronomical event platform. It teaches that eclipses, occultations, transits and mutual phenomena are not just beautiful alignments: they are predictable geometrical configurations that can produce scientifically valuable data.
