# ece8893-lab-1-solved
**TO GET THIS SOLUTION VISIT:** [ECE8893 Lab 1 Solved](https://www.ankitcodinghub.com/product/ece8893-lab-1-instructions-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113775&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE8893  Lab 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
The goal of this lab is to design accelerators for matrix multiplication. There are two parts to this lab: – In Part A, you will optimize an existing implementation of matrix multiplication with real values. – In Part B, you will implement matrix multiplication with complex values and optimize it.

In either part, we will multiply a $100*150$ matrix with a $150*200$ matrix to get a $100*200$ matrix product and accelerate the design for Pynq-Z2 board.

Part A: Real Matrix Multiplication (30 points)

Matrix multiplication is at the heart of virtually all deep learning applications and has high scope for parallelism. Compared to a trivial implementation, the amount of parallelism that you can exploit is constrained by the hardware resources and how well your code is optimized.

In this part of the lab, you are provided with the trivial (simplest) implementation along with a testbench to verify functionality. You need to optimize the design to achieve at least 10x speed-up while ensuring the resource utilization are all under 100%. – PartA/real_matmul.cpp contains the matrix multiplier, which is the top module of the accelerator. This is what you want to modify. – PartA/main.cpp is the testbench. Do not change this file.

Reference Material: Ryan Kastner et al., Parallel Programming for FPGAs, Chapter 7.

Part B: Complex Matrix Multiplication (70 points)

Many applications in scientific computing and signal processing require working with not just the magnitude but also the phase. This information is aptly captured using complex numbers. Let’s build on Part A and develop an accelerator to perform matrix multiplication with complex numbers.

In this part of the lab, you are not provided with the trivial implementation. You need to implement the design first (can be trivial), ensure its functional correctness with the testbench provided, and then optimize the design to achieve at least 10x speed-up while ensuring the resource utilization are all under 100%. – PartB/complex_matmul.cpp is the top module of the accelerator that you need to modify. – PartB/main.cpp is the testbench. Do not change this file.

Reference Material: Complex Matrix Multiplication

How to Run the Codes

In our HLS tutorial, we used GUI for synthesis; However, for faster development, we shall use Makefile and tcl script for simulation and synthesis.

Step 1: C Simulation

In PartA or Part B, go to the relevant folder and just type make. Then type ./result to test if your Vitis HLS function is functionally correct.

Important: Please run C simulation after every change you make to your top function. Cannot stress this enough!

Step 2: C Synthesis

To run C synthesis, you can either use GUI like we did in the tutorial, or you can use Makefile again. Go to the relevant folder (PartA or PartB) and type make synth. This internally runs: vitis_hls script.tcl

Once synthesis completes (this shouldn’t take more than a minute or two!), you can either open the GUI to read the reports, or you can find the reports under ./real_proj/solution_1/syn/report/ or ./complex_proj/solution_1/syn/report/ folders. The reports with .rpt extensions can be opened using text editors.

We recommend using csynth.rpt to assess the overall latency and resource utilization (BRAM, DSP, FF and LUT). You can check other reports for analysis purposes.

Step 3 (optional only if you have an FPGA): Export the design, import in Vivado, build the bitstream, and test on-board!

How I wish each of us can have a real FPGA board to play with!

What to Submit for this Lab

Part A

1. (20 points) Optimized source code and top-level synthesis report:

real_matmul.cpp

real_csynth.rpt (Please rename ./real_proj/solution_1/syn/report/csynth.rpt to real_csynth.rpt before submitting)

2. (10 points) A brief report including:

The baseline latency and resource utilization

The optimized latency you achieved; how much speed up you gained?

The resource utilization

What are the main techniques you adopted?

Part B

1. (50 points) Optimized source code and top-level synthesis report:

complex_matmul.cpp

complex_csynth.rpt (Please rename ./complex_proj/solution_1/syn/report/csynth.rpt to complex_csynth.rpt

before submitting)

2. (20 points) A brief report including:

The baseline latency and resource utilization

The optimized latency; how much speed up you gained compared to baseline?

The resource utilization (after optimization)

What are the main techniques you adopted?

Note: Please combine your Part A and Part B reports in a single file and submit Lab1_Report_&lt;Name&gt;.pdf. There is no template to follow, however, you are expected to write your report like a research paper.

Bonus (up to 20 extra points)

Perform design space exploration (DSE) for PartA or PartB or both. – Briefly describe the optimization techniques you implemented, the tradeoffs in latency and resource that you observed, etc. – Double the values of M, N, and K. Check how this affects the resource usage and performance. How about the run-time of the tool? Consisely mention your observations.

Submit your analysis and observations in the same report file.

Submission Guideline

Acknowledgements

Thanks to Adou Sangbone Assoa, PhD student with Prof. Arijit Raychowdhury and a former student of this course, for his idea of developing an accelerator for complex matrix multiplication!

Thanks to Ashwin Bhat, also a PhD student with Prof. Arijit Raychowdhury and former student of this course, for his inputs in developing this lab!

Grading Rubric

$$ Speedup = rac{Baseline Latency}{Optimized Latency} $$

Part A.1 (20 points)

simulationTestPass → +5 points if (simulationTestPass):

if(speedup ≥ 10x), +7 points else if(2x ≤ speedup &lt; 10x), +4 points else, +2 points

for resource in [BRAM, DSP, FF, LUT]:

+2 points if utilization ≤ 100%

Part A.2 (10 points)

Missing or incomplete information → -1 point for each question

Report values different from the ones achieved in Part A.1 → -2 points each

Insufficient description of technique(s) adopted → -2 points

Part B.1 (50 points)

simulationTestPass → +15 points if (simulationTestPass):

if(speedup ≥ 10x), +15 points else if(2x ≤ speedup &lt; 10x), +10 points else, +5 points

for resource in [BRAM, DSP, FF, LUT]:

+5 points if utilization ≤ 100%

Part B.2 (20 points)

if baseline latency is not ~2x or ~4x of PartA baseline → -5 points unless justified

Missing or incomplete information → -2 point for each question

Report values different from the ones achieved in Part A.1 → -3 points each

Insufficient description of technique(s) adopted → -2 points

Part C (Extra 20 points)

Awarded on a case-to-case to basis depending on how well the analysis/observations/implementations adhere to the questions stated.
