🚚 Delivery Route Optimization — ADA Capstone Project
Course: Analysis and Design of Algorithms (ADA)
Problem: Optimize parcel delivery for an e-commerce platform across 7 customer locations.

Project Structure
delivery-route-mini-project/
├── notebooks/
│   └── delivery_route_optimization.ipynb   ← main deliverable
├── images/                                  ← plots generated at runtime
│   ├── route_visualization.png
│   ├── analysis_plots.png
│   └── speed_comparison.png
├── generate_notebook.py                     ← notebook generator script
├── requirements.txt
└── README.md
Tasks Covered
Task	Description	Algorithm	Complexity
1	Environment Setup	—	—
2	Input Modeling	Distance matrix, parcels, vehicle	—
3	Recurrence Route Cost	Recursive + Memoisation	O(n² · 2ⁿ)
4a	Parcel Selection	Greedy (V/W ratio)	O(n log n)
4b	Parcel Selection	DP 0/1 Knapsack	O(n · W)
4c	Time Windows	Simulation	O(n)
5a	Shortest Paths	Dijkstra	O((V+E) log V)
5b	Connectivity	MST — Prim's	O(E log V)
6	Optimal Sequence	TSP Held-Karp DP	O(n² · 2ⁿ)
7	Profiling & Plots	Timing + Visualisation	—
8	Summary & Reflection	Discussion	—
Setup & Run
# 1. Install dependencies
pip install -r requirements.txt

# 2. Launch JupyterLab
jupyter lab notebooks/delivery_route_optimization.ipynb

# 3. Run All Cells  (Kernel → Restart & Run All)
Input Data
8 nodes: Warehouse (0) + Loc_A … Loc_G (1–7) with 2D coordinates
7 parcels: value ∈ {80–200 Rs}, weight ∈ {3–10 kg}, time windows in 24h
Vehicle: max_weight = 25 kg, speed = 10 units/hr, departs at 08:00
Key Results (example run)
Metric	Value
DP-optimal parcel value	550 Rs
TSP route distance	~18–22 units
Greedy time	< 0.01 ms
TSP time (n=7)	< 5 ms
Version
v1.0-submission — ADA Capstone Final Submission
