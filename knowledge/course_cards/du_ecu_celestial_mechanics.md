# Course Card — Celestial Mechanics

## 1. Source Identity

| Field | Value |
|---|---|
| Course name | Celestial Mechanics |
| Source type | DU ECU lecture slides |
| Origin | DU Explorer et Comprendre l’Univers — Observatoire de Paris / PSL, J. Vaubaillon, inspired by J.-E. Arlot |
| Language | French |
| Scientific domain | Celestial mechanics, orbital dynamics, astrodynamics, solar system dynamics |
| Priority for AstroPhenomena Explorer | Core foundation for prediction and simulation |
| Related project axes | Axe 3 — Prédire les phénomènes; Axe 4 — Simuler les phénomènes; Axe 5 — Produire de la science; secondary support for Axe 1 and Axe 2 |
| Public sharing status | Summary only; raw PDF should not be committed to the public repository |

---

## 2. Course Summary

This course introduces the physical and mathematical foundations needed to understand how celestial bodies move.

Its central question is:

**How can we describe, understand, predict and exploit the motion of bodies under gravity?**

The course begins with the idea that an orbit is not an absence of falling, but a continuous fall around a central body. The Moon “falls” toward Earth while also moving tangentially fast enough to keep missing Earth. This connects Galileo’s inertia with Newtonian gravitation and explains why orbital velocity is central to spaceflight.

The first foundation is **Keplerian motion**. In the ideal two-body problem, planets, moons, asteroids or satellites follow conic-section orbits described by a small set of orbital elements. Kepler’s three laws explain that orbits are ellipses with the central body at one focus, that equal areas are swept in equal times, and that the relation between orbital size and orbital period follows:

\[
\frac{a^3}{P^2} = \text{constant}
\]

The course also extends this relation to satellites by showing that the mass of the central body matters: for the same semi-major axis, a satellite orbiting Jupiter has a much shorter period than one orbiting Earth.

The course then explains how to describe an orbit using **orbital elements**:

- semi-major axis \(a\);
- eccentricity \(e\);
- inclination \(i\);
- longitude of the ascending node \(\Omega\);
- argument of periapsis \(\omega\);
- time of periapsis passage \(t_p\).

These elements are essential for AstroPhenomena Explorer because they are the natural language of ephemerides, asteroid orbits, comet paths, planetary configurations, satellite orbits and mission trajectories.

The course then moves beyond the ideal two-body case. In the real Solar System, bodies perturb each other. Jupiter strongly affects the orbits of asteroids and comets. Perturbations explain the discovery of Neptune, variations in Earth’s orbital eccentricity, secular evolution of orbits, asteroid families and the long-term instability of many small bodies.

A major part of the course is devoted to **resonances**. A resonance occurs when orbital periods, spin periods or precession rates become commensurable. The course introduces:

- mean-motion resonances;
- spin-orbit resonances;
- secular resonances;
- Kozai resonance;
- Lagrange points;
- Hilda asteroids;
- Trojan asteroids.

These concepts are central for understanding why the Solar System has structure: gaps, clusters, families, stable regions and unstable zones.

The course also discusses **non-gravitational forces**, such as cometary outgassing, solar radiation pressure, Poynting–Robertson drag and the Yarkovsky effect. These are especially important for small bodies, comets, dust and long-term asteroid orbit prediction.

Another key theme is **chaos**. Some systems are extremely sensitive to initial conditions. Even if the equations are deterministic, long-term prediction becomes impossible after a certain time. This is important for AstroPhenomena Explorer because it prevents the project from presenting all predictions as infinitely reliable.

The course then introduces **near-Earth objects**: NEOs, NEAs and PHAs. It explains that impact prediction depends on precise observations, dynamic models, numerical propagation, comparison between observations and calculations, and uncertainty analysis. This strongly supports future modules on asteroid monitoring, impact risk, ephemerides and scientific data use.

The astrodynamics section connects celestial mechanics to space missions. It explains the equivalence between a state vector \((t, X, V)\) and orbital elements, how changing velocity changes the orbit, how transfers work, why launch windows exist, how Hohmann transfers operate, how gravitational assists change spacecraft speed and direction, and why atmospheric braking matters.

Finally, the course covers artificial satellites and debris: launch, orbit types, Starlink, space debris, reentry prediction, Kessler syndrome, controlled reentry and the growing importance of orbital sustainability.

For AstroPhenomena Explorer, this course is a core source because it provides the dynamics behind prediction. The previous courses explain how to locate objects and measure distances. This course explains **why objects move, how their motion is parameterized, how future positions are predicted, and where predictions become uncertain**.

---

## 3. Key Scientific Concepts

| Concept | Short explanation | Importance for the project |
|---|---|---|
| Gravity | Attractive interaction governing planetary, satellite, asteroid and comet motion. | Physical basis of all orbit prediction modules. |
| Orbital motion | Continuous falling around a central body with sufficient tangential velocity. | Helps explain satellites, Moon motion and artificial orbits. |
| Orbital velocity | Speed needed to remain in orbit or escape. | Useful for astrodynamics and satellite modules. |
| Keplerian motion | Ideal two-body orbital motion. | First model for orbit simulation. |
| Kepler’s laws | Three laws describing ellipses, area law and period-size relation. | Core for orbit visualization and prediction. |
| Semi-major axis \(a\) | Size / energy scale of an orbit. | Essential orbital element. |
| Eccentricity \(e\) | Shape of the orbit: circle, ellipse, parabola, hyperbola. | Useful for classifying orbit types. |
| Inclination \(i\) | Tilt of the orbital plane relative to a reference plane. | Needed for 3D orbit geometry, nodes and transits. |
| Periapsis | Closest point to the central body. | Important for comets, asteroids, transfers and tides. |
| Apoapsis | Farthest point from the central body. | Important for elliptical orbit visualization. |
| Ascending node | Point where an orbit crosses the reference plane upward. | Critical for eclipses, transits, close encounters and inclination changes. |
| Descending node | Point where an orbit crosses the reference plane downward. | Same as above. |
| Longitude of ascending node \(\Omega\) | Orientation of the line of nodes in the reference plane. | Required for full 3D orbital orientation. |
| Argument of periapsis \(\omega\) | Orientation of periapsis within the orbital plane. | Required for ephemerides and orbit reconstruction. |
| Time of periapsis \(t_p\) | Date when the object passes closest to the central body. | Needed for time-dependent orbit propagation. |
| Perturbation | Deviation from ideal Keplerian motion due to other forces or bodies. | Prevents oversimplified prediction. |
| Three-body problem | Motion involving more than two interacting bodies. | Explains complexity, chaos and resonances. |
| Mean-motion resonance | Orbital periods in rational ratios. | Explains asteroid gaps, Hilda family, satellite systems. |
| Spin-orbit resonance | Rotation and revolution periods locked in a ratio. | Explains Moon’s same face and Mercury’s 3:2 resonance. |
| Libration | Apparent oscillation around a locked orientation. | Useful for Moon visualization. |
| Secular resonance | Long-term resonance involving precession rates. | Important for asteroid dynamics and long-term evolution. |
| Kozai resonance | Coupled exchange between eccentricity and inclination in inclined three-body systems. | Advanced dynamical concept. |
| Lagrange points | Regions where gravitational and inertial effects balance in a rotating frame. | Important for JWST, Gaia, SOHO, Trojan asteroids and mission design. |
| Hill sphere | Region where a body’s gravity dominates over the central body’s attraction. | Useful for moons, satellites and capture. |
| Roche limit | Distance below which tidal forces can disrupt a body. | Supports ring and tidal disruption simulations. |
| Tidal effects | Differential gravity causing deformation, orbital evolution and heating. | Important for Earth–Moon evolution and Io volcanism. |
| Non-gravitational forces | Radiation pressure, Yarkovsky effect, outgassing, drag. | Important for comets, dust, debris and asteroid prediction. |
| Chaos | Extreme sensitivity to initial conditions. | Important for honest prediction limits. |
| Near-Earth object | Asteroid or comet approaching Earth’s orbital neighborhood. | Core for future asteroid-monitoring modules. |
| MOID | Minimum Orbital Intersection Distance. | Used in impact-risk evaluation. |
| PHA | Potentially Hazardous Asteroid. | Supports risk classification tools. |
| Ephemeris | Predicted position and velocity of a body over time. | Central for prediction modules. |
| Orbit determination | Process of deriving an orbit from observations and a dynamical model. | Important for science and NEO tracking. |
| State vector | Position and velocity at a given time. | Bridge between physics simulation and orbital elements. |
| Hohmann transfer | Efficient transfer between two circular orbits. | Useful for astrodynamics education. |
| Launch window | Time when celestial geometry allows a mission trajectory. | Important for mission-planning explanations. |
| Gravity assist | Use of a planet’s gravity and motion to change spacecraft trajectory. | Supports mission visualization. |
| Atmospheric braking | Use of atmospheric drag to slow a spacecraft or satellite. | Important for reentry and orbital decay. |
| Space debris | Artificial objects in orbit that no longer serve a function. | Supports orbital sustainability modules. |
| Kessler syndrome | Collision cascade scenario increasing debris density. | Important for space environment awareness. |

---

## 4. Important Formulas, Relations or Models

### 4.1 Kepler’s first law

\[
\text{Planetary orbits are ellipses with the Sun at one focus.}
\]

**Meaning**

In the ideal two-body case, bound orbits are ellipses, not perfect circles.

**Variables**

No explicit variables are required, but the ellipse is described by:

- semi-major axis \(a\);
- eccentricity \(e\);
- focus position.

**Use in AstroPhenomena Explorer**

- orbit visualization;
- planet/comet trajectory display;
- comparison between circular and elliptical motion;
- explanation of varying orbital distance.

**Scientific status**

Exact in the ideal two-body Keplerian model. Real orbits are perturbed.

---

### 4.2 Kepler’s second law — area law

\[
\frac{dA}{dt} = \text{constant}
\]

**Meaning**

A body sweeps equal areas in equal times. It moves faster near periapsis and slower near apoapsis.

**Variables**

- \(A\): area swept by the radius vector;
- \(t\): time.

**Use in AstroPhenomena Explorer**

- orbit animation with non-uniform velocity;
- explanation of why planets accelerate and decelerate;
- seasonal duration and comet-speed intuition.

**Scientific status**

Exact in the ideal two-body model. Perturbations slightly modify real motion.

---

### 4.3 Kepler’s third law

\[
\frac{a^3}{P^2} = \text{constant}
\]

For a body orbiting a central mass \(M\):

\[
\frac{a^3}{P^2} = \frac{GM}{4\pi^2}
\]

**Meaning**

Orbital size and orbital period are linked. Around a more massive central body, the same orbital radius corresponds to a shorter period.

**Variables**

- \(a\): semi-major axis;
- \(P\): orbital period;
- \(G\): gravitational constant;
- \(M\): mass of the central body.

**Use in AstroPhenomena Explorer**

- orbital period calculator;
- satellite comparison;
- solar system scale visualization;
- relation between central mass and orbital speed.

**Scientific status**

Valid for two-body Keplerian motion. Real ephemerides require perturbations.

---

### 4.4 Eccentricity relation

\[
e^2 = 1 - \left(\frac{b}{a}\right)^2
\]

**Meaning**

Eccentricity describes how stretched an ellipse is.

**Variables**

- \(e\): eccentricity;
- \(a\): semi-major axis;
- \(b\): semi-minor axis.

**Interpretation**

- \(e = 0\): circle;
- \(0 < e < 1\): ellipse;
- \(e = 1\): parabola;
- \(e > 1\): hyperbola.

**Use in AstroPhenomena Explorer**

- orbit-shape slider;
- classification of planets, comets and escape trajectories;
- diagram of orbit families.

**Scientific status**

Exact geometric relation for conic sections.

---

### 4.5 Periapsis and apoapsis distances

\[
q = a(1-e)
\]

\[
Q = a(1+e)
\]

**Meaning**

These formulas give the closest and farthest distances from the central body for an elliptical orbit.

**Variables**

- \(q\): periapsis distance;
- \(Q\): apoapsis distance;
- \(a\): semi-major axis;
- \(e\): eccentricity.

**Use in AstroPhenomena Explorer**

- comet orbit visualization;
- asteroid close-approach classification;
- planetary distance variation;
- transfer orbit explanation.

**Scientific status**

Exact for Keplerian ellipses.

---

### 4.6 Mean-motion resonance condition

\[
\frac{P_A}{P_B} = \frac{m}{n}
\]

**Meaning**

Two bodies are in mean-motion resonance when their orbital periods form a rational ratio.

**Variables**

- \(P_A\), \(P_B\): orbital periods;
- \(m\), \(n\): integers.

**Use in AstroPhenomena Explorer**

- resonance simulator;
- asteroid belt structure;
- Hilda asteroids;
- satellite resonance systems.

**Scientific status**

Conceptually reliable. Actual resonance dynamics require more detailed gravitational modeling.

---

### 4.7 Spin-orbit resonance

\[
n_a : n_b
\]

**Meaning**

A body’s rotation period and revolution period are locked in a ratio.

Examples:

- Moon: \(1:1\), same face toward Earth;
- Mercury: \(3:2\), three rotations for two revolutions.

**Use in AstroPhenomena Explorer**

- Moon same-face simulator;
- Mercury rotation animation;
- tidal locking explanation.

**Scientific status**

Standard dynamical concept. Real librations and tidal dissipation add complexity.

---

### 4.8 Kozai resonance relation

\[
\sqrt{1-e^2}\cos(i) = \text{constant}
\]

**Meaning**

In some inclined three-body configurations, eccentricity and inclination exchange with each other.

**Variables**

- \(e\): eccentricity;
- \(i\): inclination.

**Use in AstroPhenomena Explorer**

- advanced orbit dynamics visualization;
- asteroid/comet long-term evolution;
- exoplanet dynamics extension.

**Scientific status**

Advanced secular approximation. Should be treated as an advanced concept, not a beginner formula.

---

### 4.9 State vector and orbital elements equivalence

\[
(t, X, V) \Longleftrightarrow (a, e, i, \Omega, \omega, t_p)
\]

**Meaning**

At a given date, a position and velocity vector determine the orbital elements, and orbital elements determine the state of the object in its orbit.

**Variables**

- \(t\): date;
- \(X = (x, y, z)\): position vector;
- \(V = (V_x, V_y, V_z)\): velocity vector;
- \(a, e, i, \Omega, \omega, t_p\): orbital elements.

**Use in AstroPhenomena Explorer**

- bridge between physics simulation and orbital element input;
- orbit determination;
- ephemeris generation;
- spacecraft maneuver explanation.

**Scientific status**

True for a chosen central body and dynamical model. Perturbations and reference frames must be specified.

---

### 4.10 Atmospheric drag model

\[
F_{\text{drag}} \propto \rho_{\text{atm}} V^2
\]

**Meaning**

Atmospheric braking grows with atmospheric density and the square of velocity.

**Variables**

- \(\rho_{\text{atm}}\): atmospheric density;
- \(V\): velocity.

**Use in AstroPhenomena Explorer**

- satellite decay;
- reentry prediction;
- atmospheric braking explanation.

**Scientific status**

Simplified model. Real drag also depends on shape, area, mass, orientation and atmospheric variability.

---

### 4.11 Orbit determination workflow

\[
\text{Observations} \rightarrow \text{Dynamical model} \rightarrow \text{Orbit propagation} \rightarrow O-C \rightarrow \text{Refined orbit}
\]

**Meaning**

An orbit is determined by combining observations with a physical model, then comparing observed positions to calculated positions.

**Variables**

- \(O\): observed position;
- \(C\): calculated position;
- \(O-C\): residual.

**Use in AstroPhenomena Explorer**

- asteroid-tracking module;
- ephemeris validation;
- uncertainty visualization;
- citizen-science observation pipeline.

**Scientific status**

Conceptually reliable. Real orbit determination requires advanced numerical methods.

---

## 5. Relevance for AstroPhenomena Explorer

### Axe 1 — Comprendre le ciel

This course is indirectly relevant.

Axe 1 mainly needs sky coordinates, time and local visibility. However, celestial mechanics explains why planets, the Moon, comets and asteroids do not stay fixed on the celestial sphere.

Relevant concepts:

- apparent motion of planets;
- orbital elements;
- prograde and retrograde motion;
- ephemerides;
- perturbations;
- central body reference frames.

Possible uses:

- explain why planets move relative to stars;
- distinguish fixed stars from moving solar system objects;
- add simple orbit context to sky maps;
- explain why object coordinates change over time.

---

### Axe 2 — Observer le ciel

This course supports observation planning for moving objects.

Relevant concepts:

- ephemerides;
- NEOs;
- asteroid motion;
- satellite passes;
- orbital inclination;
- orbital period;
- magnitude and close approach.

Possible uses:

- plan observation of asteroids;
- understand satellite visibility windows;
- explain fast-moving objects in images;
- identify why close-approach objects can appear trailed during long exposures.

---

### Axe 3 — Prédire les phénomènes

This is one of the most important sources for Axe 3.

Relevant concepts:

- Keplerian motion;
- orbital elements;
- perturbations;
- numerical propagation;
- ephemerides;
- resonances;
- NEO impact prediction;
- transits and orbital nodes;
- uncertainty in predictions.

Possible modules:

- Phenomena Detector;
- Ephemeris Engine;
- Orbit Propagator;
- NEO Close Approach Viewer;
- Resonance Explorer;
- Transit Geometry Helper.

This course explains that prediction is not magic: it is based on a dynamical model, observations, orbit propagation and uncertainty management.

---

### Axe 4 — Simuler les phénomènes

This course is a core source for simulations.

Relevant concepts:

- elliptical orbits;
- area law;
- varying speed along orbit;
- orbital elements;
- tidal effects;
- Hill sphere;
- Roche limit;
- Lagrange points;
- resonances;
- gravitational assists;
- Hohmann transfers.

Possible simulations:

- Kepler orbit simulator;
- orbital element visualizer;
- resonance animation;
- tidal locking and libration simulator;
- Lagrange point explorer;
- gravity assist visualization;
- satellite orbit and debris simulator.

---

### Axe 5 — Produire de la science

This course is highly relevant to scientific applications.

Relevant concepts:

- orbit determination;
- NEO tracking;
- ephemerides;
- O-C residuals;
- observational uncertainty;
- orbit propagation;
- asteroid families;
- Gaia/JWST/Lagrange point missions;
- space debris monitoring.

Possible science workflows:

- measure asteroid positions from images;
- estimate an orbit from repeated observations;
- compare measured positions to predicted ephemerides;
- visualize uncertainty regions;
- analyze satellite/debris motion;
- explore asteroid families in \((a, e, i)\) space.

---

## 6. Possible Software Modules

| Possible module | Purpose | Related concepts | Priority |
|---|---|---|---|
| Orbit Elements Explorer | Teach and visualize \(a, e, i, \Omega, \omega, t_p\). | Orbital elements, reference planes, nodes | Very high |
| Kepler Orbit Simulator | Animate elliptical motion and varying orbital speed. | Kepler’s laws, area law, eccentricity | Very high |
| Solar System Dynamics Viewer | Show planets, asteroids and comets moving in heliocentric coordinates. | Keplerian orbits, perturbations, ephemerides | High |
| Ephemeris Engine | Predict object positions over time. | Orbit propagation, state vectors, numerical models | Very high |
| Resonance Explorer | Visualize mean-motion and spin-orbit resonances. | Resonances, Hilda, Trojan, Moon, Mercury | High |
| Lagrange Point Explorer | Explain L1–L5 and mission applications. | Lagrange points, JWST, Gaia, Trojan asteroids | High |
| Tidal Effects Simulator | Show tidal deformation, tidal locking and orbital evolution. | Tides, Roche limit, Moon, Io | Medium |
| NEO Tracker | Track near-Earth objects and close approaches. | NEO, NEA, PHA, MOID, ephemerides | High |
| Impact Risk Concept Lab | Explain uncertainty and impact prediction. | Orbit uncertainty, observations, O-C residuals | Medium to high |
| Orbit Determination Lab | Teach how observations refine an orbit. | Astrometry, orbit fitting, residuals | High |
| Astrodynamics Transfer Lab | Teach orbit changes by velocity impulses. | Hohmann transfer, delta-v, launch windows | High |
| Gravity Assist Simulator | Show how planets change spacecraft trajectories. | Relative velocity, reference frames, mission design | Medium |
| Satellite Pass Predictor | Predict artificial satellite visibility. | LEO, MEO, GEO, inclination, period | Medium |
| Space Debris Explorer | Visualize debris populations and reentry risks. | Debris, drag, Kessler syndrome, reentry | Medium |
| Mission Trajectory Viewer | Recreate trajectories of JUICE, Voyager, BepiColombo or OSIRIS-REx. | Gravity assists, transfer orbits, ephemerides | Medium |

---

## 7. Possible Visualizations and Interactions

| Visual / interaction | What it explains | Suggested form | Priority |
|---|---|---|---|
| Cannonball-to-orbit animation | Why orbit is continuous falling. | Animation | Very high |
| Kepler ellipse diagram | Ellipse, focus, semi-major axis and eccentricity. | Diagram + slider | Very high |
| Area law animation | Equal areas in equal times and varying speed. | Orbit animation | Very high |
| Orbital element 3D diagram | \(a, e, i, \Omega, \omega, t_p\). | Interactive 3D orbit | Very high |
| \(a,e\) diagram | Orbit classification and planet-crossing regions. | Data plot | High |
| Node crossing visual | Ascending/descending nodes and reference plane. | 3D diagram | High |
| Perturbed orbit animation | Difference between two-body and multi-body motion. | Animation | High |
| Neptune discovery story | Perturbations as predictive science. | Historical diagram | Medium |
| Resonance pendulum analogy | Why repeated perturbations matter. | Interactive analogy | Medium |
| Mean-motion resonance simulator | Rational period ratios and repeated alignments. | Orbit animation | High |
| Spin-orbit resonance simulator | Moon 1:1 and Mercury 3:2. | Animation | High |
| Libration animation | Why we see more than half the Moon. | Moon animation | Medium |
| Lagrange point map | L1–L5, stable/unstable zones and missions. | Diagram / interactive map | High |
| Hill sphere and Roche limit | Gravitational dominance and tidal disruption. | Diagram | Medium |
| Non-gravitational forces panel | Outgassing, radiation pressure, Yarkovsky. | Concept diagram | Medium |
| Chaos sensitivity demo | Divergence of nearby initial conditions. | Simulation | Medium |
| NEO uncertainty cone | Impact prediction depends on uncertainty. | Animated uncertainty plot | High |
| O-C residual plot | Difference between observations and calculations. | Data plot | High |
| Hohmann transfer diagram | Efficient orbit transfer. | Orbit animation | High |
| Launch window timeline | Why missions wait for planetary alignment. | Timeline | Medium |
| Gravity assist reference-frame comparison | Same flyby seen from planet and Sun frames. | Split-view animation | Medium |
| Satellite orbit families | LEO, MEO, GEO, SSO, Molniya, L-points. | Comparison diagram | Medium |
| Space debris population view | Orbital debris and collision risk. | Data visualization | Medium |

---

## 8. User Questions Enabled by This Course

| User question | Scientific concepts behind it | Possible module |
|---|---|---|
| Why does the Moon not fall onto Earth? | Orbital motion, gravity, tangential velocity | Kepler Orbit Simulator |
| What is an orbit? | Free fall, inertia, central gravity | Orbit Elements Explorer |
| Why are planetary orbits ellipses? | Kepler’s first law, two-body motion | Kepler Orbit Simulator |
| Why do planets move faster near the Sun? | Kepler’s second law | Area Law Animation |
| How can we describe a comet’s orbit? | \(a, e, i, \Omega, \omega, t_p\) | Orbit Elements Explorer |
| What does eccentricity mean? | Orbit shape, conic sections | Orbit Shape Slider |
| What is the difference between perihelion and aphelion? | Periapsis, apoapsis | Orbit Elements Explorer |
| Why are orbital nodes important? | Plane crossing, transits, close encounters | Node Crossing Visual |
| Why do asteroids have unstable orbits? | Perturbations, Jupiter, resonances | Resonance Explorer |
| How was Neptune predicted? | Perturbations and orbit modeling | Perturbation Story Module |
| Why does the Moon always show the same face? | Spin-orbit resonance, tidal locking | Spin-Orbit Simulator |
| Why can we see slightly more than half the Moon? | Libration | Libration Animation |
| What are Lagrange points? | Three-body balance, rotating frame | Lagrange Point Explorer |
| Why is JWST near L2? | Lagrange points, mission geometry | Lagrange Point Explorer |
| What is a near-Earth asteroid? | NEO, NEA, PHA, MOID | NEO Tracker |
| How do we know if an asteroid might hit Earth? | Orbit determination, propagation, uncertainty | Impact Risk Concept Lab |
| Why do more observations reduce impact uncertainty? | Orbit fitting, residuals, uncertainty | Orbit Determination Lab |
| How do spacecraft change orbit? | State vector, velocity impulse, orbital elements | Astrodynamics Transfer Lab |
| What is a launch window? | Planetary geometry, Hohmann transfer | Mission Trajectory Viewer |
| How does a gravity assist work? | Velocity vector, reference frames, planet flyby | Gravity Assist Simulator |
| Why are there different satellite orbits? | Orbital period, altitude, inclination, mission needs | Satellite Orbit Families |
| Why are space debris dangerous? | Debris population, collision cascade, drag | Space Debris Explorer |

---

## 9. Pedagogical Risks and Misconceptions

| Risk / misconception | Why it is problematic | How to avoid it |
|---|---|---|
| Thinking orbit means “no gravity” | Orbit exists because of gravity, not because gravity disappears. | Explain orbit as continuous free fall. |
| Thinking circular motion is the default for planets | Ellipses are the correct Keplerian shape. | Use ellipse diagrams and eccentricity sliders. |
| Assuming planets move at constant speed | Kepler’s second law says speed varies along an ellipse. | Animate equal areas in equal times. |
| Confusing semi-major axis with instantaneous distance | \(a\) is an orbital size parameter, not the current distance. | Show current radius separately from \(a\). |
| Confusing eccentricity with inclination | Eccentricity describes shape; inclination describes tilt. | Teach orbital elements visually in 3D. |
| Treating Keplerian orbits as perfect real orbits | Real orbits are perturbed by other bodies and forces. | Add “ideal model vs real model” labels. |
| Ignoring the reference plane | Inclination and nodes only make sense relative to a plane. | Always label ecliptic/equator/reference plane. |
| Thinking orbital elements never change | Osculating elements change under perturbations. | Distinguish osculating and proper elements. |
| Believing all predictions are equally reliable | Chaos and uncertainty limit long-term prediction. | Show prediction uncertainty growth. |
| Confusing NEO and PHA | A near-Earth object is not necessarily dangerous. | Add clear classification definitions. |
| Thinking impact prediction is binary | Impact risk depends on uncertainty and observations. | Use uncertainty regions and probability evolution. |
| Thinking a spacecraft speeds up by “stealing gravity” only | Gravity assist depends on reference frame and planet motion. | Use split planet-centered and Sun-centered views. |
| Thinking slowing down always lowers orbit immediately | Orbital maneuvers depend on position and velocity direction. | Show impulse effects at periapsis/apoapsis. |
| Confusing altitude with orbital energy | Higher orbit often means lower speed but greater orbital energy. | Use energy/period explanations. |
| Assuming satellite reentry is easy to predict | Atmospheric density depends on solar activity and is uncertain. | Explain drag uncertainty and reentry footprints. |
| Treating space debris as only a visual nuisance | Debris is a dynamical collision-risk problem. | Include Kessler syndrome and risk propagation. |

---

## 10. Scientific Traceability Notes

This source should be treated as a core conceptual reference for orbital mechanics, prediction and simulation inside AstroPhenomena Explorer.

### Reliable foundations from this source

The following ideas can be treated as foundational:

- orbit as free fall under gravity;
- Keplerian motion as the first-order model;
- semi-major axis, eccentricity and inclination as core orbital descriptors;
- nodes and orbital angles as necessary for 3D orbit orientation;
- perturbations as essential in the real Solar System;
- Jupiter as a major perturber for asteroids and comets;
- resonances as a structuring mechanism in orbital dynamics;
- ephemerides as predictions from celestial mechanics;
- orbit determination as observation plus dynamical modeling;
- state vector and orbital elements as equivalent representations;
- orbit changes as velocity changes at chosen positions;
- launch windows as consequences of orbital geometry;
- space debris as a growing dynamical hazard.

### Concepts that need additional references

Before precise software implementation, AstroPhenomena Explorer should validate:

- numerical orbit propagation methods;
- ephemeris standards and kernels;
- coordinate reference frames;
- time scales;
- perturbation models;
- NEO classification thresholds from current official sources;
- up-to-date NEO population statistics;
- space debris regulations and reentry risk standards;
- atmospheric drag models;
- satellite TLE handling.

### Concepts simplified for pedagogy

The following should be treated as educational simplifications:

- pure Keplerian orbits;
- two-body problem;
- simple resonance diagrams;
- Lagrange point stability diagrams;
- simplified drag proportional to \(\rho V^2\);
- ideal impulsive maneuvers;
- simplified Hohmann transfers.

### Formulas requiring validation before implementation

The Kepler relation

\[
\frac{a^3}{P^2} = \frac{GM}{4\pi^2}
\]

is central, but real implementation must specify units and central mass.

The state-vector/orbital-element conversion must define:

- reference frame;
- central body;
- epoch;
- gravitational parameter;
- perturbation model.

NEO and PHA classification should be verified with current JPL/CNEOS or MPC definitions before being coded.

### Future tests and calculations

Useful future validation tests:

- reproduce a circular orbit and check constant radius;
- animate an elliptical orbit and verify faster speed near periapsis;
- compare Kepler period calculations with known planetary periods;
- convert simple orbital elements to a state vector and back;
- compare project ephemerides with JPL Horizons or Skyfield;
- simulate a Hohmann transfer and verify transfer time;
- propagate a simple asteroid orbit and compare with reference data;
- show uncertainty reduction when adding observations;
- visualize how a small velocity impulse changes orbit elements.

---

## 11. Links to Future Knowledge Files

```txt
knowledge/concepts/gravity.md
knowledge/concepts/orbital_motion.md
knowledge/concepts/keplers_laws.md
knowledge/concepts/keplerian_orbit.md
knowledge/concepts/semi_major_axis.md
knowledge/concepts/eccentricity.md
knowledge/concepts/inclination.md
knowledge/concepts/orbital_elements.md
knowledge/concepts/periapsis_apoapsis.md
knowledge/concepts/orbital_nodes.md
knowledge/concepts/longitude_of_ascending_node.md
knowledge/concepts/argument_of_periapsis.md
knowledge/concepts/osculating_elements.md
knowledge/concepts/proper_elements.md
knowledge/concepts/perturbations.md
knowledge/concepts/three_body_problem.md
knowledge/concepts/mean_motion_resonance.md
knowledge/concepts/spin_orbit_resonance.md
knowledge/concepts/secular_resonance.md
knowledge/concepts/kozai_resonance.md
knowledge/concepts/libration.md
knowledge/concepts/tidal_effects.md
knowledge/concepts/hill_sphere.md
knowledge/concepts/roche_limit.md
knowledge/concepts/lagrange_points.md
knowledge/concepts/non_gravitational_forces.md
knowledge/concepts/yarkovsky_effect.md
knowledge/concepts/orbital_chaos.md
knowledge/concepts/near_earth_objects.md
knowledge/concepts/minimum_orbit_intersection_distance.md
knowledge/concepts/orbit_determination.md
knowledge/concepts/ephemerides.md
knowledge/concepts/state_vectors.md
knowledge/concepts/hohmann_transfer.md
knowledge/concepts/launch_windows.md
knowledge/concepts/gravity_assist.md
knowledge/concepts/atmospheric_drag.md
knowledge/concepts/satellite_orbits.md
knowledge/concepts/space_debris.md
knowledge/concepts/kessler_syndrome.md
```

---

## 12. Notes for AI Tools

This course is mainly useful for the **prediction and simulation backbone** of AstroPhenomena Explorer.

Future AI assistants should remember that this source explains how celestial positions evolve in time. It is the bridge between static sky coordinates and dynamic prediction. A body’s future position is not guessed from a sky chart; it is predicted from observations, orbital elements, state vectors, dynamical models and numerical propagation.

An AI should not assume that Keplerian motion is always enough. Keplerian orbits are excellent first models, but many project features require perturbations, non-gravitational effects, uncertainty and reference-frame awareness.

An AI should also distinguish between:

- an ideal orbit;
- an osculating orbit at a given date;
- a propagated ephemeris;
- a measured position;
- an uncertain future position.

This source is most connected to:

- Axe 3 — Prédire les phénomènes;
- Axe 4 — Simuler les phénomènes;
- Axe 5 — Produire de la science.

It supports Axe 1 and Axe 2 whenever the observed object is a moving body: planet, Moon, comet, asteroid, satellite or debris.

**AI takeaway:** This course gives AstroPhenomena Explorer its dynamical engine. It teaches that astronomical prediction requires gravity, orbital elements, perturbations, resonances, observations, uncertainty and ephemerides. Any module involving planets, asteroids, comets, satellites, transits, close approaches or mission trajectories should be grounded in the concepts introduced here.

---

## A. Suggested file name

```txt
knowledge/course_cards/du_ecu_celestial_mechanics.md
```

Alternative possible:

```txt
knowledge/course_cards/du_ecu_orbital_dynamics.md
```

## B. Concepts to add to `docs/03_Scientific_Map.md`

```txt
Gravity
Orbital motion
Kepler’s laws
Keplerian orbit
Semi-major axis
Eccentricity
Inclination
Orbital elements
Periapsis and apoapsis
Orbital nodes
Perturbations
Three-body problem
Mean-motion resonance
Spin-orbit resonance
Secular resonance
Kozai resonance
Libration
Tidal effects
Hill sphere
Roche limit
Lagrange points
Non-gravitational forces
Yarkovsky effect
Chaos
Near-Earth objects
MOID
Orbit determination
Ephemerides
State vectors
Hohmann transfer
Launch windows
Gravity assist
Atmospheric drag
Satellite orbits
Space debris
Kessler syndrome
```

## C. Visuals to consider later

```txt
Orbit as continuous falling animation
Kepler ellipse and focus diagram
Area law orbital speed animation
3D orbital elements visualizer
Eccentricity slider
Inclination and node diagram
Perturbed orbit comparison
Mean-motion resonance simulator
Spin-orbit resonance simulator
Moon libration animation
Lagrange point map
Hill sphere and Roche limit diagram
NEO close approach viewer
Orbit uncertainty cone
Orbit determination O-C residual plot
Hohmann transfer animation
Launch window timeline
Gravity assist split-frame animation
Satellite orbit family comparison
Space debris population visualization
```

## D. Priority assessment

**Core foundation.**

This course is essential for AstroPhenomena Explorer because it supports the transition from:

> “Where is an object in the sky?”

to:

> “Why is it there, how does it move, where will it be later, and how reliable is that prediction?”
