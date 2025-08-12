

# Circuit Drafter (V0.48b)
<img width="200" height="200" alt="circuit-drafter-logo" src="https://github.com/user-attachments/assets/29b49b83-8617-48fc-aabf-a31d292b27f1" />

A simple, dependency-free, in-browser tool for quickly drafting electronic circuit diagrams and block diagrams. Everything runs client-side in a single HTML file.

**[View Live Demo](https://inverter3p.github.io/circuitdrafter/)**


<img width="1082" height="689" alt="Screenshot_409" src="https://github.com/user-attachments/assets/5f5005be-8406-4493-bb3e-71f8b1c68f0c" />

---
## `update` What's New & Version History

### V0.48b (2025-08-11)
*   **Block Diagram Shapes**: The Path Wire tool is now a powerful block diagram creator! Use commands like `box`, `triangle`, and `circle` to draw shapes directly within a path. Shapes are automatically oriented based on the path's direction (horizontal or vertical).
*   **Example Command**: `h 100 arrow box 60 40 h 100 arrow` creates a complete block diagram element.
    mg width="563" height="484" alt="Screenshot_410" src="https://github.com/user-attachments/assets/4850e1c5-1d19-4e2c-8874-07c8561b207c" />

### V0.43a (2025-08-07)
*   **Path Wire Tool**: Introduced the "Path Wire" tool (`P` key) for creating complex, multi-segment wires and diagrams using simple text commands (e.g., `h 100 cr 20 v 50 `).
*   **Arrowheads**: Added an `arrow` command to the path tool to easily create directional flows.

### V0.42aR (2025-08-07)
*   **Component Scaling**: Components can now be resized via a transform modal (double-click a component). All drawing functions were refactored to respect custom dimensions.
*   **Expanded Component Library**: Added NPN/PNP transistors, N-CH/P-CH MOSFETs, and Op-Amps.
*   **AI Circuit Generation**: Integrated a "Draw by AI" feature using the Gemini API to generate circuits from natural language descriptions.

### V0.32R (2025-07-24)
*   **Math Evaluation**: Text labels can now evaluate mathematical expressions wrapped in `&...&` (e.g., `&(1/15)+8**2&`).
*   **New Components**: Added dependent voltage and current sources.
*   **Direct Rotation Edit**: Double-click a component to open a modal and directly edit its rotation, flip, and scale properties.

---

## `apps` Core Features

#### Drawing & Editing
*   **Component Library**: Resistors, capacitors, inductors, diodes, transistors (BJT, MOSFET), Op-Amps, dependent/independent sources, switches, and ground symbols.
*   **Smart Wiring**: Wires automatically snap to component terminals, the grid, and other wires. Junctions are created automatically.
*   **Path Wire for Block Diagrams**: Use text commands (`h`, `v`, `box`, `circle`, `arrow`) to create complex signal flow and block diagrams.
*   **Versatile Selection**: Select individual components or use the marquee tool to select, move, duplicate, and rotate entire groups.
*   **Precise Control**: Draw right-angled (Manhattan) or straight-line wires. Manually place junction dots with `Ctrl` + `Click`.
*   **Full Component Transforms**: Double-click any component to precisely set its rotation, scale, and horizontal/vertical flip.

#### Workflow & Usability
*   **AI-Powered Generation**: Describe a circuit in plain English and let the AI assistant generate a schematic for you.
*   **Bulk Operations**: Rapidly place multiple components or text labels at once using intuitive modals.
*   **File Management**: Save and load complete projects as `.json` files.
*   **High-Resolution Export**: Export schematics as high-quality `.png` images with a user-defined scale factor.

#### Advanced Text Engine
*   **Rich Formatting**: Create professional labels without external libraries.
*   **LaTeX-Style Syntax**: Use `_` for subscripts (`V_in`), `^` for superscripts (`10^-6`), and `\frac{}{}` for fractions.
*   **Greek Letters & Symbols**: A full library of Greek letters is available (e.g., `\alpha`, `\mu`, `\Omega`, `\times`).
*   **In-Label Math**: Automatically calculate and display results of expressions like `&(5*2.2)/1.1&`.

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
| Draw Wire | `W` key | Draw standard circuit wires. |
| Path Wire / Block Diagram | `P` key | Draw complex paths and shapes with text commands. |
| Add Text | `T` key | Add a rich text label to the canvas. |
| **Editing** | | |
| Undo / Redo | `Ctrl` + `Z` / `Ctrl` + `Y` | Revert or re-apply actions. |
| Duplicate Selection | `Ctrl` + `D` | Create a copy of the selected element(s). |
| Rotate Selection | `R` key | Rotate selected component(s) by 45°. |
| Delete Selection | `Delete` / `Backspace` | Delete the currently selected element(s). |
| **Drawing** | | |
| Straight Line Wire | Hold `Shift` while drawing | Forces a direct, point-to-point wire. |
| Add Manual Junction | `Ctrl` + `Click` | Places a permanent connection dot on the canvas. |
| Add Manual Arrow | `Alt` + `Click` | Places an arrowhead on the canvas. |
| Change Color | `Alt` + `C` | Change component color to 'Red'. |
| **Path Commands** | `h 100`, `v 50`, `box 60 40` | Examples for drawing horizontal/vertical lines and shapes. |




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

- [ ] **Expanded Component Library:** Add logic gates and other integrated circuits.
- [ ] **Component Properties Panel:** A dedicated UI to edit component values (e.g., "10kΩ", "100uF") and labels directly.
- [ ] **SVG Export:** Add an option to export diagrams as scalable vector graphics.
- [ ] **Improved Wire Editing:** Allow dragging and modification of existing wire segments.
- [ ] **Theming:** Introduce a dark mode for late-night drafting sessions.

---

## `description` License

This project is open source and available under the [MIT License](LICENSE).
