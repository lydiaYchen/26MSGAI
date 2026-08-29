
:warning: **We are making significant changes to the evaluation of the course, compared to the previous year. The content will only be finalized by the end of the first week of the semester.**

<!-- vscode-markdown-toc -->
* 1. [Important links](#1-important-links)
* 2. [Course description](#2-course-description)
* 3. [Course team](#3-course-team)
* 4. [Learning objectives](#4--learning-objectives)
* 5. [Workload and expectation](#5-️--workload-and-expectations) 
* 6. [:dart: Grading policy](#6-dart-grading-policy)
    * 6.1. [Quizzes]()
    * 6.2. [Group projects]()
* 7. [Detailed schedule](#7--detailed-schedule)
* 8. [Relevant references](#8-relevant-references)

    
<!-- vscode-markdown-toc-config
    numbering=true
    autoSave=true
    /vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc --><!-- vscode-markdown-toc -->


# [MSGAI26] Modeling and Scaling Generative AI Systems <!-- omit in toc -->

This repository contains the materials of the **MSc Modeling and Scaling for Generative AI systems** course running in fall 2026 at UNINE. This is part of BeNeFri Master's program.




##  1. <a name='Importantlinks'></a>Important links

- [Project description](project.md)
- [Labs and assignments](lab.md)


##  2. <a name='Coursedescription'></a>Course description

# 2. Course description

# 2. Course description

Today's artificial intelligence landscape is rapidly shifting from static generative models to autonomous, multi-step agentic systems. Agentic AI systems are capable of reasoning, planning, executing tools, and adapting dynamically to solve complex real-world tasks. However, building and deploying agentic systems that meet high performance, reliability, and safety standards while efficiently managing computational constraints remains a significant technical challenge. To build production-grade agentic applications, it is essential to master both full-stack agent orchestration and the underlying systems engineering—from low-level key-value (KV) cache management to distributed optimization.

An example of real-world of this paradigm is Klarna’s OpenAI-powered AI Assistant. Moving far beyond traditional rule-based chatbots, this agentic system executes dynamic multi-step tasks by integrating directly with live backend payment systems, verifying account histories, and autonomously resolving refunds or payment disputes. In production, the assistant managed 2.3 million customer conversations in its first month alone—performing the workload equivalent of 700 full-time agents while slashing average resolution times from 11 minutes down to under two minutes.

The goal of this course is to provide students with the core foundations, systems-level optimizations, and practical skills required to design, improve, and secure agentic AI systems. Through hands-on architecture design and experimental evaluation, students will learn how to build effective agent harnesses, engineer context dynamically, implement self-correction and self-improving loops, scale training via distributed SGD, and protect systems using modern guardrails, activation steering, and privacy-preserving techniques.

Course topics include

* **Part I: Building Agentic Systems**
  * Introduction to Agentic Systems
  * Agentic Benchmark: tool use and function calling
  * Harness of Agentic Systems
  * System and KV Cache

* **Part II: Improving Agentic Systems**
  * Context Engineering
  * Self-Correction
  * Self-Improving
  * Distributed SGD

* **Part III: Robustness of Agentic Systems**
  * Self-Evolving
  * Attacks/Defenses for LLMs
  * Safety: Guardrails & Activation Steering
  * Privacy for LLMs






##  3.👩‍🏫👨‍🏫 <a name='Courseteam'></a>Course team

This course will be primarily taught by [Prof. Lydia Y Chen](https://lydiaychen.github.io/)  The course team is composed of a number of PhDs  who support the course through guest lectures and project supervision and a TA who focuses on the grading of homework. 


-  [Giulios Segalini](mailto:guilio.segalini@unine.ch) (Unine PhD student) 
-  [Abel Malan](mailto:abel.malan@unine.c) (Unine PhD student)


Lydia is the responsible instructor of this course and can be reached at **lydiaychen@ieee.org**.



##  4. 🏆 <a name='Learningobjectives'></a>Learning objectives
LO1. Understand the core architectures, harnesses, and memory systems of agentic AI, including tool use and KV caching.

LO2. Improve agent performance through context engineering, self-correction, self-improving loops, and distributed SGD.

LO3. Design resilient, self-evolving agents hardened against adversarial attacks, prompt injections, and privacy risks.

LO4. Implement runtime safety mechanisms and operational controls using guardrails, activation steering, and trajectory benchmarks.

## 5. ⏱️ <a name='Expectation'></a> Workload and Expectations

This course covers many exciting and rapidly evolving topics in AI. As these topics build on a range of existing concepts in machine learning and deep learning, the course can be demanding. Students should expect to spend an average of **4–6 hours per week** on this course, including lectures, labs, and independent study. Students without a solid background in machine learning can still take this course, but should be prepared to put in **significant additional effort to catch up with the required background**. In our experience, students who lack the necessary background may find it challenging to keep up with the course and its hands-on exercises.

At the same time, the effort can be highly rewarding. A well-executed project can develop into a successful conference publication, provide a strong foundation for a master's thesis, or serve as a strong basis for an internship. We have close collaborations with industry, and successful projects may provide opportunities to connect with our industry partners. We have several examples of students who have taken their course projects further into publications, theses, and internships, and we are happy to share these examples with the class.


## 6. <a name='dart:Gradingpolicy'></a>:dart: Grading policy

This course has no final exam; instead, the grade is largely determined through continuous evaluation. You need to **receive more than 55% on each quiz** to be eligible for the final project.

1. **Labs (0%):** Each lab provides hands-on exercises that connect the concepts covered in the course with practical coding implementations. The first part of each lab is dedicated to students working on the exercises, while the second part is led by the TA, who will address students' questions and discuss common challenges. We strongly encourage students to attend the labs and work through the exercises together, as this will help them learn the course materials more effectively and prepare for the project. **Additional content and concepts covered in the labs will also be included in the quizzes.** We expect students to spend an average 4-6 hours per week for this course. 
   
2. **Quizzes (36%):** There are 3 quizzes in weeks 4, 9, and 12. Each quiz accounts for 12% of the grade and covers 3–5 weeks of material, depending on the subject. The exact format of each quiz will be announced during the corresponding lab. The key purpose of the quizzes is to ensure that students have a sufficient understanding of **the materials covered in the course and labs.**

3. **Group project (70%):** The group project consists of a project report and a presentation. Students will develop a GAI application and optimize its performance. There will be an initial proposal in week 6, followed by an in-class interim discussion with each team in week 10. The final report will be due in week 14, with a 20-minute presentation in week 14 as well. The grading criteria of the project is described below. 




**All assessment items (project reports) have to be submitted via ILIAS.**




###  6.1. <a name='Groupprojects'></a>Group projects
<!-- 7 predefined project topics: evaluating the systems of 
-->
In this project, you will work in a group of 2–3 students to design, build, and optimize a generative AI application. Your project should address a concrete research question and investigate a measurable trade-off between model quality and system performance. For example, you may study context engineering or RAG, fine-tuning, model selection and routing, inference-time compute, KV-cache management, quantization, batching, or other inference and serving optimizations. You will evaluate your approach using appropriate quality and efficiency metrics, such as task performance, latency, throughput, memory usage, and computational cost.

The project should include a working baseline, at least one modeling or system-level optimization, and an experimental evaluation that demonstrates when and why the proposed approach is effective. There are two mandatory but ungraded milestones: an initial project proposal and an interim meeting. Completing both milestones is required to receive a passing grade for the project.

- Group size: 2-3 students
- Schedule: 
  - Initial proposal: week 6
  - Interim meeting: week 10
  - Report due: week 14
  -  Presentation/interview: week 14



At the end of each project phase we will conduct a short interview (20 minutes per group) about the group project and its connection to the course content. Based on the project report and the interview, each member of the group receives a grade. 





##  7. 📅 <a name='Detailedschedule'></a>Detailed schedule


**Week**|**Lecture Topic**|**Lab Topic**|
:-----|:-----|:-----|
Week 1 (Sep 15) | 1. Introduction of GAI| No-Lab
Week 2 (Sep 22) | 2. Diffusion Model| Diffusion Models (DDPM)
Week 3 (Sep 29) | 3. VAE and Flow Matching | VAE + Flow Matching
Week 4 (Oct 6) | 4.  LLM Introduction + Pre-train |  **Quiz1**
Week 5 (Oct 13) |5.  LLM Models and Transformers  | SFT|
Week 6 (Oct 20) | 6. Reinforcement Learning in LLM |RLHF |
Week 7 (Oct 27) | 7. LLM Reasoning |Reasoning | 
Week 8 (Nov 3 | 8. Post training  | **Quiz 2** |
Week 9 (Nov 10) | 9. Context Engineering  | Context Engineering |
Week 10 (Nov 17) | 10. Positional Embedding | Positional Embedding |Project midterm
Week 11 (Nov 24) | 11. KV Cache| KV Cache | 
Week 12 (Dec 1) | 12. Agentic AI  |  **Quiz 3** |
Week 13 (Dec 9) | Holiday - No class| Holiday -  No Lab | 
Week 14 (Dec 15) | Project presentation | No Lab | Project report and presentation



## 8. <a name='Relevantreferences'></a>Relevant references

### 8.1 Textbooks and Online Documents

* [Understanding Deep Learning](https://udlbook.github.io/udlbook/) by Simon J. D. Prince
* [Dive into Deep Learning](https://www.d2l.ai/) by Alex Smola et. al.
* [Build a Large Language Model (From Scratch)](https://sebastianraschka.com/llms-from-scratch/) by Sebastian Raschka
* [Deep Learning](https://www.deeplearningbook.org/) by Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* [Hugging Face Transformers Documentation](https://huggingface.co/docs/transformers/) by Hugging Face
* [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course/) by Hugging Face


### 8.2 Useful Code Repositories



**Diffusion Models for Different Data Modalities**

* **Images:** [Denoising Diffusion Probabilistic Models (DDPM)](https://arxiv.org/abs/2006.11239) by Jonathan Ho, Ajay Jain, and Pieter Abbeel
* **Images:** [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752) by Robin Rombach et al.
* **Images:** [Hugging Face Diffusion Models Course](https://huggingface.co/learn/diffusion-course/) by Hugging Face
* **Videos:** [Video Diffusion Models](https://arxiv.org/abs/2204.03458) by Jonathan Ho et al.
* **Videos:** [Stable Video Diffusion: Scaling Latent Video Diffusion Models to Large Datasets](https://arxiv.org/abs/2311.15127) by Andreas Blattmann et al.
* **Tables:** [Mixed-Type Tabular Data Synthesis with Score-based Diffusion in Latent Space (TabSyn)](https://openreview.net/forum?id=4Ay23yeuz0) by Hengrui Zhang et al.


**Large Language Models**

* [Qwen3](https://github.com/QwenLM/Qwen3) — Official repository for the Qwen3 family of open-weight large language models, including examples for inference, deployment, quantization, and training.
* [Llama Cookbook](https://github.com/meta-llama/llama-cookbook) — Official practical examples for building applications with Llama models, including inference, fine-tuning, RAG, and end-to-end applications.
* [Llama 2](https://github.com/meta-llama/llama) — Official Llama 2 inference code and examples.
* [Hugging Face Transformers](https://github.com/huggingface/transformers) — A general framework for using and training pretrained transformer models, including Llama, Qwen, and many other open models.
* [Hugging Face TRL](https://github.com/huggingface/trl) — Tools for post-training language models, including supervised fine-tuning (SFT), preference optimization (DPO), and reinforcement learning methods such as GRPO.









