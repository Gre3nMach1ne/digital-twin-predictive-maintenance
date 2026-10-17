# Physics Background

## Filter Clogging Model

### Key Concepts
- Darcy's Law
- Permeability Decay (Pressure drop vs. particle accumulation)

### Darcy's Law

Describes the pressure drop across a porous medium:

ΔP = (μ · Q · L) / (k · A)

| Symbol | Meaning | Unit |
|--------|---------|------|
| ΔP | Pressure drop | Pa |
| μ | Dynamic viscosity | Pa·s |
| Q | Volume flow rate | m³/s |
| L | Filter thickness | m |
| k | Permeability | m² |
| A | Filter area | m² |

**Interpretation:**
- Numerator (μ · Q · L): Factors that increase pressure drop
- Denominator (k · A): Factors that decrease pressure drop

### Permeability Decay

As particles accumulate, permeability k decreases exponentially over time:

k(t) = k₀ * exp(-α * m(t))

| Symbol | Meaning | Units |
|--------|---------|-------|
| k₀ | Initial permeability (clean filter) | m² |
| α | Clogging coefficient | 1/g |
| m(t) | Accumulated particle mass at time t | g |

**Behavior:** More particles → lower permeability → higher pressure drop → filter needs replacement.

### Model Explanation

The model combines Darcy's Law with exponential permeability decay to simulate filter clogging over time:

1. Particles enter the filter at a constant rate (c · Q)
2. Accumulated particle mass m(t) grows linearly over time
3. Permeability k(t) decreases exponentially as particles accumulate
4. Pressure drop ΔP increases as permeability drops

This creates a feedback loop: more contamination → higher pressure drop → filter approaches end of life.

### Parameter Overview

| Parameter | Role in Model |
|-----------|---------------|
| μ, Q, L, A | Fixed system properties (fluid, flow rate, filter geometry) |
| k₀ | Starting condition – how permeable is a clean filter? |
| α | Sensitivity – how quickly does contamination affect permeability? |
| c | Input – how dirty is the incoming fluid? |

### Simplifications and Assumptions

- **Constant flow rate:** In reality, Q may vary with operating conditions
- **Uniform particle distribution:** Model assumes particles spread evenly across filter area
- **No particle size distribution:** All particles treated equally, regardless of size
- **Linear mass accumulation:** Assumes constant contamination rate over time
- **Exponential decay model:** Simplified representation; real filters may show different behavior (e.g., cake filtration)
- **Isothermal conditions:** Temperature effects on viscosity not considered
- **Illustrative parameters:** Values not calibrated to real filter data
