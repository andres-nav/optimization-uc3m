# Optimization — UC3M

Mathematical optimization coursework at Universidad Carlos III de Madrid. Two assignments covering portfolio optimization and network flow problems.

## HW1 — ETF Portfolio Optimization

Linear and mixed-integer programming models for European ETF allocation. Optimizes portfolios for different investor profiles (young/mid-age/elderly) by maximizing returns subject to risk, diversification, and asset allocation constraints.

**Key features:**
- Dataset: 9500+ European ETFs from MorningStar (returns, risk, sectors, sustainability)
- Continuous model: LP with 13 constraint types (risk, allocation, fund size, dividends, assets, sustainability)
- Mixed-integer model: Binary variables for long/short positions, conditional constraints, purchase fees
- Sensitivity analysis: Shadow prices reveal constraint impacts (risk +0.92, stocks +0.08, bonds -0.04)
- Results: 70% return (young/risky), 14% return (elderly/conservative) with optimized allocations

**Tools:** Pyomo, Gurobi, pandas, matplotlib

## HW2 — Network Flow Optimization

Min-cost flow optimization on router networks with capacity constraints and half-duplex edges.

**Linear model:**
- Objective: Minimize total routing cost
- Constraints: Flow conservation, capacity limits, one-way flow (half-duplex), source/sink balance
- Result: Optimal path selection with 30 units routed from node 9→2

**Non-linear extension:**
- Quadratic objective: Penalizes high-flow edges (degradation cost)
- Quadratic constraints: Flow progression decay, router buffer limits
- Result: Distributed flow across multiple paths (10 units, 9→2) for reliability

**Tools:** Pyomo, Gurobi, NetworkX, matplotlib

## Project Structure

```
.
├── 01/
│   ├── ETFs.csv                      # European ETF dataset
│   ├── Navarro-Andres-HW1.ipynb      # Portfolio optimization
│   └── Navarro-Andres-HW1.html
├── 02/
│   ├── Navarro_Andres_HW2.ipynb      # Network flow optimization
│   └── Navarro_Andres_HW2.html
└── README.md
```

## Stack

Python 3.10+ • Pyomo • Gurobi • pandas • NumPy • matplotlib • NetworkX