# Circuit Drafter: Quick Start Guide

Welcome to Circuit Drafter! This guide will get you drawing professional schematics in minutes. The interface is designed to be fast and intuitive.

### 1. Placing Your First Component
Components are located in the toolbar. Some, like Resistors, Capacitors, and Diodes, are grouped into **dropdown menus**.

*   **To Place:** Click a component icon (e.g., the Resistor). The tool becomes active. Click anywhere on the grid canvas to place it.
*   **Example:** Place a **Voltage Source**, a **Resistor**, and a **Ground** to start a simple circuit.

### 2. Wiring It Up
Connecting components is easy with the smart wire tool.

*   Select the **Wire Tool (`W`)** from the toolbar.
*   Click and drag from one component terminal to another. The wire will automatically snap to connection points (indicated by a red circle).
*   **Right-Angle Wires (Manhattan):** The default behavior creates clean, 90-degree bends.
*   **Straight-Line Wires:** Hold **`Shift`** while dragging to draw a direct, point-to-point wire.

### 3. Selection & Manipulation
The **Select Tool (`S`)** is your primary tool for managing the circuit.

*   **Select:** Click an element. To select multiple, hold **`Shift`** and click, or drag a selection box (marquee) over the elements.
*   **Move:** Click and drag any selected element(s).
*   **Rotate (`R`):** Rotates the selected component(s) in 45° increments.
*   **Duplicate (`Ctrl+D`):** Instantly creates a copy of the selected element(s).
*   **Delete (`Del` / `Backspace`):** Removes whatever is selected.
*   **Undo/Redo (`Ctrl+Z` / `Ctrl+Y`):** Your safety net. Use the toolbar buttons or keyboard shortcuts to step backward or forward.

### 4. Adding Labels & Notes
Use the **Text Tool (`T`)** to add labels, values, and notes. The text engine supports LaTeX-style formatting.

*   Click the **Text Tool (`T`)**, then click on the canvas where you want the label.
*   A dialog will appear. Enter your text using these formats:
    *   **Subscript:** `V_{in}` or `R_1`
    *   **Superscript:** `x^2` or `I_{out}^2`
    *   **Fractions:** `\frac{V_{in}}{R_1}`
    *   **Greek Letters:** `\muF`, `\Omega`, `\delta`
*   **Edit Text:** Double-click any existing text label to edit it.
*   **Font Style:** You can choose between an *italic* (default) or normal font in the text dialog.

### 5. Power User Shortcuts
These shortcuts speed up your workflow significantly.

*   **Junction Dot:** **`Ctrl + Click`** on a wire or intersection to place a manual connection dot.
*   **Red Arrow Marker:** **`Alt + Click`** to place a small red arrowhead, perfect for indicating current flow or pointing to specific parts of the circuit.
*   **Open Terminal:** **`Double-click`** on an empty part of the canvas to create a circular open terminal point.
*   **Toggle Switch:** **`Double-click`** any SPST or SPDT switch to toggle its state (open/closed or position 1/2).

### 6. Bulk Operations for Large Circuits
For complex schematics, use the bulk tools.

*   **Bulk Add Components (`playlist_add` icon):** Opens a table where you can list multiple components to add at once (e.g., `R` x 10, `C` x 5). You can even enable auto-labeling (R1, R2, etc.).
*   **Bulk Add Text (`format_list_bulleted_add` icon):**
    1.  **Add Labels:** Type a list of labels separated by a semicolon (`;`).
    2.  **Append a Circuit:** Paste the entire text content of a saved `.json` file into the box to append that circuit below your current drawing.

### 7. Saving & Exporting Your Work
Click the **Save Icon** or press **`Ctrl+S`** to open the save/export prompt.

*   **Save as JSON:** This is your **project file**. It saves everything and allows you to load it back into Circuit Drafter later for further editing (**`Ctrl+O`** to load).
*   **Export as PNG:** This creates a **high-resolution image** of your circuit, perfect for reports, presentations, or sharing.
