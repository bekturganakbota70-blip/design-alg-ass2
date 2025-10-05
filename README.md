# design-alg-ass2
Insertion Sort Algorithm – Assignment 2

This project implements the Insertion Sort algorithm in Java with an optimization for nearly sorted arrays.
It includes performance measurement, CSV export, and a CLI benchmark runner for empirical analysis.

#✅ Features

Insertion Sort implementation (in-place, stable)

Early termination optimization for nearly sorted data

CLI benchmark runner (time & operations tracking)

JUnit 5 test suite covering all edge cases

CSV export for performance results

Plot-ready data for analysis reports

#📦 Project Structure

<img width="449" height="575" alt="Снимок экрана 2025-10-05 143334" src="https://github.com/user-attachments/assets/17209c20-5dfe-4f98-83a0-e0aa2503b435" />


⚙️ Build & Test

Requirements:

Java 17+

Maven 3.9+

Setup and run:


# Run all unit tests
mvn clean test

#🚀 Run Benchmark

You can run performance benchmarks using the CLI runner:

mvn compile
java -cp target/classes cli.BenchmarkRunner


#Example output:

n=100 | time=0,078 ms | comparisons=2688 | swaps=2592
n=1000 | time=2,441 ms | comparisons=252558 | swaps=251567
n=10000 | time=24,919 ms | comparisons=25038444 | swaps=25028457


Results are automatically saved to:

benchmark_results.csv

#📊 Example Output (CSV)
n,time_ms,comparisons,swaps
100,0.0918,2833,2742
1000,8.5459,253893,252903
10000,37.0416,24772048,24762054
n,time_ms,comparisons,swaps
100,0.1051,2467,2370
1000,12.5802,248193,247202
10000,165.3997,25010494,25000503

#🧮 Complexity Analysis
Case	Time Complexity	Space Complexity
Best Case (nearly sorted)	Ω(n)	O(1)
Average Case	Θ(n²)	O(1)
Worst Case (reverse order)	O(n²)	O(1)



#🧠 Conclusion

Insertion Sort is efficient for small or nearly sorted arrays.

The optimization significantly reduces operations in best-case scenarios.

The results align with the theoretical O(n²) complexity model.

Future improvements may include binary insertion or Shell Sort adaptation.
