# 🎨 UML Class Studio

> **Interactive Web-Based UML Class Diagram Editor, Architecture Evaluator & Code Generator**

UML Class Studio is a modern, single-page web application designed for software engineers, students, and system architects. It enables interactive creation of UML Class Diagrams, real-time diagnostic evaluation against key object-oriented architecture rules, and automated code generation for Java and C++.

---

## ✨ Features

- **Interactive Visual Canvas**: 
  - Drag-and-drop class cards with dynamic connector lines.
  - Infinite pan and smooth zoom (30% to 250%) controls.
  - Quick-action context menus for classes and relationships.
- **UML Class & Interface Editing**:
  - Support for standard Classes, Interfaces (`<<interface>>`), and Abstract Classes (`<<abstract>>`).
  - Double-click modal editing for Attributes (fields) and Operations (methods) with UML access modifiers (`+`, `-`, `#`).
- **Comprehensive Connector Types**:
  - **Association** (open chevron)
  - **Inheritance** / *extends* (hollow triangle)
  - **Implementation** / *implements* (dashed line with hollow triangle)
  - **Aggregation** (hollow rhombus diamond at owner)
  - **Composition** (solid rhombus diamond at owner)
  - Support for multiplicity notation (`1..1`, `1..*`, `0..*`).
- **Diagram Architecture Diagnostic Evaluator**:
  - Automated diagnostic scanner verifying standard OO design rules (e.g., interface realizations, circular inheritance detection, and aggregation method thresholds).
- **Multi-Language Code Generator**:
  - Generates syntactically valid **Java** and **C++** header/source code from diagram models.
- **Export & Persistence**:
  - Save/Load diagrams as standard JSON files.
  - Export diagram specifications to high-quality **PDF** documentation.
- **Dark Mode Support**: Built-in dark/light theme switcher tailored for modern developer environments.

---

## 🛠️ Tech Stack

- **HTML5 & Vanilla JavaScript (ES6+)**
- **SVG**: For vector relationship paths and marker endpoints.
- **Tailwind CSS**: Modern utility-first styling.
- **Font Awesome 6**: UI and stereotype iconography.
- **jsPDF**: Client-side PDF document generation.

---

## 🚀 Getting Started

No complex build pipeline or package installation is required! UML Class Studio is bundled as a clean, single-file client application.

### Running Locally

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/uml-class-studio.git
   cd uml-class-studio
   ```

2. **Open in Browser**:
   - Simply double-click `index.html` or open it with your browser of choice (Chrome, Firefox, Edge, Safari).
   - Alternatively, serve it locally using VS Code's **Live Server** or Python:
     ```bash
     python -m http.server 8000
     ```

---

## 📋 Diagram Architecture Rules Evaluated

The built-in **Evaluate Diagram** tool tests your model against six architectural best practices:

| Rule | Name | Description |
| :--- | :--- | :--- |
| **Rule 1** | Subclass Requirement | Abstract classes must be extended by at least one concrete child class. |
| **Rule 2** | Interface Realization | Interfaces must be implemented by at least one class. |
| **Rule 3** | Operation Completion | Classes implementing an interface must declare all signatures specified by that interface. |
| **Rule 4** | Circular Inheritance | Detects and flags circular inheritance loops. |
| **Rule 5** | Single Inheritance Check | Flags multiple class inheritance (restricted in languages like Java). |
| **Rule 6** | Aggregation & Composition | Verifies that aggregate owner classes (e.g. `Student` aggregating `Department`) contain a target field reference and at least **5 operational methods** demonstrating domain dependency. |

---

## ⌨️ Quick Controls & Shortcuts

- **Move / Select Tool**: Click & drag classes freely across the canvas.
- **Create Connector**: Click a connector tool from the palette (e.g. *Aggregation*), click the source class, then click the target destination class.
- **Edit Specification**: Double-click any class card to edit name, stereotype, fields, and operations.
- **Delete Relationship**: Click any connection path to highlight it, then press <kbd>Delete</kbd> / <kbd>Backspace</kbd> or click the floating **Delete** button.
- **Cancel Action**: Press <kbd>Escape</kbd> to cancel drawing active connector lines or close active popups.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).