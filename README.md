# design-alg-ass2
Insertion Sort Algorithm – Assignment 2

This project implements the Insertion Sort algorithm in Java with an optimization for nearly sorted arrays.
It includes performance measurement, CSV export, and a CLI benchmark runner for empirical analysis.

✅ Features

Insertion Sort implementation (in-place, stable)

Early termination optimization for nearly sorted data

CLI benchmark runner (time & operations tracking)

JUnit 5 test suite covering all edge cases

CSV export for performance results

Plot-ready data for analysis reports

📦 Project Structure

<img width="449" height="575" alt="Снимок экрана 2025-10-05 143334" src="https://github.com/user-attachments/assets/17209c20-5dfe-4f98-83a0-e0aa2503b435" />


⚙️ Build & Test

Requirements:

Java 17+

Maven 3.9+

Setup and run:

# Clone and enter the project
git clone https://github.com/your-username/assignment2-insertionsort
cd assignment2-insertionsort

# Run all unit tests
mvn clean test

🚀 Run Benchmark

You can run performance benchmarks using the CLI runner:

mvn compile
java -cp target/classes cli.BenchmarkRunner


Example output:

n=100 | time=0.12 ms | comparisons=4550 | swaps=2300
n=1000 | time=4.50 ms | comparisons=254890 | swaps=128340
n=10000 | time=480.75 ms | comparisons=25,000,000 | swaps=12,400,000


Results are automatically saved to:

benchmark_results.csv

📊 Example Output (CSV)
n	time_ms	comparisons	swaps
100	0.12	4550	2300
1000	4.50	254890	128340
10000	480.75	25000000	12400000
🧮 Complexity Analysis
Case	Time Complexity	Space Complexity
Best Case (nearly sorted)	Ω(n)	O(1)
Average Case	Θ(n²)	O(1)
Worst Case (reverse order)	O(n²)	O(1)

Optimization Effect:
When the array is nearly sorted, the algorithm detects order early and avoids unnecessary swaps, leading to near-linear time.

🧪 Testing

JUnit 5 tests verify correctness and edge cases:

Empty array

Single element

Already sorted

Reverse sorted

With duplicates

To run all tests:

mvn test

📈 Empirical Analysis

CSV data can be visualized using Python or Excel:

Python Example:

import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("benchmark_results.csv")
plt.plot(data["n"], data["time_ms"], marker="o")
plt.xlabel("Input Size (n)")
plt.ylabel("Time (ms)")
plt.title("Insertion Sort: Time vs Input Size")
plt.grid(True)
plt.show()


Result example:
📊 time_vs_n.png → shows quadratic growth (O(n²)).

🧾 Report (docs/analysis-report.pdf)

The report includes:

Algorithm overview

Theoretical complexity (O, Θ, Ω)

Empirical validation (graphs & CSV data)

Code review and optimization discussion

Conclusion and recommendations

🧠 Conclusion

Insertion Sort is efficient for small or nearly sorted arrays.

The optimization significantly reduces operations in best-case scenarios.

The results align with the theoretical O(n²) complexity model.

Future improvements may include binary insertion or Shell Sort adaptation.
