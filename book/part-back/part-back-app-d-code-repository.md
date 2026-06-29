
# Appendix D: Code Repository

```yaml
---
lifecycle_status:
  zone: "Zone 2 (Contextual Skeletons)"
  completeness: "60%"
  pending_tasks:
    - "Fill in analytical solutions and field equations during Phase 4 of each section."
    - "Validate coordinate geometries for PyVista and Manim animations."
    - "Test all code in both GUI and headless (off-screen) rendering modes."
    - "Cross-reference vector identities with Appendix B Heaviside mappings."
---
```

---

## Overview

This appendix documents all Python and Manim code used in the computational visualizations for Paper 1. The code is organized by section, with each section containing one or more Jupyter notebooks or Python scripts.

The toolchain follows the specifications established in Chapter 1, Section 1.4:

| Tool | Primary Use Case |
| :--- | :--- |
| **Matplotlib** | Static 2D planar vector fields and contour slices |
| **Plotly** | Interactive 3D scalar fields |
| **PyVista** | Volumetric 3D vector fields; field-line tracing; complex geometric deformations |
| **Manim** | Animations illustrating temporal changes |
| **Mayavi** | Optional pathway for advanced 3D scientific visualization (VTK-based) |

---

## D.1 Directory Structure

```
code/
├── README.md                                    # Setup instructions and overview
├── section-1-fluid-analogy/
│   ├── streamlines.ipynb                        # Matplotlib / Plotly
│   └── source-sink-animation.ipynb              # Manim
├── section-2-fundamental-quantities/
│   └── unit-flow-tube.ipynb                     # PyVista
├── section-3-circuit-laws/
│   └── circulation-animation.ipynb              # Manim
├── section-4-forces/
│   └── pressure-contours.ipynb                  # Matplotlib
├── section-5-applications/
│   └── solenoid-field.ipynb                     # Plotly / PyVista
└── part-2-electro-tonic/
    ├── vector-potential-3d.ipynb                # PyVista / Mayavi (optional)
    ├── curl-field-visualization.ipynb           # PyVista / Mayavi (optional)
    ├── faraday-animation.ipynb                  # Manim
    └── concept-map.ipynb                        # Matplotlib / Plotly
```

---

## D.2 Setup Instructions

### Environment Setup

1. **Create a virtual environment:**
   ```bash
   python -m venv maxwell_env
   source maxwell_env/bin/activate  # On Windows: maxwell_env\Scripts\activate
   ```

2. **Install dependencies:**
   ```bash
   pip install numpy matplotlib plotly pyvista manim
   ```

3. **Optional: Install Mayavi for advanced 3D visualization:**
   ```bash
   pip install mayavi
   ```

### Headless and Off-Screen Rendering Configuration

If you are running PyVista or Manim inside a headless environment (such as a Docker container, Windows Subsystem for Linux (WSL), or a remote JupyterHub server), you must configure a virtual frame buffer to avoid OpenGL driver initialization crashes.

Prior to launching any PyVista notebooks or executing Manim commands in headless setups, set the following environment variables in your terminal:

```bash
# Force PyVista to render off-screen without requiring a physical display
export PYVISTA_OFF_SCREEN=true

# Force Manim to run in headless mode
export MANIM_OFFSCREEN_RENDERING=true
```

**Alternative for WSL Users:** If the environment variables fail to initialize PyVista or Manim, you may need to install a virtual frame buffer:

```bash
sudo apt-get install xvfb
Xvfb :99 -screen 0 1024x768x24 &
export DISPLAY=:99
```

**Important:** Always verify your visualization configuration by running a minimal render test before attempting full section implementations. This prevents time-consuming debugging of graphics backends at the time of final code generation.

---

## D.3 Code Listings

### Section 1: Fluid Analogy Foundation

#### streamlines.ipynb (Matplotlib / Plotly)

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the potential function for a source-sink pair
def potential(x, y, q1_pos, q2_pos, q1=1.0, q2=-1.0):
    r1 = np.sqrt((x - q1_pos[0])**2 + (y - q1_pos[1])**2)
    r2 = np.sqrt((x - q2_pos[0])**2 + (y - q2_pos[1])**2)
    return q1 / r1 + q2 / r2

# Compute field lines (streamlines)
# [Full implementation to be written during Phase 4]
```

#### source-sink-animation.ipynb (Manim)

```python
from manim import *

class SourceSinkAnimation(Scene):
    def construct(self):
        # Create source and sink
        source = Dot(ORIGIN, color=RED, radius=0.2)
        sink = Dot(2*RIGHT, color=BLUE, radius=0.2)
        # Animate streamlines
        # [Full implementation to be written during Phase 4]
```

### Section 2: Fundamental Quantities

#### unit-flow-tube.ipynb (PyVista)

```python
import pyvista as pv
import numpy as np

# Define the flow tube geometry
# [Full implementation to be written during Phase 4]
```

### Section 3: Circuit Laws

#### circulation-animation.ipynb (Manim)

```python
from manim import *

class CirculationAnimation(Scene):
    def construct(self):
        # Animate magnetic field circulation around a current
        # [Full implementation to be written during Phase 4]
```

### Section 4: Forces Between Lines

#### pressure-contours.ipynb (Matplotlib)

```python
import numpy as np
import matplotlib.pyplot as plt

# Define pressure distribution around current filaments
# [Full implementation to be written during Phase 4]
```

### Section 5: Applications

#### solenoid-field.ipynb (Plotly / PyVista)

```python
import numpy as np
import plotly.graph_objects as go

# Compute and visualize magnetic field of a solenoid
# [Full implementation to be written during Phase 4]
```

### Part II: Electro-tonic State

#### vector-potential-3d.ipynb (PyVista / Mayavi optional)

```python
import pyvista as pv
import numpy as np

# Compute and visualize vector potential A around a current loop
# [Full implementation to be written during Phase 4]
```

#### curl-field-visualization.ipynb (PyVista / Mayavi optional)

```python
import pyvista as pv
import numpy as np

# Visualize the curl of the vector potential (B = ∇ × A)
# [Full implementation to be written during Phase 4]
```

#### faraday-animation.ipynb (Manim)

```python
from manim import *

class FaradayLawAnimation(Scene):
    def construct(self):
        # Animate changing magnetic flux inducing EMF
        # [Full implementation to be written during Phase 4]
```

#### concept-map.ipynb (Matplotlib / Plotly)

```python
import matplotlib.pyplot as plt
import networkx as nx

# Create concept map of Paper 1's relations
# [Full implementation to be written during Phase 4]
```

---

## D.4 Visualization Review Checklist

Each visualization should undergo the following review:

- [ ] Does the visualization accurately represent the mathematical quantities derived?
- [ ] Does the visualization capture the physical intuition Maxwell intended?
- [ ] What is the single most important insight this visualization communicates?
- [ ] What are the limitations of this visualization?
- [ ] Does the visualization run correctly in both GUI and headless environments?
- [ ] Have the vector identities in the visualization code been cross-referenced with Appendix B?

