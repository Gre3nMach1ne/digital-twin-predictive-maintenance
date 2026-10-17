# Project Progress

## Week 1 Setup (05.10.2026 - 11.10.2026)
- Project setup with uv
- Created folder structure
- First test notebook running
- First test python running

### Learnings
- uv is faster than pip + venv
- pyproject.toml replaces requirements.txt

## Week 2: Physics Refresher (12.10.2026 - 18.10.2026)

### Goal: 
Understand the physical fundamentals of filter clogging and implement first Python model.

### Tasks:
- Research Darcy's Law (relationship between pressure drop and permeability)
- Understand filter clogging model (exponential decrease of permeability)
- Create first notebook `01_physics_exploration.ipynb` with simulation
- Document findings in `docs/physics.md`

### Core formulas:
- Pressure drop: `ΔP = (μ · Q · L) / (k · A)`
- Permeability over time: `k(t) = k₀ · exp(-α · m(t))`

### Learnings
- Darcy's Law describes pressure drop through porous media
- Permeability decreases exponentially as particles accumulate
- Model parameters need realistic values to show meaningful behavior
- Small changes in α and c have large effects on pressure drop curve
- Simplifications (constant flow, uniform particles) are necessary for a first model