# Circuit Drafter (V0.32R)
<img width="200" height="200" alt="circuit-drafter-logo" src="https://github.com/user-attachments/assets/29b49b83-8617-48fc-aabf-a31d292b27f1" />

A simple, dependency-free, in-browser tool for quickly drafting electronic circuit diagrams. Everything runs client-side in a single HTML file.

**[View Live Demo](https://inverter3p.github.io/circuitdrafter/)**

<img width="1056" height="465" alt="circuitdrafter-v0.32b" src="https://github.com/user-attachments/assets/dc10be2e-41da-445c-b514-c0a613505a4a" />

---
## Circuit Drafter - V0.32R (Date: 2025-07-24)
*    **Math expression** can be evaluated inside &.....&
*   Add \times for multiply symbol.
*   Add dependent sources.
*   Double click component to direct edit rotation value.
## `update` What's New in V0.32b

*   **UI Overhaul**: The main toolbar has been reorganized for a more intuitive workflow. R/L/C components are now grouped together.
*   **Bulk Component Placement**: A new "Bulk Add Components" feature allows for rapid creation of multiple components via a table-based modal.
*   **Bulk Text Creation**: Add multiple text labels at once using a simple semicolon-delimited input.
*   **Smart Canvas Resizing**: The canvas now resizes dynamically to prevent bulk-added elements from being placed off-screen.
*   **Enhanced Text Engine**:
    *   Added support for LaTeX-style grouped subscripts and superscripts (e.g., `V_{in}`).
    *   Implemented fraction rendering with `\frac{numerator}{denominator}`.
    *   Fixed a rendering bug involving fractions with subscripts in the numerator.
*   **Bug Fixes**: Corrected selection box sizing for diodes, zener diodes, and LEDs. Ensured auto-generated component labels are always capitalized.

---

## `apps` Core Features

#### Drawing & Editing
*   **Component Library**: Includes resistors, capacitors, inductors, diodes (standard, Zener, LED), voltage/current sources, batteries, switches, and ground symbols.
*   **Smart Wiring**: Wires automatically snap to component terminals, the grid, and other wires. Junctions are created automatically.
*   **Versatile Selection**: Select individual components or use the marquee tool to select, move, duplicate, and rotate entire groups.
*   **Precise Control**: Draw right-angled (Manhattan) or straight-line wires. Manually place junction dots with `Ctrl` + `Click`.
*   **Standard Tools**: Full support for Undo/Redo, Duplicate, Rotate, and Delete.

#### Workflow & Usability
*   **File Management**: Save and load complete projects as `.json` files.
*   **High-Resolution Export**: Export schematics as high-quality `.png` images.
*   **Efficient Interface**: A streamlined toolbar and keyboard shortcuts for all major tools and actions.
*   **Snapping Grid**: Ensures all components and wires are perfectly aligned for a clean layout.

#### Advanced Text Engine
*   **Rich Formatting**: Create professional labels without external libraries.
*   **Subscripts & Superscripts**: Use `_` for subscripts (e.g., `V_in`) and `^` for superscripts (e.g., `10^-6`).
*   **Greek Letters & Symbols**: A full library of Greek letters is available (e.g., `\alpha`, `\mu`, `\Omega`).
*   **Fractions**: Render complex expressions with `\frac{}{}`.

---

## `build_circle` Getting Started

### Live Demo
The easiest way to use Circuit Drafter is to visit the **[Live Demo link](https://inverter3p.github.io/circuitdrafter/)**.

### Running Locally
1.  Clone this repository or download the `circuitdrafter.html` file.
    ```bash
    git clone https://github.com/inverter3p/circuitdrafter.git
    ```
2.  Open the `circuitdrafter.html` file in any modern web browser.

---

## `keyboard` Controls & Shortcuts

| Action | Tool / Shortcut | Description |
| :--- | :--- | :--- |
| **Tools** | | |
| Select / Move | `S` key | Select, move, and interact with elements. |
| Draw Wire | `W` key | Draw wires between points. |
| Add Text | `T` key | Add a rich text label to the canvas. |
| **Editing** | | |
| Undo | `Ctrl` + `Z` | Revert the last action. |
| Redo | `Ctrl` + `Y` | Re-apply the last undone action. |
| Duplicate Selection | `Ctrl` + `D` | Create a copy of the selected element(s). |
| Rotate Selection | `R` key | Rotate the selected component(s) by 45°. |
| Delete Selection | `Delete` / `Backspace` | Delete the currently selected element(s). |
| **Drawing** | | |
| Straight Line Wire | Hold `Shift` while drawing | Forces a direct, point-to-point wire. |
| Add Manual Junction | `Ctrl` + `Click` | Places a permanent connection dot on the canvas. |
| **Text Syntax** | `_{}`, `^{}`, `\frac` | `V_{in}` for subscript, `10^{-6}` for superscript, `\frac{V}{R}` for fractions. |

<img width="800"  alt="Example circuit diagram" src="https://github.com/user-attachments/assets/a0d6743d-8c30-48fa-bb09-aa8d223a1312" />

---

## `code` Technology Stack

*   **HTML5** (Canvas API)
*   **CSS3**
*   **Vanilla JavaScript (ES6+)**

No frameworks, no build steps, no nonsense. Just the web platform.

---

## `list` Roadmap
This project is under active development. Future plans include:

- [ ] **Expanded Component Library:** Add transistors (BJT, MOSFET), op-amps, and logic gates.
- [ ] **Component Properties Panel:** A dedicated UI to edit component values (e.g., "10kΩ", "100uF") and labels directly.
- [ ] **SVG Export:** Add an option to export diagrams as scalable vector graphics.
- [ ] **Improved Wire Editing:** Allow dragging and modification of existing wire segments.
- [ ] **Theming:** Introduce a dark mode for late-night drafting sessions.

---

## `description` License

This project is open source and available under the [MIT License](LICENSE).
