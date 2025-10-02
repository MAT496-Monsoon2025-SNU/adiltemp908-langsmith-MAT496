Module 1
Video 1 — Tracing Basics

Learnings:

In this lesson, I was introduced to the fundamentals of tracing in LangChain. I learned how tracing can be used to monitor and understand what happens inside a language model application, making it easier to debug and improve. A key takeaway was the use of metadata, which makes runs easier to organize and identify in LangSmith. I also practiced setting up tracing by configuring environment variables, which is the foundation for enabling observability. The exercise showed me how tracing provides visibility into questions asked to the model, and how this setup can help in systematically tracking performance over time.

Code Changes:

Set environment variables to enable tracing

Added traceable functions and metadata

Added a new question for testing

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/tracing_basics.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module1/tracing_basics.ipynb

Video 2 — Types of Run

Learnings:

In this video, I learned about assigning different run types to different parts of the code. This feature is especially useful because it makes the outputs in LangChain much easier to interpret. For example, by setting a run type to “retriever,” the retrieved documents are neatly organized and clearly separated from other steps in the pipeline. This makes debugging and analysis much simpler, as each component’s role is explicitly defined. I realized that assigning run types is not only good practice but also an important way to make complex workflows more transparent and manageable.

Code Changes:

Set environment variables and enabled tracing

Labeled runs with appropriate run types

Added a new question for validation

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/types_of_runs.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module1/types_of_runs.ipynb

Video 3 — Alternative Tracing Methods

Learnings:

This module introduced me to alternative ways of enabling tracing, such as using the trace() method for finer-grained control. I learned that this approach is particularly useful when you want to track specific parts of the code instead of tracing everything by default. The video also showed how tracing can be set up globally from the beginning, which is convenient for projects where consistent monitoring is needed. While runtree was mentioned, it was not covered in detail, so that portion of the code was not run or modified. Overall, this video highlighted that there isn’t just one way to do tracing, and different approaches can be chosen depending on the use case.

Code Changes:

Set environment variables and enabled tracing

Added trace() for finer-grained tracing control

Added a new question for testing

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/alternative_tracing_methods.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module1/alternative_tracing_methods.ipynb

Video 4 — Conversational Thread

Learnings:

In this lesson, I explored how metadata can be used to create conversational threads. By assigning a common thread ID across runs, it becomes possible to link a sequence of interactions and simulate a natural conversation. This allows follow-up questions to be meaningfully connected to earlier responses, which is crucial for chatbot-like applications. In LangChain, this structure is visualized as conversational turns, making it easy to see how dialogue flows across multiple queries. This approach taught me how to build a more realistic conversational experience while keeping the system simple.

Code Changes:

Set environment variables and enabled tracing

Used metadata to establish a conversation thread

Kept the original questions since the second one was a follow-up

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/conversational_threads.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module1/conversational_threads.ipynb

Module 2

Video 1 — Datasets

Learnings:

In this video, I learned the importance and use of datasets in LangSmith. A dataset is a collection of golden examples that represent the outputs we expect from the model. These examples can later be used to evaluate model performance by comparing run outputs with reference outputs. I explored different ways of adding examples to a dataset — programmatically, manually through the UI, by tracing, and even by AI generation. This flexibility ensures that we can create high-quality benchmarks for the model. Understanding datasets helped me realize that they form the foundation for evaluation and experimentation in LangSmith.

Code Changes:

Set environment variables and enabled tracing

Created datasets and added examples in different ways

Added a new question for validation

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/dataset_upload.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module2/dataset_upload.ipynb

Video 2 — Evaluators

Learnings:

In this video, I learned about evaluators, which are tools that measure how good the output of a model is compared to the reference or golden output. Evaluators take input, run output, and reference output, and then produce a score or qualitative evaluation. I explored multiple ways of defining evaluators — in local code, through LLM-as-judge, and custom code in the LangSmith UI. Evaluators can test different metrics such as similarity, correctness, or hallucination, depending on what matters most for the application. I also learned how evaluators make it easier to scale evaluation across multiple examples.

Code Changes:

Set environment variables and enabled tracing

Created a new cell block to compare evaluator scores for two cases: contradictory output and an almost identical output to the and evualator score was as desired 1(least similar) for the contradictory output and 9 for the 
almost identical output 

Added the required changes for the code to run smoothly

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/evaluators.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module2/evaluators.ipynb

Video 3 — Experiments

Learnings:

This lesson introduced me to experiments in LangSmith. I learned that experiments are essentially a way to apply evaluators on a dataset of examples to measure model performance. Experiments can be run on an entire dataset, on specific examples by using their IDs, or on specific splits of the dataset. After running an experiment, LangSmith provides detailed reports that allow us to analyze performance metrics across all examples. This was an important step in understanding how to systematically test and compare different approaches instead of relying on individual test cases.

Code Changes:

Set environment variables and enabled tracing

Made required changes for execution

Ran experiments on specific examples to observe evaluation results

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/experiments.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module2/experiments.ipynb

Video 4 — Analyzing Experiment Results

Learnings:

In this video, I learned how to interpret and analyze the results of experiments. LangSmith provides detailed dashboards and analytics that show how models perform over time, making it easier to track progress and spot weaknesses. I saw a direct comparison between ChatGPT 4o and 3.5 Turbo, where 4o was more accurate and concise but slightly slower. The analysis highlighted the value of running structured experiments, since they reveal not just raw outputs but measurable differences in performance. This reinforced the importance of evaluation when choosing or fine-tuning models for real-world applications.

Code Changes:

No code was provided to edit, as this video focused entirely on result analysis

Video 5 — Pairwise Experiments

Learnings:

This module focused on pairwise experiments, which are used to compare two outputs directly against each other. I learned that pairwise evaluation is particularly useful in cases where independent scoring doesn’t clearly show which output is better. By using LLM-as-judge to evaluate outputs side by side, it becomes possible to identify the stronger response more reliably. I saw how this method was applied to compare outputs from ChatGPT 4o and 3.5 Turbo, and the LLM consistently judged 4o’s responses as better. This module demonstrated that pairwise experiments are an essential tool for prompt optimization and model comparison.

Code Changes:

Set environment variables and enabled tracing

Modified the evaluation prompt to reduce maximum scoring, since outputs were otherwise scoring too high

Ran pairwise comparisons to determine which chatbot produced stronger results

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/pairwise_experiments.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module2/pairwise_experiments.ipynb

Video 6 — Summary Evaluators

Learnings:

In this lesson, I learned about summary evaluators, which are designed to compute metrics over the entire experiment rather than on individual examples. Unlike earlier evaluators that score each run output separately, summary evaluators look at the bigger picture by aggregating results. This allows us to measure global statistics such as overall accuracy, average similarity, or distribution of scores. I realized that this is crucial when evaluating large datasets, since focusing only on individual scores may not capture the model’s true performance. Summary evaluators are therefore a key part of high-level evaluation and comparison across different experiments.

Code Changes:

Set environment variables and enabled tracing

Made only the required changes to ensure functionality, since altering core code would affect evaluation results

Notebooks:

Source code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Sourcecodes/summary_evaluators.ipynb

Edited code: https://github.com/MAT496-Monsoon2025-SNU/adiltemp908-langsmith-MAT496/blob/deb8d5926fbfd19eaa93fd60e6c8632dee599a07/Module2/summary_evaluators.ipynb

