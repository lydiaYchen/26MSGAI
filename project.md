## Objectives

The objectives of this project are two fold: (i) building an interesting Generative AI application using appropriate models, techniques, and tools, and (ii) improving the quality, efficiency, or performance of the application through appropriate adaptation and optimization strategies. The project can involve different types of GAI systems, such as large language models, diffusion models, or other generative models. Students are expected to understand the underlying model, design an effective application around it, and make informed choices about techniques such as context engineering, fine-tuning, post-training, and inference-time optimization.

Your final grade depends on (i) the rigor and correctness of your experiments, (ii) the quality and effectiveness of your GAI application and the improvements achieved through your optimization strategies, and (iii) the readability and clarity of your report.

## Key Milestones

Milestones:

1. **Project proposal** (mandatory, but ungraded - you will receive feedback): due on week 6
2. **Intermediate project meeting** (mandatory, but ungraded - you will receive feedback): due on week 10
3. **Final project report** (mandatory, graded): due on week 14
4. **20 min project presentation** (mandatory, graded): due on week 14

All the documents need to be submitted via the ILISAS. Exact due dates are on the ILIAS.

## Grading Breakdown 

* Your project accounts for 70% of your final grade.
* Final report: 65%
* 20 min project presentation: 15 %
* Individual contribution: 20%

## Project Guidline

<figure style="text-align: center;">
  <img src="Projectimeline.jpeg" alt="GAI project timeline" style="max-width: 100%;">
  <figcaption><strong>Project timeline:</strong> From building a GAI application to adapting, evaluating, and optimizing its performance. Illustration generated with Google Gemini.</figcaption>
</figure>

Here is an example of how this project will look like. The goal is to build a GAI application for a specific real-world task and then improve its quality and/or performance through appropriate model adaptation and inference optimization. For example, you may build an LLM-based application for document analysis, question answering, or an agentic task, or a diffusion-based application for generating images, videos, or tabular data. The very first step is to identify an interesting application and select an appropriate generative model. You then need to understand the model and design a working application around it. The second step is to improve the application using techniques learned in the course, such as context engineering, fine-tuning, post-training, or inference-time optimization.

* In order to build the GAI application, you first need to clearly define the application task, target users, and desired behavior. You should investigate existing models and select an appropriate model for your application. This may involve using an open LLM such as Qwen or Llama, or an appropriate diffusion model. You should explain why the selected model is suitable for your application and establish a meaningful baseline system.

* Then, you need to design and implement the application. Depending on your task, this may involve prompt and context engineering, retrieval or external information, structured outputs, model fine-tuning, or other techniques. You should design appropriate experiments to understand which components of your system are important and evaluate the quality and robustness of your application using suitable metrics and test cases.

* After obtaining a working application, you should identify opportunities for improvement. This is where you can maximize the impact and novelty of your project. For example, you may fine-tune the model for your specific task, improve the context provided to the model, introduce a more effective reasoning strategy, or use inference-time compute to improve the quality of the generated results. You should clearly formulate the hypothesis behind your proposed improvement and evaluate it systematically. Ideally, the initial application and evaluation should be sufficiently developed **by the intermediate project meeting**.

* Finally, you should optimize the application for practical deployment. Depending on your application, this may involve reducing inference latency or memory consumption, improving throughput, or achieving a better quality-efficiency trade-off. For LLM-based systems, possible directions include KV-cache optimization, efficient positional embeddings, model selection, quantization, or inference-time compute strategies. For diffusion-based systems, possible directions include reducing the number of sampling steps, using latent representations, model distillation, or other acceleration techniques. You should demonstrate the impact of your optimization experimentally and discuss the trade-offs between generation quality, computational cost, and inference performance.

The project does not need to introduce a completely new algorithm. A strong project should instead demonstrate that you can **understand an existing GAI model, build a meaningful application, systematically evaluate it, and make it better through informed adaptation and optimization**. Particularly successful projects may provide a strong foundation for a master's thesis, internship, or research publication.

## Grading Rubrics

| Criteria | 9–10 (Excellent) | 7–8 (Good) | 4–6 (Satisfactory) | 1–3 (Needs Improvement) | Score |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **Novelty of GAI Application** | Highly original concept; tackles a compelling problem with innovative open-model utilization. | Clear, practical application with distinct original features or tailored workflows. | Conventional use case; limited original thought beyond standard applications. | Trivial wrapper around a model with minimal creativity or added value. | **/10** |
| **Difficulty of Adaptation** | Implements a novel model adaptation and inference-time improvement, supported by solid performance gains. | Combines model adaptation with explicit inference-time optimization (e.g., quantization, pruning, caching). | Adapts an existing model (e.g., fine-tuning, RAG, custom agent pipelines) beyond default usage. | Uses an existing model out-of-the-box without meaningful adaptation (insufficient). | **/10** |
| **Extensiveness of Evaluation** | Evaluates **4+ datasets** or distinct model variants with comprehensive metrics and benchmark analysis. | Evaluates **3 datasets** or distinct model variants with thorough comparative metrics. | Evaluates **2 datasets** or distinct model variants using basic validation metrics. | Evaluates **1 or 0 datasets**; superficial testing with minimal empirical validation. | **/10** |
| **Report & Code Repository** | Professional report paired with a well-structured, reproducible code repository and clear README setup. | Clear report and organized repository; code runs with minor setup effort. | Complete report, but repository lacks clear documentation or setup instructions. | Incomplete report or broken, unstructured repository without instructions. | **/10** |

## Project Examples

completed by student groups from previous terms during the second or third week of the course. Please note that earlier iterations of this course emphasized Design of Experiments and Queueing Theory, which are not covered in this semester's curriculum. Instead, your main task will be to develop novel Generative AI applications leveraging open-source foundation models. Focus on the sample projects' structure, technical depth, and presentation style rather than their specific theoretical requirements.



 
