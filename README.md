# Mealy-to-Moore Finite State Machine (FSM) Converter & Simulator

A full-stack web application and algorithmic engine for converting **Mealy Machines** into equivalent **Moore Machines** using the standard state-splitting algorithm. Built with **Python (Flask)** on the backend and **HTML/CSS/JavaScript** with **Viz.js (Graphviz)** on the frontend, the tool validates formal machine definitions, generates interactive state transition diagrams, and runs step-by-step trace simulations to verify input-output equivalence.

---

## Key Features

- **Formal Input Validation:** Verifies state sets ($Q$), input alphabets ($\Sigma$), output alphabets ($\Delta$), initial state ($q_0$), and deterministic transition/output mappings ($\delta, \lambda$) before processing.
- **Automated State-Splitting Conversion:** Splits Mealy states associated with multiple incoming transition outputs into distinct Moore states ($q_{i}/y_{j}$) and handles unreachable or start-state edge cases.
- **Interactive State Diagrams:** Generates Graphviz `DOT` representations on the backend and renders side-by-side Mealy and Moore directed graphs in the browser via Viz.js.
- **Equivalence Trace Simulator:** Executes arbitrary input strings across both machines simultaneously, displaying state-by-state execution paths and confirming identical output sequences (accounting for the Moore machine's initial state output).
- **REST API Endpoints:** Exposes clean JSON endpoints (`/api/convert` and `/api/simulate`) for programmatic conversion and testing.

---

## Tech Stack

- **Backend:** Python 3, Flask
- **Frontend:** HTML5, CSS3 (Tailwind CSS), Vanilla JavaScript
- **Graph Visualization:** Graphviz DOT syntax rendered client-side with Viz.js

---

## Project Structure

```text
mealy-to-moore-converter/
├── app.py                  # Flask server, MealyToMooreConverter engine, and REST API routes
├── templates/
│   └── index.html          # Interactive web interface and Viz.js diagram renderer
├── static/                 # Custom stylesheets and client-side scripts (if separated)
├── requirements.txt        # Python dependencies
└── README.md
