

## Objectives

The objectives of this project are two fold: (i) building a performance model to predict the latency or throughput for the Generative AI systems, which can be either training or inference, and (ii) improving the the performance of such systems via strategies, e.g., early exit, caching, or better scheduling policies. 



 Your final grade depends on (i) the rigorousness and correctness of your experiments, (ii) the percentage of performance improvement of your solution compared to the non-optimized systems, and  (iii) the readability of your report.



## Key milestones

Milestones:

1. **Project proposal** (mandatory, but ungraded - you will receive feedback): due on week 6
2. **Intermediate project meeting** (mandatory, but ungraded - you will receive feedback): due on week 10
3. **Final project report** (mandatory, graded): due on week 13
4. **20 min project presentation** (mandatory, graded): due on week 13

All the documents need to be submitted via the ILISAS. Exact due dates are on the ILIAS.

## Grading breakdown of the project
- Your project accounts for 70% of your final grade.
- Final report: 65%
- 15 min project presentation: 15 %
- Individual contribution: 20%

## Example of a project

Here is an example of how this project will look like. The goal is to build a queueing model to predict the average latency of inference of tabular/image diffusion jobs and to apply early exist to improve the latency. The very first step is that you setup/emulate such a diffusion serving system, which can receive inference job. Put in simple words, you try to build a mathematical models to predict the average job response times of your lab exercises. The second step is that you try to tweak model and system parameters to improve the latency of your serving system, e.g., early exit, and different schedule policies. 
-  In order to build the latency model, you need to first know/assume the arrival patterns of such inference jobs, e.g., average arrival rate and inter-arrival time distribution. 
-  Then, you need to decide the job execution time or then obtain the estimates. This can be done through running/measuring the inference time of jobs with respect to different system parameters, e.g., the memory size, and the number of cores.  
-   After obtaining the job arrival times and execution times, you can make assumption of the underlying and simplified queueing systems, e.g., single queue and single server, and then apply the formula/methodologies learned in the last part of the course. Then you judge the the accuracy of your model and explain where the discrepancy comes from. Ideally, this should be done **by intermediate project meeting**.**
-  Apply the optimization strategy of your own choice. This is where you can maximize your novelty. Read through papers on different acceleration technologies and apply them. For instance, keep two version of models and swapped to smaller models when the queue is exceeding the certain threshold. Verify if such a strategies working on your system and your model can capture the impact of such an optimization strategy. This can be done through mathematical modeling, simulation, or actual improvement.

 
## Fruit of thoughts - papers

https://arxiv.org/pdf/2312.05385
https://www.usenix.org/conference/nsdi24/presentation/agarwal-shubham
https://i.cs.hku.hk/~cwu/papers/Sheng-ARR24-HiddenKey.pdf
https://i.cs.hku.hk/~cwu/papers/hphu-eurosys24.pdf
https://arxiv.org/pdf/2403.01136
