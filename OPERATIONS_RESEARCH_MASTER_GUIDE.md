# 📚 OPERATIONS RESEARCH (OR) — COMPLETE ENCYCLOPEDIC MASTER GUIDE & LEARNING PLATFORM BLUEPRINT
> **Course Scope:** Unit 1 (Introduction & Linear Programming) & Unit 2 (Transportation, Assignment & Sequencing)  
> **Purpose:** 100% Comprehensive Learning Curriculum, Step-by-Step Solver Reference, Oral Puzzle Bank, and Interactive Web Application Architecture.

---

## 🧭 SYSTEM ARCHITECTURE & WEB APP NAVIGATION (TASKBAR LAYOUT)
When implemented in the interactive web application, the navigation header and sidebar are structured as follows:

```
┌───────────────────────────────────────────────────────────────────────────────────────────────────────┐
│  🌐 OR-MASTER: Interactive Learning & Solver Engine                                                   │
├───────────────────────────────────────────────────────────────────────────────────────────────────────┤
│  [🏠 Dashboard]  [📘 Module 1: Linear Programming]  [🚚 Module 2: Networks & Scheduling]  [⚡ Puzzles]  │
│  [📊 Solvers: 2D Graph | Simplex | Big-M | Two-Phase | VAM/MODI | Hungarian | Gantt]  [🎯 Exam Mode]  │
└───────────────────────────────────────────────────────────────────────────────────────────────────────┘
```

---

# 📖 MODULE 1: INTRODUCTION TO OR & LINEAR PROGRAMMING (12 HOURS)

---

## 🔹 MICRO-TOPIC 1.1: Foundations & Mathematical Modeling in OR

### 1. Core Theory & Definitions
* **Operations Research (OR)** is the application of advanced analytical methods (mathematical modeling, statistical analysis, and mathematical optimization) to help make better decisions in complex organizational systems.
* **Phases of OR Study**:
  1. *Formulation of the Problem* (Identifying decision variables, objective, and constraints).
  2. *Construction of a Mathematical Model* (Converting English statements into linear/non-linear equations).
  3. *Deriving Solutions from the Model* (Applying algorithms: Graphical, Simplex, MODI, Hungarian, etc.).
  4. *Model Testing & Validation* (Sensitivity analysis, verifying feasibility in real world).
  5. *Implementation & Control* (Deploying the optimal operational policy).
* **Anatomy of an LPP (Linear Programming Problem)**:
  $$\text{Optimize (Max or Min) } Z = c_1 x_1 + c_2 x_2 + \dots + c_n x_n \quad \text{(Objective Function)}$$
  Subject to:
  $$\begin{aligned}
  a_{11} x_1 + a_{12} x_2 + \dots + a_{1n} x_n &\le \text{ (or } \ge, = \text{) } b_1 \\
  a_{21} x_1 + a_{22} x_2 + \dots + a_{2n} x_n &\le \text{ (or } \ge, = \text{) } b_2 \\
  &\vdots \\
  a_{m1} x_1 + a_{m2} x_2 + \dots + a_{mn} x_n &\le \text{ (or } \ge, = \text{) } b_m \quad \text{(Linear Constraints)}
  \end{aligned}$$
  With non-negativity:
  $$x_1, x_2, \dots, x_n \ge 0 \quad \text{(Non-negativity Restrictions)}$$
* **Assumptions of Linear Programming**:
  1. *Linearity / Proportionality*: The contribution of each variable to $Z$ and constraints is strictly proportional to its value.
  2. *Additivity*: Total resource usage and total profit are the algebraic sum of individual contributions.
  3. *Divisibility (Continuity)*: Decision variables can take fractional / continuous values.
  4. *Certainty / Determinism*: All parameters ($c_j, a_{ij}, b_i$) are known constants with $100\%$ certainty.
  5. *Finiteness*: Finite number of activities and resource constraints.
  6. *Single Objective*: Only one criterion (either profit max or cost min) is pursued.
* **Limitations of OR**:
  - Neglects qualitative and human emotional factors.
  - Linear assumptions often fail in economies of scale.
  - High computational complexity for large integer/non-linear systems.

---

### 2. Formulation Problem Subtypes & Exam Recognition
* **Subtype 1.1.A: Product Mix Allocation (Maximization)**
  * *Trigger Words*: "Produces products A and B", "machine hours available", "unit profit", "maximize total profit".
  * *Standard Structure*: $\text{Max } Z = p_1 x_1 + p_2 x_2$ subject to resource usage $\le$ available capacity.
* **Subtype 1.1.B: Diet & Blending (Minimization)**
  * *Trigger Words*: "Minimum daily requirement of Vitamin A, B", "Cost per kg of food 1 and 2", "minimize cost".
  * *Standard Structure*: $\text{Min } Z = c_1 x_1 + c_2 x_2$ subject to nutrient intake $\ge$ minimum requirement.
* **Subtype 1.1.C: Trim Loss / Cutting Stock Problem**
  * *Trigger Words*: "Roll width $W$", "cut into demand widths $w_1, w_2$", "minimize scrap / trim loss".

---

### 3. Fully Worked Formulation Example
> **Problem Statement:** A carpentry shop manufactures Tables ($x_1$) and Chairs ($x_2$). Each table yields \$50 profit and requires 2 hours of carpentry and 1 hour of painting. Each chair yields \$30 profit and requires 1 hour of carpentry and 1 hour of painting. The shop has at most 80 hours of carpentry and 50 hours of painting per week. Formulate the LPP.

* **Step 1: Identify Decision Variables**:
  - Let $x_1 =$ Number of tables produced per week.
  - Let $x_2 =$ Number of chairs produced per week.
* **Step 2: Formulate Objective Function**:
  $$\text{Maximize } Z = 50x_1 + 30x_2$$
* **Step 3: Formulate Constraints**:
  - Carpentry: $2x_1 + 1x_2 \le 80$
  - Painting: $1x_1 + 1x_2 \le 50$
* **Step 4: Non-negativity**:
  $$x_1 \ge 0, \quad x_2 \ge 0$$

---

### 4. ⚡ Zero-Pen Oral Puzzles (No Paper Needed)
1. **Puzzle 1:** If a factory can produce fractional chairs (e.g. 3.5 chairs), which core assumption of LPP allows this?  
   *Answer:* **Divisibility (Continuity)**.
2. **Puzzle 2:** A manager says "If I double chair production, the unit profit jumps from \$30 to \$40 due to popularity." Does this fit LPP?  
   *Answer:* **No**, it violates the **Proportionality / Linearity** assumption.
3. **Puzzle 3:** Can an LPP have two simultaneous objectives: "Maximize profit AND Minimize employee fatigue"?  
   *Answer:* **No**, standard LPP requires a **Single Objective**. Multi-objective requires Goal Programming.

---

### 5. Practice Questions (Self-Attempt)
* **Q1.1.1:** A farmer feeds cows using Feed X (\$2/kg) and Feed Y (\$3/kg). Feed X contains 3 units of protein and 1 unit of fat per kg. Feed Y contains 2 units of protein and 4 units of fat per kg. The cow needs at least 12 units of protein and 8 units of fat daily. Formulate the LPP to minimize feeding cost.  
  *Solution Check:* $\text{Min } Z = 2x_1 + 3x_2$ subject to $3x_1 + 2x_2 \ge 12$, $x_1 + 4x_2 \ge 8$, $x_1, x_2 \ge 0$.

---

## 🔹 MICRO-TOPIC 1.2: Graphical Method for 2-Variable LPPs

### 1. Core Theory & Algorithm
* **Applicability**: Only problems with **exactly 2 decision variables** ($x_1, x_2$).
* **Algorithm Steps**:
  1. Treat all inequalities as linear equations ($=$) and plot them on the Cartesian plane $(x_1, x_2)$.
  2. Determine the valid half-plane for each constraint by testing the origin $(0,0)$.
     - If $(0,0)$ satisfies $a_{i1}(0) + a_{i2}(0) \le b_i$, shade the side containing $(0,0)$.
  3. Identify the **Feasible Region** (the convex intersection of all shaded half-planes in the first quadrant $x_1 \ge 0, x_2 \ge 0$).
  4. Find coordinates of all **Extreme Points (Vertices / Corner Points)** of the feasible polygon.
  5. Evaluate the objective function $Z$ at every corner point.
  6. The point giving the highest $Z$ (for Max) or lowest $Z$ (for Min) is the **Optimal Solution**.

---

### 2. The 4 Special Cases in Graphical Solutions
```
1. UNIQUE OPTIMAL          2. MULTIPLE OPTIMAL         3. UNBOUNDED REGION          4. INFEASIBLE REGION
   ▲                          ▲                           ▲                            ▲
   │   /───\                  │   /════\ (Parallel)       │   /                        │   ░░ (Region 1)
   │  /     \                 │  /      \                 │  / ░░░░░ (Open             │
   │ /   *   \                │ /   *    *                │ /  ░░░░░  to infinity)     │      ░░ (Region 2)
   └──────────►               └──────────►                └──────────►                 └──────────►
   Single Best Vertex         Infinite points on edge     Z -> Infinity                No Overlap
```

* **Unique Optimum**: Exactly one vertex maximizes/minimizes $Z$.
* **Alternative / Infinite Multiple Optima**:
  - *Mathematical Condition*: The slope of the objective function is identical to the slope of a binding boundary constraint:
    $$\text{Slope of } Z = -\frac{c_1}{c_2} = -\frac{a_{k1}}{a_{k2}} = \text{Slope of Constraint } k$$
  - *Result*: Every point on the line segment connecting the two optimal vertices gives the exact same optimal value of $Z$.
* **Unbounded Solution**:
  - *Condition*: The feasible region is open/unbounded in the direction of optimization, allowing $Z \to \infty$.
* **Infeasible Solution (No Feasible Region)**:
  - *Condition*: The intersection of all constraint half-spaces is the empty set $\emptyset$ (e.g. $x_1 + x_2 \le 2$ and $x_1 + x_2 \ge 5$).

---

### 3. Fully Worked Graphical Example
> **Solve Graphically:**  
> $\text{Maximize } Z = 6x_1 + 4x_2$  
> Subject to:  
> $2x_1 + 3x_2 \le 30$  
> $3x_1 + 2x_2 \le 24$  
> $x_1 + x_2 \ge 3$  
> $x_1, x_2 \ge 0$

* **Step 1: Find Line Intercepts**:
  - Line 1 ($2x_1 + 3x_2 = 30$): When $x_1=0 \implies x_2=10$ $(0,10)$; when $x_2=0 \implies x_1=15$ $(15,0)$.
  - Line 2 ($3x_1 + 2x_2 = 24$): When $x_1=0 \implies x_2=12$ $(0,12)$; when $x_2=0 \implies x_1=8$ $(8,0)$.
  - Line 3 ($x_1 + x_2 = 3$): Intercepts at $(0,3)$ and $(3,0)$.
* **Step 2: Determine Intersection of Binding Lines (1 & 2)**:
  $$\begin{cases} 2x_1 + 3x_2 = 30 \quad (\times 2) \implies 4x_1 + 6x_2 = 60 \\ 3x_1 + 2x_2 = 24 \quad (\times 3) \implies 9x_1 + 6x_2 = 72 \end{cases}$$
  Subtracting: $5x_1 = 12 \implies x_1 = 2.4 \implies x_2 = 8.4$. Corner point: $(2.4, 8.4) = \left(\frac{12}{5}, \frac{42}{5}\right)$.
* **Step 3: List All Feasible Region Vertices**:
  1. $A(3, 0)$
  2. $B(8, 0)$
  3. $C(2.4, 8.4)$
  4. $D(0, 10)$
  5. $E(0, 3)$
* **Step 4: Evaluate $Z = 6x_1 + 4x_2$ at each vertex**:
  - At $A(3, 0)$: $Z = 6(3) + 4(0) = 18$
  - At $B(8, 0)$: $Z = 6(8) + 4(0) = 48$
  - At $C(2.4, 8.4)$: $Z = 6(2.4) + 4(8.4) = 14.4 + 33.6 = 48$
  - At $D(0, 10)$: $Z = 6(0) + 4(10) = 40$
  - At $E(0, 3)$: $Z = 6(0) + 4(3) = 12$
* **Conclusion**:
  - Maximum value $Z^* = 48$ occurs at **both** $B(8, 0)$ and $C(2.4, 8.4)$.
  - *Phenomenon*: **Infinite / Multiple Optimal Solutions** exist along the entire line segment connecting $(8, 0)$ and $(2.4, 8.4)$.

---

### 4. ⚡ Zero-Pen Oral Puzzles
1. **Puzzle 1:** Objective is $\text{Max } Z = 4x_1 + 6x_2$. Constraint is $2x_1 + 3x_2 \le 12$. Without plotting, does this problem have multiple optimal solutions?  
   *Answer:* **Yes!** Notice that $\text{Slope of } Z = -\frac{4}{6} = -\frac{2}{3}$, which is identical to $\text{Slope of constraint} = -\frac{2}{3}$.
2. **Puzzle 2:** If the feasible region has corner points $(0,0), (5,0), (0,6)$, what is the maximum of $Z = 2x_1 + 3x_2$?  
   *Answer:* At $(0,0) \to 0$, at $(5,0) \to 10$, at $(0,6) \to 18$. Maximum is **$18$** at $(0,6)$.

---

## 🔹 MICRO-TOPIC 1.3: Standard Simplex Method (All $\le$ Constraints)

### 1. Canonical & Standard Form
* If all constraints are $\sum a_{ij} x_j \le b_i$ with $b_i \ge 0$:
  - Add a non-negative **Slack Variable** $S_i \ge 0$ to each constraint:
    $$a_{i1}x_1 + a_{i2}x_2 + \dots + a_{in}x_n + S_i = b_i$$
  - Objective Function: $\text{Max } Z = \sum c_j x_j + \sum 0 \cdot S_i$.
  - Initial Basis: All slack variables $S_1, S_2, \dots, S_m$ form the starting identity basis matrix $I_m$.

---

### 2. Simplex Tableau Anatomy & Step-by-Step Algorithm
```
┌─────────┬────────┬────────┬──────────────────────────┬─────────────┐
│  Basis  │  C_B   │  X_B   │  x_1   x_2  ...  S_1 S_2 │  Min Ratio  │
├─────────┼────────┼────────┼──────────────────────────┼─────────────┤
│   S_1   │   0    │  b_1   │  a_11 a_12 ...    1   0  │  b_1 / a_1k │
│   S_2   │   0    │  b_2   │  a_21 a_22 ...    0   1  │  b_2 / a_2k │
├─────────┴────────┼────────┼──────────────────────────┴─────────────┤
│        Z_j       │   Z    │  Z_1   Z_2  ...  Z_s1 Z_s2         │
├──────────────────┴────────┼────────────────────────────────────────┤
│     C_j - Z_j (Δ_j)       │  Δ_1   Δ_2  ...  Δ_s1 Δ_s2         │
└───────────────────────────┴────────────────────────────────────────┘
```

* **Step 1: Compute Row $Z_j$**:
  $$Z_j = \sum_{i=1}^m C_{Bi} \cdot a_{ij}$$
* **Step 2: Compute Net Evaluation Row (Indicator Row) $\Delta_j = C_j - Z_j$**:
  $$\Delta_j = C_j - Z_j$$
* **Step 3: Optimality Test (for Maximization)**:
  - If **all $\Delta_j = C_j - Z_j \le 0$**, current tableau is **OPTIMAL**. Stop!
  - If any $C_j - Z_j > 0$, proceed to pivot.
* **Step 4: Select Entering Variable (Key Column)**:
  $$\text{Key Column } k = \operatorname{argmax}_j (C_j - Z_j) \quad \text{(Most positive value)}$$
* **Step 5: Select Leaving Variable (Key Row) via Minimum Ratio Rule**:
  $$\text{Key Row } r = \operatorname{argmin}_i \left\{ \frac{X_{Bi}}{a_{ik}} : a_{ik} > 0 \right\}$$
  *(Ignore $a_{ik} \le 0$ and division by zero!)*
* **Step 6: Identify Key / Pivot Element ($p = a_{rk}$)**: Intersection of key row and key column.
* **Step 7: Gaussian Row Operations for Next Tableau**:
  $$\text{New Key Row } R_r^{(new)} = \frac{R_r^{(old)}}{p}$$
  $$\text{Other Rows } R_i^{(new)} = R_i^{(old)} - a_{ik} \cdot R_r^{(new)}$$

---

### 3. Fully Worked Simplex Example
> **Solve via Simplex Method:**  
> $\text{Maximize } Z = 3x_1 + 5x_2 + 4x_3$  
> Subject to:  
> $2x_1 + 3x_2 \le 8$  
> $2x_2 + 5x_3 \le 10$  
> $3x_1 + 2x_2 + 4x_3 \le 15$  
> $x_1, x_2, x_3 \ge 0$

#### Converting to Standard Form:
$$\text{Max } Z = 3x_1 + 5x_2 + 4x_3 + 0S_1 + 0S_2 + 0S_3$$
Subject to:
$$\begin{aligned}
2x_1 + 3x_2 + 0x_3 + S_1 &= 8 \\
0x_1 + 2x_2 + 5x_3 + S_2 &= 10 \\
3x_1 + 2x_2 + 4x_3 + S_3 &= 15
\end{aligned}$$

#### Iteration 1:
| Basis | $C_B$ | $X_B$ | $x_1 (3)$ | $x_2 (5)$ | $x_3 (4)$ | $S_1 (0)$ | $S_2 (0)$ | $S_3 (0)$ | Min Ratio $\theta = X_B / x_2$ |
|---|---|---|---|---|---|---|---|---|---|
| $S_1$ | 0 | 8 | 2 | **(3)** | 0 | 1 | 0 | 0 | $8/3 = 2.67 \to$ **Leaving Row ($S_1$)** |
| $S_2$ | 0 | 10 | 0 | 2 | 5 | 0 | 1 | 0 | $10/2 = 5$ |
| $S_3$ | 0 | 15 | 3 | 2 | 4 | 0 | 0 | 1 | $15/2 = 7.5$ |
| **$Z_j$** | | 0 | 0 | 0 | 0 | 0 | 0 | 0 | |
| **$C_j - Z_j$** | | | 3 | **5 $\uparrow$** | 4 | 0 | 0 | 0 | Key Column = $x_2$ |

* Pivot element = **3** (Row 1, Col 2).
* Row operations: $R_1' = R_1 / 3$; $R_2' = R_2 - 2R_1'$; $R_3' = R_3 - 2R_1'$.

#### Iteration 2:
| Basis | $C_B$ | $X_B$ | $x_1$ | $x_2$ | $x_3$ | $S_1$ | $S_2$ | $S_3$ | Min Ratio $\theta = X_B / x_3$ |
|---|---|---|---|---|---|---|---|---|---|
| $x_2$ | 5 | $8/3$ | $2/3$ | 1 | 0 | $1/3$ | 0 | 0 | — |
| $S_2$ | 0 | $14/3$ | $-4/3$ | 0 | **(5)** | $-2/3$ | 1 | 0 | $\frac{14/3}{5} = 0.93 \to$ **Leaving Row ($S_2$)** |
| $S_3$ | 0 | $29/3$ | $5/3$ | 0 | 4 | $-2/3$ | 0 | 1 | $\frac{29/3}{4} = 2.42$ |
| **$Z_j$** | | $40/3$ | $10/3$ | 5 | 0 | $5/3$ | 0 | 0 | |
| **$C_j - Z_j$** | | | $-1/3$ | 0 | **4 $\uparrow$** | $-5/3$ | 0 | 0 | Key Column = $x_3$ |

* Pivot element = **5** (Row 2, Col 3).
* Row operations: $R_2'' = R_2' / 5$; $R_1'' = R_1'$; $R_3'' = R_3' - 4R_2''$.

#### Iteration 3:
| Basis | $C_B$ | $X_B$ | $x_1$ | $x_2$ | $x_3$ | $S_1$ | $S_2$ | $S_3$ | Min Ratio $\theta = X_B / x_1$ |
|---|---|---|---|---|---|---|---|---|---|
| $x_2$ | 5 | $8/3$ | $2/3$ | 1 | 0 | $1/3$ | 0 | 0 | $\frac{8/3}{2/3} = 4$ |
| $x_3$ | 4 | $14/15$ | $-4/15$ | 0 | 1 | $-2/15$ | $1/5$ | 0 | — ($a_{ik} < 0$) |
| $S_3$ | 0 | $89/15$ | **(41/15)**| 0 | 0 | $-2/15$ | $-4/5$| 1 | $\frac{89/15}{41/15} = 2.17 \to$ **Leaving Row ($S_3$)** |
| **$Z_j$** | | $256/15$| $34/15$| 5 | 4 | $17/15$ | $4/5$ | 0 | |
| **$C_j - Z_j$** | | | **11/15 $\uparrow$**| 0 | 0 | $-17/15$| $-4/5$| 0 | Key Column = $x_1$ |

* Pivot element = **41/15** (Row 3, Col 1).

#### Iteration 4 (Final Optimal Table):
| Basis | $C_B$ | $X_B$ | $x_1$ | $x_2$ | $x_3$ | $S_1$ | $S_2$ | $S_3$ |
|---|---|---|---|---|---|---|---|---|
| $x_2$ | 5 | $50/41$ | 0 | 1 | 0 | $15/41$ | $8/41$ | $-10/41$ |
| $x_3$ | 4 | $62/41$ | 0 | 0 | 1 | $-6/41$ | $5/41$ | $4/41$ |
| $x_1$ | 3 | $89/41$ | 1 | 0 | 0 | $-2/41$ | $-12/41$| $15/41$ |
| **$Z_j$** | | $765/41$| 3 | 5 | 4 | $45/41$ | $24/41$| $11/41$ |
| **$C_j - Z_j$** | | | 0 | 0 | 0 | **-45/41**| **-24/41**| **-11/41** |

* Since all $C_j - Z_j \le 0$, the solution is **OPTIMAL**.
* **Final Result**:
  $$x_1^* = \frac{89}{41}, \quad x_2^* = \frac{50}{41}, \quad x_3^* = \frac{62}{41}, \quad \text{Max } Z^* = \frac{765}{41}$$

---

### 4. ⚡ Zero-Pen Oral Puzzles
1. **Puzzle 1:** In a simplex table for $\text{Max } Z$, $C_j - Z_j$ row is $[0, -3, 5, 0, -1]$. Which variable MUST enter the basis?  
   *Answer:* The variable corresponding to **$+5$** (the most positive value).
2. **Puzzle 2:** In the key column, the values in the constraint rows are $[-2, 0, -5]$. What does this immediately tell you about the problem?  
   *Answer:* The solution is **UNBOUNDED** ($Z \to \infty$) because no positive ratio can be computed to determine a leaving variable!
3. **Puzzle 3:** In the final optimal table, all basic variables have $C_j - Z_j = 0$, but a **non-basic** variable $x_4$ also has $C_4 - Z_4 = 0$. What does this mean?  
   *Answer:* There are **Alternative / Multiple Optimal Solutions**.

---

## 🔹 MICRO-TOPIC 1.4: Big-M (Penalty Cost) Method

### 1. Why Big-M is Needed
When constraints have $\ge$ or $=$ signs, slack variables cannot form an initial starting identity matrix because:
- Constraint $a x \ge b \implies ax - S + A = b$. The surplus variable $-S$ has coefficient $-1$ (cannot be in starting basis).
- Therefore, a non-negative **Artificial Variable ($A_i \ge 0$)** is added to serve as an initial basic variable.
- To guarantee that artificial variables leave the basis and do not appear in the final physical solution, they are assigned an immense **penalty cost $M$**:
  - In **Maximization**: Objective receives **$-M \cdot A_i$**
  - In **Minimization**: Objective receives **$+M \cdot A_i$** ($M > 0, M \to \infty$)

---

### 2. Big-M Transformation Rules Table
| Constraint Sign | Variable Transformations | Coeff in Max $Z$ | Coeff in Min $Z$ | Initial Basic Variable |
|---|---|---|---|---|
| $\le$ | $+ S_i$ (Slack) | $+ 0 S_i$ | $+ 0 S_i$ | $S_i$ |
| $\ge$ | $- S_i$ (Surplus) $+ A_i$ (Artificial) | $+ 0 S_i - M A_i$ | $+ 0 S_i + M A_i$ | $A_i$ |
| $=$ | $+ A_i$ (Artificial) | $- M A_i$ | $+ M A_i$ | $A_i$ |

---

### 3. Identifying the 3 Key Outcomes in Big-M Table
1. **Case 1: Standard Optimal Solution**:
   - All $C_j - Z_j \le 0$ (for Max) and **no artificial variable $A_i$ is in the basis** (or $A_i = 0$).
2. **Case 2: Infeasible Solution (Crucial Exam Test)**:
   - Optimality condition is satisfied (all $C_j - Z_j \le 0$), **BUT at least one artificial variable $A_k$ remains in the basis with a strictly positive value ($X_{Bk} > 0$)**.
   - *Meaning*: Original constraints are contradictory; no feasible region exists.
3. **Case 3: Degeneracy & Tie in Leaving Variable**:
   - When minimum ratios tie between a regular variable and an artificial variable, **always drop the artificial variable first** to clean up the tableau faster!

---

### 4. Fully Worked Big-M Examples

#### Example A: Detecting Infeasible Solution
> **Solve via Big-M:**  
> $\text{Max } Z = 6x_1 + 4x_2$  
> Subject to:  
> $x_1 + x_2 \le 5$  
> $x_2 \ge 8$  
> $x_1, x_2 \ge 0$

1. **Standard Form**:
   $$\text{Max } Z = 6x_1 + 4x_2 + 0S_1 + 0S_2 - M A_1$$
   $$\begin{aligned} x_1 + x_2 + S_1 &= 5 \\ x_2 - S_2 + A_1 &= 8 \end{aligned}$$
2. **Iteration 1**:
   | Basis | $C_B$ | $X_B$ | $x_1 (6)$ | $x_2 (4)$ | $S_1 (0)$ | $S_2 (0)$ | $A_1 (-M)$ | Min Ratio $\theta$ |
   |---|---|---|---|---|---|---|---|---|
   | $S_1$ | 0 | 5 | 1 | **(1)** | 1 | 0 | 0 | $5/1 = 5 \to$ Leaves |
   | $A_1$ | $-M$ | 8 | 0 | 1 | 0 | $-1$ | 1 | $8/1 = 8$ |
   | $Z_j$ | | $-8M$ | 0 | $-M$ | 0 | $M$ | $-M$ | |
   | $C_j - Z_j$ | | | 6 | **M + 4 $\uparrow$**| 0 | $-M$ | 0 | Key Col = $x_2$ |

   * Pivot element = 1 (Row 1, Col 2). $S_1$ leaves, $x_2$ enters.
3. **Iteration 2**:
   | Basis | $C_B$ | $X_B$ | $x_1 (6)$ | $x_2 (4)$ | $S_1 (0)$ | $S_2 (0)$ | $A_1 (-M)$ |
   |---|---|---|---|---|---|---|---|
   | $x_2$ | 4 | 5 | 1 | 1 | 1 | 0 | 0 |
   | $A_1$ | $-M$ | 3 | $-1$ | 0 | $-1$ | $-1$ | 1 |
   | $Z_j$ | | $20 - 3M$ | $M + 4$ | 4 | $M + 4$ | $M$ | $-M$ |
   | $C_j - Z_j$ | | | **-M + 2** | 0 | **-M - 4** | **-M** | 0 |

4. **Conclusion**:
   - Since $M \to +\infty$, all $C_j - Z_j$ values ($-M+2, -M-4, -M$) are strictly negative ($\le 0$).
   - Optimality condition is satisfied, but **$A_1$ remains in the basis with positive value $X_B = 3$**.
   - Therefore, the problem is **INFEASIBLE (No Feasible Solution)**!

---

## 🔹 MICRO-TOPIC 1.5: Two-Phase Simplex Method

### 1. Why Two-Phase is Preferred in Computer Implementations
Handling the symbolic constant $M$ manually in pencil-paper calculations is error-prone. The **Two-Phase Method** eliminates $M$ by solving two consecutive, standard simplex problems.

---

### 2. The Two Phases Explained
* **Phase I (Eliminate Artificial Variables)**:
  - Formulate an auxiliary objective function:
    $$\text{Minimize } W = \sum A_i \quad \iff \quad \text{Maximize } W^* = -\sum A_i$$
  - Assign cost $0$ to all real variables ($x_j$) and slack/surplus variables ($S_i$).
  - Solve using standard Simplex.
  - **Outcome check at end of Phase I**:
    - If $\text{Max } W^* < 0$ (i.e. $\min W > 0$ with artificial variables still $>0$): **STOP! Problem is INFEASIBLE**.
    - If $\text{Max } W^* = 0$ (all artificial variables driven to $0$): **Proceed to Phase II**.
* **Phase II (Find True Optimal Solution)**:
  - Drop all artificial variable columns ($A_i$) completely from the tableau.
  - Restore original objective coefficients $c_j$ into the $C_j$ row.
  - Compute new $Z_j$ and $C_j - Z_j$ using original costs.
  - Continue simplex pivoting until all $C_j - Z_j \le 0$.

---

### 3. ⚡ Zero-Pen Oral Puzzles
1. **Puzzle 1:** In Phase I of Two-Phase method, what are the objective function coefficients for the original decision variables $x_1, x_2$?  
   *Answer:* Exactly **0**.
2. **Puzzle 2:** If Phase I finishes with optimal value $W^* = -2$, what does that imply?  
   *Answer:* The problem has **NO FEASIBLE SOLUTION (Infeasible)**.

---

# 🚚 MODULE 2: TRANSPORTATION, ASSIGNMENT & SEQUENCING (10 HOURS)

---

## 🔹 MICRO-TOPIC 2.1: Transportation Problem (TP)

### 1. Mathematical Structure & Balance Condition
$$\text{Minimize } Z = \sum_{i=1}^m \sum_{j=1}^n c_{ij} x_{ij}$$
Subject to:
$$\sum_{j=1}^n x_{ij} = a_i \quad (\text{Supply from origin } i), \quad \sum_{i=1}^m x_{ij} = b_j \quad (\text{Demand at destination } j)$$
* **Balanced Condition**: $\sum_{i=1}^m a_i = \sum_{j=1}^n b_j$.
* **Unbalanced Resolution**:
  - If $\sum a_i > \sum b_j$: Add a **Dummy Destination** with demand $\sum a_i - \sum b_j$ and cost $c_{i, \text{dummy}} = 0$.
  - If $\sum b_j > \sum a_i$: Add a **Dummy Origin** with supply $\sum b_j - \sum a_i$ and cost $c_{\text{dummy}, j} = 0$.
* **Maximization TP**: Convert profit matrix to opportunity loss matrix:
  $$c'_{ij} = (\text{Maximum entry in profit matrix}) - c_{ij}$$

---

### 2. Step 1: Three Methods for Initial Basic Feasible Solution (IBFS)

```
             ┌─────────────────────────────────────────────────────────┐
             │       METHODS TO FIND INITIAL BASIC FEASIBLE SOLUTION   │
             └────────────────────────────┬────────────────────────────┘
                                          │
        ┌─────────────────────────────────┼─────────────────────────────────┐
        │                                 │                                 │
  ▼───────────▼                     ▼───────────▼                     ▼───────────▼
  1. NORTH-WEST CORNER (NWCR)       2. LEAST COST METHOD (LCM)        3. VOGEL'S APPROXIMATION (VAM)
  • Pure geometric top-left         • Greedily allocates to cell with • Calculates penalties (diff of
  • Completely ignores cost matrix    minimum unit cost min(c_ij)       two lowest costs in row/col)
  • Fastest, but worst initial cost • Better than NWCR                • Best & closest to optimality
```

---

### 3. Step 2: Optimality Test — MODI (Modified Distribution / $u-v$) Method

* **Non-Degeneracy Condition**:
  An initial solution is non-degenerate if:
  $$\text{Number of allocated cells} = m + n - 1$$
  *(If $< m + n - 1$, problem is **Degenerate**. Fix by allocating an infinitesimal quantity $\epsilon > 0$ to an unallocated cell that does not form a closed loop).*

* **MODI Algorithm Steps**:
  1. Set $u_1 = 0$ (or the row/col with the highest number of allocations).
  2. For every **allocated cell $(i,j)$**, solve:
     $$u_i + v_j = c_{ij}$$
  3. For every **unallocated cell $(i,j)$**, compute Net Evaluation (Opportunity Cost):
     $$\Delta_{ij} = c_{ij} - (u_i + v_j)$$
  4. **Optimality Check**:
     - If all $\Delta_{ij} \ge 0$: Current solution is **OPTIMAL**.
     - If any $\Delta_{ij} < 0$: Solution can be improved.
  5. **Closed Loop Reallocation**:
     - Select unallocated cell with the **most negative $\Delta_{ij}$** as the entering cell $(+\theta)$.
     - Draw a closed loop containing horizontal and vertical lines connecting only allocated cells at right-angle corners.
     - Alternate signs: $+\theta, -\theta, +\theta, -\theta$ along the loop corners.
     - Determine maximum transferable quantity:
       $$\theta = \min \{ \text{Allocations at corners with } -\theta \}$$
     - Add $\theta$ to positive corners and subtract $\theta$ from negative corners.
     - Re-test with MODI until all $\Delta_{ij} \ge 0$.

---

### 4. ⚡ Zero-Pen Oral Puzzles
1. **Puzzle 1:** In a transportation problem with 4 origins and 5 destinations, how many basic allocations MUST be present to apply the MODI method?  
   *Answer:* $m + n - 1 = 4 + 5 - 1 = \mathbf{8}$ **allocations**.
2. **Puzzle 2:** In MODI test, all empty cells have $\Delta_{ij} \ge 0$, and one empty cell has $\Delta_{23} = 0$. What does this mean?  
   *Answer:* The solution is optimal, but **Alternative Optimal Solutions** exist!
3. **Puzzle 3:** If total supply is 100 and total demand is 85, what must you do before applying VAM?  
   *Answer:* Add a **Dummy Destination** with demand of **15** and unit transportation costs of **0**.

---

## 🔹 MICRO-TOPIC 2.2: Assignment Problem (AP) & Hungarian Algorithm

### 1. Mathematical Formulation & Distinction from Transportation
* Special case of TP where $m = n$, supply $a_i = 1$, demand $b_j = 1$, and $x_{ij} \in \{0, 1\}$.
* **Objective**: Assign exactly 1 person to 1 job to minimize total cost.

---

### 2. Hungarian Algorithm (Flood's Technique) Step-by-Step
1. **Square Matrix Check**: If rows $\ne$ columns, add dummy row/column with zeros.
2. **Row Reduction**: Subtract the minimum element of each row from every element in that row.
3. **Column Reduction**: Subtract the minimum element of each column from every element in that column.
4. **Line Covering**: Draw the **minimum number of straight horizontal and vertical lines ($L$)** to cover all zeros in the matrix.
   - If **$L = n$** (where $n$ is matrix size): **Optimal assignment is reached!** Jump to Step 6.
   - If **$L < n$**: Proceed to Step 5.
5. **Matrix Modification**:
   - Find the smallest uncovered element $k = \min(\text{uncovered elements})$.
   - **Subtract $k$** from all uncovered elements.
   - **Add $k$** to elements at the intersections of two lines.
   - **Leave unchanged** elements covered by a single line.
   - Return to Step 4.
6. **Zero Assignment**:
   - Find a row with exactly one zero $\to$ box that zero $[0]$ and cross out $(\times)$ any other zeros in its column.
   - Find a column with exactly one zero $\to$ box that zero $[0]$ and cross out $(\times)$ any other zeros in its row.
   - Repeat until each row and column has exactly one boxed zero.

---

### 3. Special Assignment Cases
* **Maximization Assignment**: Convert by subtracting all matrix values from the maximum value in the matrix: $c'_{ij} = \max(c) - c_{ij}$, then run standard Hungarian.
* **Prohibited / Restricted Assignment**: Put $c_{ij} = \infty$ or $M$ for forbidden cells.
* **Travelling Salesperson Problem (TSP)**:
  - Diagonal $c_{ii} = \infty$ (cannot travel to self).
  - Solve via Hungarian algorithm.
  - Verify that the assignments form a **single Hamiltonian cycle** ($1 \to 3 \to 4 \to 2 \to 1$).
  - If sub-tours occur (e.g. $1 \to 2 \to 1$ and $3 \to 4 \to 3$), branch and force the next smallest non-zero cell to break the cycle.

---

### 4. Fully Worked Hungarian Algorithm Example
> **Assign 4 Workers ($A, B, C, D$) to 4 Jobs ($1, 2, 3, 4$) with cost matrix:**
> $$\begin{pmatrix} 10 & 12 & 19 & 11 \\ 5 & 10 & 7 & 8 \\ 12 & 14 & 13 & 11 \\ 8 & 15 & 11 & 9 \end{pmatrix}$$

* **Step 1: Row Reduction**:
  - Row 1 (min 10): $[0, 2, 9, 1]$
  - Row 2 (min 5): $[0, 5, 2, 3]$
  - Row 3 (min 11): $[1, 3, 2, 0]$
  - Row 4 (min 8): $[0, 7, 3, 1]$
* **Step 2: Column Reduction**:
  - Col 1 (min 0): $[0, 0, 1, 0]^T$
  - Col 2 (min 2): $[0, 3, 1, 5]^T$
  - Col 3 (min 2): $[7, 0, 0, 1]^T$
  - Col 4 (min 0): $[1, 3, 0, 1]^T$
* Reduced Matrix:
  $$\begin{pmatrix} 0 & 0 & 7 & 1 \\ 0 & 3 & 0 & 3 \\ 1 & 1 & 0 & 0 \\ 0 & 5 & 1 & 1 \end{pmatrix}$$
* **Step 3: Minimum Line Covering**:
  - Line 1: Col 1 covers $(1,1), (2,1), (4,1)$.
  - Line 2: Row 3 covers $(3,3), (3,4)$.
  - Line 3: Row 1 covers $(1,2)$.
  - Line 4: Row 2 covers $(2,3)$.
  - Total lines $L = 4 = n$. Optimal reached!
* **Step 4: Optimal Assignment**:
  - Row 4 has single zero at Col 1 $\implies$ **$D \to 1$** (Cost = 8).
  - Row 1: zero at Col 2 $\implies$ **$A \to 2$** (Cost = 12).
  - Row 2: zero at Col 3 $\implies$ **$B \to 3$** (Cost = 7).
  - Row 3: zero at Col 4 $\implies$ **$C \to 4$** (Cost = 11).
  - **Total Minimum Cost** = $8 + 12 + 7 + 11 = \mathbf{38}$.

---

### 5. ⚡ Zero-Pen Oral Puzzles
1. **Puzzle 1:** In a Hungarian problem, you have 3 lines covering all zeros in a $4 \times 4$ matrix. The smallest uncovered element is $2$. What do you add to the intersection elements?  
   *Answer:* You add **$+2$**.
2. **Puzzle 2:** If you have 5 jobs and 4 workers, what must you add to make the Hungarian method work?  
   *Answer:* A **Dummy Worker (Dummy Row)** with all costs equal to **0**.

---

## 🔹 MICRO-TOPIC 2.3: Sequencing Problems & Job Scheduling

### 1. Assumptions of Sequencing
- Operation times are known and fixed.
- No job passing (first come first processed order maintained across stages).
- Only one operation per machine at a time.

---

### 2. Subtype 2.3.A: $n$ Jobs on 2 Machines ($A \to B$) — Johnson's Rule
* **Algorithm**:
  1. Find the smallest processing time among all remaining jobs on Machine $A$ and $B$.
  2. If the minimum time is on **Machine $A$**: Place that job **FIRST (from left)**.
  3. If the minimum time is on **Machine $B$**: Place that job **LAST (from right)**.
  4. Cross off the scheduled job and repeat.
  5. *Tie breaking*: If tie on same machine, pick arbitrarily; if tie between $A$ and $B$, put $A$ job first and $B$ job last.
* **In-Out Table & Gantt Chart Construction**:
  $$\text{Total Elapsed Time } T = \text{Out time of last job on Machine } B$$
  $$\text{Idle Time of Machine } A = T - \sum A_i$$
  $$\text{Idle Time of Machine } B = \text{In time of 1st job on } B + \sum \max(0, \text{In}_{B} - \text{Out}_{prev B})$$

---

### 3. Subtype 2.3.B: $n$ Jobs on 3 Machines ($A \to B \to C$)
* **Condition for Applicability of Johnson's Rule**:
  $$\min(A_i) \ge \max(B_i) \quad \text{OR} \quad \min(C_i) \ge \max(B_i)$$
* If condition holds, create two fictitious machines $G$ and $H$:
  $$G_i = A_i + B_i, \quad H_i = B_i + C_i$$
* Apply standard 2-machine Johnson's rule on $G$ and $H$.

---

### 4. Subtype 2.3.C: 2 Jobs on $m$ Machines (Graphical Method)
```
  Job 2 (Y-axis)
  ▲
  │   ┌────────┐
  │   │CONFLICT│ (Machine M2)
  │   │  ZONE  │
  │   └────────┘   / 45° Diagonal Movement (Both jobs working simultaneously)
  │               /
  │              /── Horizontal (Job 1 working, Job 2 idle)
  │             /│
  │            / │ Vertical (Job 2 working, Job 1 idle)
  └───────────┴──┴──────────────► Job 1 (X-axis)
```
* **Steps**:
  1. Represent Job 1 processing times along $X$-axis and Job 2 along $Y$-axis according to their machine sequences.
  2. Draw shaded rectangular **Conflict Regions** where both jobs require the same machine.
  3. Draw path from $(0,0)$ to $(T_1, T_2)$ moving horizontally, vertically, or at **$45^\circ$ diagonally**.
  4. Avoid entering the conflict blocks.
  5. Makespan = $T_1 + (\text{Total Vertical idle segments}) = T_2 + (\text{Total Horizontal idle segments})$.

---

### 5. ⚡ Zero-Pen Oral Puzzles
1. **Puzzle 1:** In Johnson's 2-machine rule, Job 3 has processing time 1 hr on Machine B, which is the absolute minimum in the entire table. Where should Job 3 be placed in the sequence?  
   *Answer:* At the **very end (last position)**.
2. **Puzzle 2:** For a 3-machine problem ($A, B, C$), $\min(A) = 4, \max(B) = 6, \min(C) = 7$. Can we convert it to a 2-machine problem?  
   *Answer:* **Yes!** Because $\min(C) = 7 \ge \max(B) = 6$ satisfies the condition.

---

# 🌐 COMPLETE INTERACTIVE WEB APPLICATION CODEBLUEPRINT

The platform will include:
1. **Linear Programming Visualizer**:
   - 2D Canvas plotting constraints, polygon vertices, and animated isocost line.
   - Interactive Simplex & Big-M stepping engine with live pivot highlights.
2. **Transportation & Hungarian Solver**:
   - Automated VAM penalty calculator and visual MODI closed-loop animation.
   - Hungarian matrix reduction tool with zero-covering lines.
3. **Sequencing & Gantt Chart Generator**:
   - Interactive In-Out time generator and 2-Job $m$-machine graphical grid.
4. **Gamified Oral Puzzle Arena**:
   - Instant conceptual flashcards and quizzes categorized by topic with zero-paper mental reasoning.
