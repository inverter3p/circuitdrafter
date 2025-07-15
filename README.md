# Circuit Drafter (V0.1a)

![Circuit Drafter Screenshot](https://user-images.githubusercontent.com/1011386/160295843-7f551c9d-8c1d-4f68-9844-3151859c76d2.gif)
*(Suggestion: Create a short GIF like the one above showing the tool in action and replace this placeholder)*

A simple, dependency-free, in-browser tool for quickly drafting electronic circuit diagrams. Everything runs client-side in a single HTML file.

**[➡️ View Live Demo Here](https://inverter3p.github.io/circuitdrafter/)**

<img width="1112" height="556" alt="circuitdrafter" src="https://github.com/user-attachments/assets/59defc63-893b-46f5-b65e-96d953b28c50" />

---

## ✨ Features

This initial version (v0.1a) provides a solid foundation for a powerful circuit drafting tool:

*   **Core Drawing Tools:**
    *   **Component Library:** Includes Resistor, Capacitor, Inductor, Diode, Voltage Source, Battery, and Ground symbols.
    *   **Smart Wiring:** Wires automatically snap to component terminals, the grid, or other wires.
    *   **Manhattan & Direct Routing:** Draw right-angled (Manhattan) wires by default, or hold `Shift` for straight-line (direct) connections.
    *   **Automatic Junctions:** Junction dots are automatically drawn where three or more wires/terminals connect.
    *   **Text Labels:** Add text annotations to your schematic. Supports the `Ω` symbol via the `/ohm` shortcut.

*   **Editing & Workflow:**
    *   **Select & Move:** Easily select and reposition any element on the canvas.
    *   **Rotate:** Rotate selected components in 45-degree increments.
    *   **Duplicate:** Quickly copy and paste selected elements.
    *   **Delete:** Remove unwanted elements from the schematic.
    *   **Undo/Redo:** Full history support for undoing and redoing actions.

*   **Usability:**
    *   **Keyboard Shortcuts:** Intuitive hotkeys for tools and actions to speed up your workflow.
    *   **Snapping Grid:** Elements and wire points snap to a grid for clean, aligned diagrams.
    *   **High-Resolution Export:** Export your entire circuit as a crisp PNG image with a user-defined resolution scale.

*   **Technology:**
    *   **100% Client-Side:** Runs entirely in your browser. No server or backend required.
    *   **Zero Dependencies:** Written in pure, vanilla JavaScript, HTML, and CSS. No frameworks or external libraries (besides Google Material Icons).

---

## 🚀 How to Use

### Live Demo
The easiest way to use Circuit Drafter is to visit the **[Live Demo link](https://inverter3p.github.io/circuitdrafter/)**.

### Running Locally
Since this is a self-contained application, running it locally is extremely simple.

1.  Clone this repository or download the `circuitdrafter.html` file.
    ```bash
    git clone https://github.com/inverter3p/circuitdrafter.git
    ```
2.  Open the  file in any modern web browser (like Chrome, Firefox, or Edge).

That's it! You're ready to start drafting.

---

## ⌨️ Controls & Keyboard Shortcuts

| Action                 | Tool / Shortcut                  | Description                                            |
| ---------------------- | -------------------------------- | ------------------------------------------------------ |
| **Tools**              |                                  |                                                        |
| Select / Move          | `S` key                          | Select, move, and interact with elements.              |
| Draw Wire              | `W` key                          | Draw wires between points.                             |
| Add Text               | `T` key                          | Add a text label to the canvas.                        |
| **Editing**            |                                  |                                                        |
| Undo                   | `Ctrl` + `Z`                     | Revert the last action.                                |
| Redo                   | `Ctrl` + `Y`                     | Re-apply the last undone action.                       |
| Duplicate Selection    | `Ctrl` + `D`                     | Create a copy of the selected element.                 |
| Rotate Selection       | `R` key                          | Rotate the selected component by 45°.                  |
| Delete Selection       | `Delete` / `Backspace`           | Delete the currently selected element.                 |
| **Wire Drawing**       |                                  |                                                        |
| Straight Line Wire     | Hold `Shift` while drawing a wire | Forces a direct, point-to-point wire.                  |

---

## 🛠️ Technology Stack

*   **HTML5** (Canvas API)
*   **CSS3**
*   **Vanilla JavaScript (ES6+)**

No frameworks, no build steps, no nonsense. Just the web platform.

---

## 📝 Future Development (To-Do)

This project is in its early stages. Here are some ideas for future versions:

-   [ ] **More Components:** Add transistors (BJT, MOSFET), op-amps, logic gates, etc.
-   [ ] **Component Properties:** A panel to edit component values (e.g., "10kΩ", "100uF") and labels.
-   [ ] **Save/Load Project:** Implement saving the circuit state to a local `.json` file or browser `localStorage`.
-   [ ] **SVG Export:** Add an option to export diagrams as scalable vector graphics.
-   [ ] **Theming:** Introduce a dark mode for late-night drafting sessions.
-   [ ] **Improved Wire Editing:** Allow dragging and modification of existing wire segments.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
