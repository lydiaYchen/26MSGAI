
:warning: **I am still developing the course content. The content will be only be finalized by the end of the first week of the semester.**

<!-- vscode-markdown-toc -->
* 1. [Important links](#Importantlinks)
* 2. [Course description](#Coursedescription)
* 3. [Course team](#Courseteam)
* 4. [Learning objectives](#Learningobjectives)
* 5. [:dart: Grading policy](#dart:Gradingpolicy)
    * 5.1. [Homework](#Homework)
    * 5.2. [Group projects](#Groupprojects)
* 6. [Detailed schedule](#Detailedschedule)

    
<!-- vscode-markdown-toc-config
    numbering=true
    autoSave=true
    /vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc --><!-- vscode-markdown-toc -->


# [MSGAI25] Modeling and Scaling Generative AI Systems <!-- omit in toc -->

This repository contains the materials of the **MSc Modeling and Scaling for Generative AI systems** course running in fall 2025 at UNINE. This is part of BeNeFri Master program.


##  1. <a name='Importantlinks'></a>Important links

- [Project description](project.md)
- [Labs and assignments](lab.md)


##  2. <a name='Coursedescription'></a>Course description


Todays machine learning systems become the backbone technology for our daily life.  Generative AI (GAI) systems, such as language models and diffusion models, are widely used to generate texts, images, videos, and tables. It is challenging to design and run the inference of GAI system that guarantee users’ performance requirements, e.g., latency constraint, in a resource efficient way. Various quantitative methods are applied to capture such complex system dynamics and predict metrics of interests, from the designing phase of the systems to the runtime performance, e.g., job response times and system anomaly.  To optimize the performance of GAI  systems, a deep understanding on those methods and their applications on the system design are essential. 
<!-- Having practical hand-on experience on designing experiments, deriving models, and validating results with benchmark systems will prepare students to tackle challenges of real systems. -->

Course topics include
- Generative adversarial networks
- Diffusion models
- Large language models
- Design of experiments and statistical tests 
- Operational laws and queueing methods for modeling GAI systems
- Scheduling and load balancing for GAI systems







##  3. <a name='Courseteam'></a>Course team

This course will be mainly taught by [Prof. Lydia Y Chen](https://lydiaychen.github.io/)  The course team is composed of a number of PhDs  who support the course through guest lectures and project supervision and a TA who focuses on the grading of homework. 


-  [Gert Lek](mailto:gert.lek@unine.ch) (Unine PhD student) 
-  [Basile Lewandowski](mailto:basile.lewandowski@unine.c) (Unine PhD student)


Lydia is the responsible instructors of this course and can be reached at **lydiaychen@ieee.org**.



##  4. <a name='Learningobjectives'></a>Learning objectives
- LO1. Understanding the training and sampling of generative models, namely diffusion and language models 
- LO2. Design full/fractional factorial experiments for multi-variate regression analysis, e.g., finding critical parameters for GAI systems
- LO3 Apply queueing theory to analyse and predict the run-time performance of applications, e.g., the average response times of on-line GAI sampling service
- LO4. Develop resource management policies for GAI systems and validate them on real computing systems


## 5. <a name='dart:Gradingpolicy'></a>:dart: Grading policy

This course has no final exam, instead the grade is largely determined through three components: 

1. Homework (30%): 3 individual homework due in week 5, 9, 12. Each homework accounts 10  of the grade and cover 3-4 weeks material. All homework will be released at the beginning of the semester.


2. Group project (70%): group project report (60%) and presentation (10%). There will be topics of modeling response times, configuring, dependability, scheduling design. There will be an initial proposal in week 6, interim discussion with each team in week 10. The final report will be due in week 13, and 20 minutes presentation in week 9 as well.


**All assessment items (homework, and projects reports) have to be submitted via ILIAS.**


###  5.1. <a name='Homework'></a>Homework
- Homework 1: due in week 5 
- Homework 2: due in week 9
- Homework 3: due in week 12

Students are given additional 48 hours grace period for late submission and will not receive any grade penalty. However, submissions after 48 hours grace period will not be considered and students will loose 25 points of their final grade. 


###  5.2. <a name='Groupprojects'></a>Group projects
<!-- 7 predefined project topics: evaluating the systems of 
-->
There are different aspects of performance  on modeling and optimizing the executions of deep neural network jobs. In this project, you will play with benchmarks that emulate the training jobs of deep neural networks on top of Spark platform - one of the most popular platform. You can build a model to predict the performance such jobs, to optimize their response times through resource allocations and scheduling, and to test the dependability of such a cluster against malicious attacks. You will do this project in a group with 1-2 other peers.

- Group size: 1-2 students
- Schedule: 
  - Initial proposal: week 6
  - Interim meeting: week 10
  - Report due: week 14
  -  Presentation/interview: week 14



At the end of each project phase we will conduct a short interview (20 minutes per group) about the group project and its connection to the course content. Based on the project report and the interview, each member of the group receives a grade. 





##  6. <a name='Detailedschedule'></a>Detailed schedule


**Week**|**Lecture Topic**|**Lab Topic**|**Assignment Due**
:-----|:-----|:-----|:-----
Week 1 (Sep 15) | Introduction on Generative AI (lecture 1)| Diffusion model (lecture 2)
Week 2 (Sep 22) | Holiday - No class| Holiday- No Lab
Week 3 (Sep 29) | Lab setup | Diffusion models (DDPM)
Week 4 (Oct 6) | VAE and GANs | Diffusion models (DDIM)| 
Week 5 (Oct 13) | LLM Models and Architecture| HW1 (DDIM and Tabular Diffusion) | HW1
Week 6 (Oct 20) | Model Pretrain - Alignment | Transformers |Project proposal
Week 7 (Oct 27) | Model Postraining and Reasoning |Prompt engineering|
Week 8 (Nov 3 | Model Editing and Merging | Q/A on H2 |
Week 9 (Nov 10) | Model Evaluation and Robustness  | No Lab | HW2
Week 10 (Nov 17) | DTMC | Job generator | Project midterm
Week 11 (Nov 24) | CTM| Performance analysis | 
Week 12 (Dec 1) | Queueing   |  Q/A on HW3 |HW3
Week 13 (Dec 9) | Holiday - No class| Holiday   No Lab | 
Week 14 (Dec 15) | Project presentation | No Lab | Project report and presentation



##  7. <a name='Relevantreferences'></a>Relevant references 


###  7.1. <a name='Booksonstatisticalexperimentsandlearning'></a>Statistical and Deep and learning
- [Design and Analysis of Experiments](http://faculty.business.utsa.edu/manderso/STA4723/readings/Douglas-C.-Montgomery-Design-and-Analysis-of-Experiments-Wiley-2012.pdf) by Douglas Montgomery
- [Dive into Deep Learning](https://www.d2l.ai/) by Alex Smola et. al.
- [Deep Learning](https://www.deeplearningbook.org/)
- [Pattern Recognition and Machine Learning]() by Christopher Bishop 
- [Introduction to Machine learning](http://www.cs.cmu.edu/~epxing/Class/10701/), Eric Xing at Carnagie Mellon University
- [Data Mining](http://personal.psu.edu/jol2/course/stat557/), Jia Li at Penn State University
- [Design of Experiments](https://newonlinecourses.science.psu.edu/stat503/node/5/), Penn State University



###  7.2. <a name='Booksonperformancemodeling'></a>Books on performance modeling
- Introduction to Probability Models by S. M. Ross, 
- Quantitative System Performance by E. Lazowska, J. Zahorjan, S. Graham, and K. Sevcik.
- Capacity Planning and Performance Modeling by D. Menasce, V. Almeida, and L. Dowdy 
- [Computer System Performance Evaluation](http://www.cse.cuhk.edu.hk/~cslui/csc5420.html) , John C.S. Lui at CUHK






