Mandelbrot Set Benchmark Suite

A comprehensive Java benchmarking tool for analyzing Mandelbrot set generation performance across different parameters and configurations.
Project Structure

This project contains multiple implementations and benchmarks for Mandelbrot set generation:

    MandelbrotCPUBenchmark.java - CPU time measurement using ThreadMXBean

    MandelbrotBenchmark.java - Comprehensive benchmarking with multiple regions (commented)

    MandelbrotViewer.java - Interactive visualization tool (commented)

    USACO practice files - Additional programming challenge solutions

Features
MandelbrotCPUBenchmark

    Precise CPU Time Measurement: Uses ThreadMXBean for accurate CPU time tracking

    Comprehensive Parameter Sweep:

        Image sizes: 100x100 to 1600x1600 (in steps of 100)

        Iteration limits: 1000 to 5000 (in steps of 1000)

    Thread-Safe Benchmarking: Isolated from UI components for reliable measurements

    Detailed Output: Tabular results showing size, iterations, CPU time, and total iterations

MandelbrotBenchmark (Commented)

    Multi-region testing (default view, seahorse valley, elephant valley)

    Visual feedback during benchmarking

    HSB color mapping for result visualization

MandelbrotViewer (Commented)

    Interactive zooming via mouse selection

    Real-time rendering with performance metrics

    Reset functionality for view navigation

Requirements

    Java 8 or higher

    Swing/AWT (for graphical components in commented versions)

Usage
Running the CPU Benchmark
bash

javac MandelbrotCPUBenchmark.java
java MandelbrotCPUBenchmark

Output Format

The benchmark produces tabular output:
text

Size    Iterations    CPU Time (ms)    Total Iterations
100x100    1000        45.23            1,234,567
100x100    2000        89.67            2,468,135
...
1600x1600  5000        15678.90         12,345,678,901

Benchmark Parameters
Image Sizes

    Minimum: 100x100 pixels

    Maximum: 1600x1600 pixels

    Step Size: 100 pixels

Iteration Limits

    Minimum: 1000 iterations

    Maximum: 5000 iterations

    Step Size: 1000 iterations

Test Regions (in commented version)

    Default View: Full Mandelbrot set (zoom=1.0, center=-0.5,0.0)

    Seahorse Valley: Detailed region (zoom=100.0, center=-0.743643887037151,0.13182590420533)

    Elephant Valley: Complex filaments (zoom=200.0, center=0.274999999999999,0.0075)

Technical Details
Algorithm

The Mandelbrot set is generated using the standard iterative formula:
text

zₙ₊₁ = zₙ² + c

where c is the complex coordinate and iteration continues until |z| > 2 or maximum iterations reached.
Performance Measurement

    CPU Time: Measured using ThreadMXBean.getCurrentThreadCpuTime() for precision

    Wall Clock Time: Available in commented graphical versions

    Iteration Counting: Tracks total mathematical operations performed

Color Mapping

    Uses HSB color space for smooth gradient rendering

    Black for points within the Mandelbrot set (max iterations reached)

    Color spectrum for escape time visualization

Development Notes
Current Implementation

    MandelbrotCPUBenchmark: Fully functional, headless benchmarking

    MandelbrotBenchmark: Commented out, requires Swing dependencies

    MandelbrotViewer: Commented out, interactive version available

Code Structure

The project demonstrates:

    Mathematical computation optimization

    Precise performance measurement techniques

    Parameter sweeping for algorithmic analysis

    Multiple implementation approaches (headless vs graphical)

Potential Enhancements

    Multi-threading: Parallelize across CPU cores

    GPU Acceleration: OpenCL/CUDA implementation

    Additional Fractals: Julia sets, Newton fractals

    Advanced Metrics: Memory usage, cache performance

    Export Options: CSV results, performance graphs

Academic Context

This benchmark suite is particularly useful for:

    Algorithm analysis and complexity measurement

    Parallel computing performance studies

    Numerical computation optimization

    Comparative studies of mathematical algorithms

License

Educational/Research Use - See individual file headers for specific licensing.
