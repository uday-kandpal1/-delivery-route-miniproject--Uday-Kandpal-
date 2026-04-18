# E-Commerce Delivery Route Optimization 🚚

**Course:** Analysis and Design of Algorithms (ADA) - Capstone Project  
**Version:** `v1.0-submission`

## 📖 Overview
E-commerce platforms face complex delivery challenges that combine time, cost, and vehicle constraints. The delivery routing problem involves selecting parcels, respecting delivery windows, and planning optimal travel paths. 

This project integrates multiple algorithmic paradigms across the ADA syllabus to solve these challenges. It offers a hands-on exploration of algorithmic decision-making in real-world logistics, comparing Greedy approaches, Dynamic Programming, Graph Pathfinding, and the Traveling Salesman Problem (TSP).

---

## 📂 Project Structure

```text
delivery-route-mini-project/
├── notebooks/
│   └── delivery_route_optimization.ipynb   ← Main deliverable (Jupyter Notebook)
├── images/                                 ← Plots generated at runtime
│   ├── route_visualization.png
│   └── complexity_graphs.png
├── requirements.txt                        ← Environment dependencies
└── README.md                               ← Project documentation
```
🧠 Algorithms & Complexity Analysis

This project implements the following strategies to tackle different facets of the routing problem:

```Task Focus   ,Algorithmic Strategy,Purpose,Time Complexity,Space Complexity
Route Costing,Recurrence (Recursion),Calculate total distance for sequences.,O(N) per route,O(N) stack depth
Parcel Selection (Fast),Greedy Algorithm,Maximize value using Value/Weight ratio.,O(NlogN),O(N)
Parcel Selection (Optimal),Dynamic Programming,0/1 Knapsack to maximize value strictly within capacity constraints.,O(N×W),O(N×W)
Pathfinding,Dijkstra's Algorithm,Navigate the absolute shortest path between two specific stops.,O(E+VlogV),O(V)
Network Connectivity,Kruskal's/Prim's (MST),Find the Minimum Spanning Tree of the delivery network.,O(ElogE),O(V+E)
Optimal Routing,TSP (Brute Force),Find the absolute optimal round-trip sequence hitting all customers.,O(N!),O(N)
```
🚀 Setup & Execution
Prerequisites
Python 3.10+

Git & GitHub

1. Environment Setup
Clone the repository and install the required dependencies:
# Create and activate a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install libraries
pip install -r requirements.txt

2. Running the Project
Launch JupyterLab to interact with the code, view the profiling metrics, and generate the network graphs:
jupyter lab notebooks/delivery_route_optimization.ipynb

🔬 Discussion & ReflectionOptimization vs. Realism: The optimal TSP route strictly minimizes distance but ignores delivery time windows. Real-world logistics require complex

heuristic models (like TSPTW) to balance shortest distance with strict delivery deadlines.Algorithm Trade-offs: The Greedy algorithm proved exceptionally fast ($O(N \log 

N)$) but occasionally missed the mathematical optimum. DP guaranteed the highest profit but at a massive memory cost ($O(N \times W)$) when vehicle capacity scaled up.The NP-

Hard Challenge: The Brute-Force TSP algorithm scales factorially ($O(N!)$). Profiling demonstrated that while $N=5$ evaluates instantly, $N \ge 12$ becomes computationally

infeasible on standard hardware, proving why enterprise logistics rely on approximation algorithms rather than perfect solvers.

Version: v1.0-submission — ADA Capstone Final Submission
