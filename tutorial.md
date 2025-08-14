# Circuit Drafter: Quick Start Guide

Welcome to Circuit Drafter! This guide will get you drawing professional schematics in minutes. The interface is designed to be fast and intuitive.

### 1. Placing Your First Component
<img width="370" height="306" alt="place" src="https://github.com/user-attachments/assets/23a85fa3-5f2a-4a72-b7fa-785b6103d243" />

Components are located in the toolbar. Some, like Resistors, Capacitors, and Diodes, are grouped into **dropdown menus**.

*   **To Place:** Click a component icon (e.g., the Resistor). The tool becomes active. Click anywhere on the grid canvas to place it.
*   **Example:** Place a **Voltage Source**, a **Resistor**, and a **Ground** to start a simple circuit.

### 2. Wiring It Up
<img width="506" height="314" alt="wire" src="https://github.com/user-attachments/assets/8e500846-4c8b-4986-8c76-272f8ff15d28" />

Connecting components is easy with the smart wire tool.

*   Select the **Wire Tool (`W`)** from the toolbar.
*   Click and drag from one component terminal to another. The wire will automatically snap to connection points (indicated by a red circle).
*   **Right-Angle Wires (Manhattan):** The default behavior creates clean, 90-degree bends.
*   **Straight-Line Wires:** Hold **`Shift`** while dragging to draw a direct, point-to-point wire.

### 3. Selection & Manipulation
<img width="409" height="326" alt="select" src="https://github.com/user-attachments/assets/580904b9-d554-4ef3-99af-72667e9abbad" />

The **Select Tool (`S`)** is your primary tool for managing the circuit.

*   **Select:** Click an element. To select multiple, hold **`Shift`** and click, or drag a selection box (marquee) over the elements.
*   **Move:** Click and drag any selected element(s).
*   **Rotate (`R`):** Rotates the selected component(s) in 45° increments.
*   **Duplicate (`Ctrl+D`):** Instantly creates a copy of the selected element(s).
*   **Delete (`Del` / `Backspace`):** Removes whatever is selected.
*   **Undo/Redo (`Ctrl+Z` / `Ctrl+Y`):** Your safety net. Use the toolbar buttons or keyboard shortcuts to step backward or forward.
<img width="461" height="265" alt="duplicate" src="https://github.com/user-attachments/assets/80ffb5a8-4e51-4914-afef-46d3d8dd7375" /> <img width="223" height="148" alt="rotate" src="https://github.com/user-attachments/assets/07454a2d-f8e9-47e9-8523-eac92cc4d503" />


### 4. Adding Labels & Notes
Use the **Text Tool (`T`)** to add labels, values, and notes. The text engine supports LaTeX-style formatting.

<img width="794" height="562" alt="text" src="https://github.com/user-attachments/assets/39477b96-6330-44a7-a5b7-47a4d82ee031" />


<img width="187" height="91" alt="text_output" src="https://github.com/user-attachments/assets/a9e5ef46-810e-4895-aa03-6bc31cb8302a" />


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

<img width="215" height="137" alt="click" src="https://github.com/user-attachments/assets/b3c539a6-f262-44de-8165-8ad4cb634100" />

*   **Junction Dot:** **`Ctrl + Click`** on a wire or intersection to place a manual connection dot.
*   **Red Arrow Marker:** **`Alt + Click`** to place a small red arrowhead, perfect for indicating current flow or pointing to specific parts of the circuit.
*   **Open Terminal:** **`Double-click`** on an empty part of the canvas to create a circular open terminal point.
*   **Toggle Switch:** **`Double-click`** any SPST or SPDT switch to toggle its state (open/closed or position 1/2).
  
<img width="266" height="168" alt="switch" src="https://github.com/user-attachments/assets/b4ecff34-1ae3-4009-a2ee-8a225fcc222b" />

### 6. Bulk Operations for Large Circuits
For complex schematics, use the bulk tools. 

<img width="118" height="68" alt="bulk" src="https://github.com/user-attachments/assets/4852a242-c4a0-4487-9c21-57cf1e6e30fd" />


*   **Bulk Add Components (`playlist_add` icon):** Opens a table where you can list multiple components to add at once (e.g., `R` x 10, `C` x 5). You can even enable auto-labeling (R1, R2, etc.).
*   **Bulk Add Text (`format_list_bulleted_add` icon):**
    1.  **Add Labels:** Type a list of labels separated by a semicolon (`;`).
    2.  **Append a Circuit:** Paste the entire text content of a saved `.json` file into the box to append that circuit below your current drawing.

### 7. Saving & Exporting Your Work
Click the **Save Icon** or press **`Ctrl+S`** to open the save/export prompt.

<img width="183" height="187" alt="file" src="https://github.com/user-attachments/assets/005497c5-0a4a-4627-86e2-0b5f346289a6" />

*   **Save as JSON:** This is your **project file**. It saves everything and allows you to load it back into Circuit Drafter later for further editing (**`Ctrl+O`** to load).
*   **Export as PNG:** This creates a **high-resolution image** of your circuit, perfect for reports, presentations, or sharing.




# Tutorial: Using the Text Command Bar in Circuit Drafter

The Text Command Bar is a powerful feature for rapidly drafting circuits using simple, text-based commands. It allows you to place wires and components in sequence without using the mouse, making it ideal for quickly laying out schematics.



## The Basics

Commands are entered into the input bar and separated by spaces. The drawing starts at a default position on the canvas and continues from the end of the last placed element.

### Core Commands

There are two types of core commands: **Path Commands** for drawing wires and **Component Commands** for placing components.

#### 1. Path Commands

Path commands define how wires are drawn.

| Command | Description | Example | Result |
| :--- | :--- | :--- | :--- |
| `h <length>` | Draws a **h**orizontal wire. A negative length draws to the left. | `h 100` | Draws a wire 100 units to the right. |
| `v <length>` | Draws a **v**ertical wire. A negative length draws upwards. | `v -60` | Draws a wire 60 units up. |
| `cr <radius>` | Adds a **c**orner **r**adius (fillet) to the last corner. | `h 40 cr 10 v 40` | Draws an L-shape with a rounded corner. |
| `arrow` | Adds an arrowhead to the end of the previous wire segment. | `h 60 arrow` | Draws a horizontal wire with an arrow. |

You can also draw shapes directly in the wire path:

| Command | Description | Example |
| :--- | :--- | :--- |
| `box <w> <h>` | Draws a **box** of specified width and height. | `h 40 box 20 20 h 40` |
| `circle <r>` | Draws a **circle** with the specified radius. | `h 40 circle 15 h 40` |
| `triangle <báse> <h>` | Draws a **triangle** with the specified base and height. | `h 40 triangle 20 30 h 40` |

#### 2. Component Commands

Component commands place two-terminal components on the canvas. They automatically align with the preceding wire's direction.

-   **To place a component with a label:** Use the command followed by a number (e.g., `r1`, `c22`).
-   **To place a component without a label:** Use only the command (e.g., `r`, `c`).

| Command | Component | Example with Label | Example without Label |
| :--- | :--- | :--- | :--- |
| `r` | Resistor | `r1` | `r` |
| `c` | Capacitor | `c5` | `c` |
| `l` | Inductor | `l10` | `l` |
| `d` | Diode | `d3` | `d` |
| `zd` | Zener Diode | `zd1` | `zd` |
| `led` | LED | `led2` | `led` |
| `fwd` | Freewheeling Diode | `fwd1` | `fwd` |
| `sw` | Switch | `sw4` | `sw` |
| `vdc` | DC Voltage Source | `vdc1` | `vdc` |
| `vac` | AC Voltage Source | `vac2` | `vac` |
| `idc` | Current Source | `idc1` | `idc` |
| `dvs` | Dependent Voltage Source | `dvs1` | `dvs` |
| `dcs` | Dependent Current Source | `dcs1` | `dcs` |
| `batt` | Battery | `batt1` | `batt` |

## Building a Circuit: Step-by-Step Examples

#### Example 1: Simple RC Circuit

Let's build a simple series RC circuit.

**Command:** `vdc1 v -30 h 20 r1 h 20 v 20 c1 v 20 h -120 v-30`
**Breakdown:**
1.  `vdc1`: Places a DC Voltage Source named `V₁`. Since this is the first (vertical) component, the next element will start from its top terminal.
2.  `v -30`: Draws a vertical wire 30 units up.
3.  `h 20`: Draws a horizontal wire 20 units to the right.
4.  `r1`: Places a resistor `R₁` horizontally. (place after h command)
5.  `v 20`: Draws a vertical wire 20 units down.
6.  `c1`: Places a capacitor `C₁` vertically. (place after v command)

**Result:**
<img width="418" height="273" alt="image" src="https://github.com/user-attachments/assets/616ad8d2-1e0d-4678-912d-6368acc79198" />

#### Example 2: Line Path Commands

This example uses a rounded corner and places an arrow at the end.

**Command:** `h 60 cr 20 v 60 cr 30 h 120 cr 40 v -100  arrow`

**Breakdown:**
1.  `h 60`: Draws a horizontal wire.
2.  `cr 20 v 60`: Draws a vertical wire 60 units down with a corner radius of 20.
3.  `cr 30 h 120`: Draws a horizontal wire 120 units to the right with a corner radius of 30.
4.  `cr 40 v -100`: Draws a vertical wire 100 units up with a corner radius of 40.
5.  `arrow`: Places an arrowhead at the tip of the vertical line.

**Result:**
<img width="397" height="263" alt="image" src="https://github.com/user-attachments/assets/4dd42ea2-65d7-4f21-8b87-ca6a29fb8e1c" />

#### Example 3: Block diagram

**Command:** `h 40 arrow box 60 50 h 40 arrow circle 15 h 40 arrow triangle 60 60 h 40 arrow`

**Breakdown:**
1.  `h 40 arrow`: Draws a horizontal wire 40 units to the right with an arrowhead at the end.
2.  `box 60 50`: Draws a rectangular shape with 60 units width and 50 unit height.
3.  `h 40 arrow`: Draws a horizontal wire 40 units to the right with an arrowhead at the end.
4.  `circle 15`: Draws a circle with 15 units radius.
5.  `h 40 arrow`: Draws a horizontal wire 40 units to the right with an arrowhead at the end.
6.  `triangle 60 60`: Draws a triangle with 60 units width and 50 unit height. (the top in in horizontal direction)
7.  `h 40 arrow`: Draws a horizontal wire 40 units to the right with an arrowhead at the end.

**Result:**

<img width="616" height="231" alt="image" src="https://github.com/user-attachments/assets/5b76f5a0-aaa3-4460-aec7-1328f059add9" />

## Tips for Effective Use

-   **Start Simple:** Begin with basic `h`, `v`, and component commands to get a feel for the flow.
-   **Plan Your Path:** Think in terms of a continuous, clockwise path when laying out simple loops.
-   **Use Negative Values:** `h -50` and `v -50` are great for drawing left and up, respectively.
-   **Add Labels Later:** If you're unsure about numbering, place components without labels (`r`, `c`, `l`) and add text labels manually later.
-   **Chain Path Commands:** You can create complex wire shapes before placing a component, like `h 50 v 50 h -20 arrow r1`.
