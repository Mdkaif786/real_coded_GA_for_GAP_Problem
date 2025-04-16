
# Real-Coded GA for Optimization and GAP Problem

This project contains two major components:
1. **Optimization of the Sphere function with 4 variables using Real-Coded GA.**
2. **Solving the Generalized Assignment Problem (GAP), specifically `gap12`, using Real-Coded GA and comparing it with Binary-Coded GA, optimal, and greedy approximations.**

---

## 📁 Project Structure

```
.
├── real_ga.ipynb                   # Jupyter notebook for Real-Coded GA implementation
├── real_ga_results.csv            # Results of Real-Coded GA runs
├── binary_ga_results.csv          # Results of Binary-Coded GA (for comparison)
├── optimal_results.csv            # Optimal values for comparison
├── greedy_results.csv             # Results from greedy approximation algorithm
for GAP12
├── gap_dataset_files/             # Contains GAP instances like gap12.txt
├── README.md
├── binary_ga_convergence_gap12
├── real_ga_convergence_gap12
├── output_comparison.png
├── gap12_real_convergence_plot.png
├── gap12_convergence_binary_vs_real.png
```

---

## 🧮 1. Sphere Function Optimization

**Objective:**
Minimize the following function using Real-Coded GA:

min f(x) = ∑ xi²  
           4  
          i=1

where, xi ∈ [−10, 10]  ∀i

**Key Features:**
- Real-number encoding for 4 decision variables.
- Fitness is based on minimizing the squared sum.
- Efficient selection, crossover, and mutation strategies implemented.

---

## 📦 2. GAP Problem (gap12)

**Problem Description:**
The Generalized Assignment Problem (GAP) involves assigning tasks to agents such that:
- Each user is assigned to exactly one server.
- The total utility is maximized.
- Server resource constraints are not violated.

This project evaluates the performance of **Real-Coded GA** in solving GAP, and compares it to:
- Binary-Coded GA
- Greedy Algorithm
- Optimal Solutions

### Dataset Format

Each `.txt` file contains:
1. Number of instances
2. For each instance:
   - Number of servers and users
   - Utility matrix (servers × users)
   - VM allocation matrix (servers × users)
   - Server capacities (list)

### Output

For each instance:
- Task Assignments (user → server)
- Total Utility Achieved

**Approach:**
- Real-number vector representation of assignments.
- Custom decoder to enforce feasibility.
- Penalty-based fitness for constraint violations.

**Comparative Analysis:**
- **Optimal Solution:** From `optimal_results.csv`
- **Greedy Approximation:** From `greedy_results.csv`
- **Binary-Coded GA:** From `binary_ga_results.csv`
- **Real-Coded GA:** From `real_ga_results.csv`

**Visualization:**
- `gap12_comparison.png`: Convergence plot of Binary-Coded GA over 100 iterations.

---

## 📊 Results & Interpretation

- **Convergence Plot**: Evaluates performance of Binary-Coded GA.
- **Comparison Tables**: Analyze performance of different algorithms on GAP12.
- **GA Settings**: Parameters such as mutation rate, population size, and crossover strategy are customizable in `real_ga.ipynb`.

---

## 📝 References

- GAP Dataset: [OR-Library GAP Instances](https://people.brunel.ac.uk/~mastjjb/jeb/orlib/gapinfo.html)
- Related Algorithms:
  - [Binary GA + ACO + BA implementations](https://github.com/acco93/GAP-using-GA-ACO-and-BA)
  - [Efficient Approximation Algorithm](https://github.com/suzhiyang/GAP)

---

## 📌 How to Run

1. Open `real_ga.ipynb` in Jupyter.
2. Execute each section to:
   - Solve the Sphere function using Real-Coded GA.
   - Load and solve GAP12 using real-coded approach.
   - View convergence and compare with other methods.

---

## ✍️ Author

**Md Kaif**  
M.Tech (CSE)  
NIT Jamshedpur  

📎 GitHub Repository: [https://github.com/Mdkaif786/binaryGA_for_GAP](https://github.com/Mdkaif786/binaryGA_for_GAP)
