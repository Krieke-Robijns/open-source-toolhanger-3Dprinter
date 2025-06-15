# open-source-toolhanger-3Dprinter
## Overview

This document describes a toolchanger system for FDM 3D printers. The design features a **centralized extrusion system, heatsink, cooling, and filament paths** permanently mounted on the motion carriage, while the **interchangeable toolheads** consist only of a **nozzle, heatblock, and heatbreak**.

## Core Principles

- **Centralized Cold Side**:  
  The extruder, heatsink, filament path, part cooling, and induction coil are all permanently installed on the main toolhead. Only the hot section is swapped.

- **Passive Hotends as Tools**:  
  Each tool is a passive module containing:
  - Brass nozzle
  - Stainless steel heatblock (induction-heated)
  - Heatbreak
  These tools do not contain electronics or active cooling.

- **Tool Holding & Clamping Mechanism**:
  The motion carriage contains a **split heatsink** mounted on a vertical linear rail. This heatsink can:
  - **Open and close** to grip the heatbreak via a hinged side
  - **Slide vertically** to engage or disengage the tool
  - **Transfer heat away** from the heatbreak through direct surface contact
  - One half of the heatsink is fixed to the linear rail block, the other swivels via a hinge.

- **Tool Change Process**:
  1. **Drop-off**:
     - Carriage aligns the hotend above a drop slot.
     - Slot allows the nozzle and heatblock to pass through but stops at the heatblock’s upper rim.
     - The carriage moves up.
     - Induction coil hinges out of the way to avoid collision.
     - Carriage lowers to rest in the slot.
     - Hinged half of heatsink opens, releasing the heatbreak.
     - Gantry moves backward, disengaging the heatbreak fully.
  
  2. **Pickup**:
     - Carriage aligns with new tool.
     - Gantry moves forward until the fixed half of the heatsink contacts the heatbreak.
     - Hinged half closes, gripping the heatbreak.
     - Carriage lifts the tool up from the slot.
     - Induction coil swivels back into heating position.
     - Carriage moves down positioning the heatblock in the induction coil.

- **Heatbreak Interface**:
  Heatbreaks have a **retaining flange** and a precisely machined surface to ensure reliable thermal contact when clamped in the heatsink. Spring-loaded force or     cam locking may be used to ensure constant contact pressure.

- **Cooling & Thermal Isolation**:
  - Tool heatblocks are heated via **induction coils**.
  - Cooling is handled by the central heatsink and **compressed air-assisted part cooling**.
  - The design ensures thermal separation between tools during inactive phases.

- **Alignment Safety & Feedback**:
  - Microswitches may be used to verify alignment before pickup.
  - Positional accuracy ensures high-speed tool changes are reliable.

- **Environmental Control**:
  - The printer operates in an enclosed chamber.
  - Air cooling is routed internally or via compressor lines.

## Legal Purpose

This document serves as **public prior art** to prevent the patenting of the mechanisms described herein. It is freely released under the MIT License and is intended to benefit the open-source hardware and 3D printing communities. Any party may use or modify the design, but **no patent claims may be made** on the concepts described.

## License

This design is released under the **MIT License** to encourage widespread use and innovation without restriction.
