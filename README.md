# Multi-Class-LLM-CodeGen-Benchmark
This repository presents two thoroughly designed Multi-Class-level Code Generation tasks for evaluating Human-LLM interaction (HLI) strategies, including different prompting patterns, context curation methods, various models, etc.
These tasks are designed to test how well **LLM + developer** pairs can interact and generate **multi-class Python applications** that satisfy an extensive test suite.  

It currently includes two independent tasks:

| Task | Domain | Classes to Implement | Test Suite |
|------|--------|---------------------|-------------------|
| **E-Commerce Application** | On-line retail (No GUI) | `User`, `Product`, `ShoppingCart`, `Order`, `EcommerceApp` | 128 Test Cases (Branch & Line Coverage: 100%) |
| **Smart Home Gym** | Personal fitness (No GUI) | `User`, `Feed`, `MembershipRegistration`, `LoginSystem`, `Calendar`, `ExerciseSystem`, `Ranking` | 100 Test Cases (Branch & Line Coverage: 100%) |

---

## Goals

* **Specification adherence** – every function listed in the design document must be implemented, including validation and error handling rules.  
  *Example*: the `Order` class must reject invalid status transitions such as `Delivered → Processing`.
* **Edge-case robustness** – tests cover boundary values (e.g., cart quantity `1‒100`).
* **Test Prompt Engineering Methods** – encourages use of pre-defined or customized prompting patterns (Reflection, Cognitive-Verifier, Alternative-Approach, Few-Shot) to validate the effectiveness of your own HLI strategies.
* **Human-in-the-loop Iteration on Process** – you can establish the iterative process by applying different software development processes, like Waterfall, Test-Driven Development, etc.

---

## Repository Layout
<code>.
├── Experiment Introduction.pdf
├── ScreenRecording Manual.pdf
├── Task_E-Commerse_App/
│   ├── Design Description_E-commerce_Application.pdf   # authoritative requirements
│   └── Task1.ipynb/                                    # class skeletons + 128 unit tests
├── Task_Smart_Home_Gym/
│   ├── Design Description_SmartHomeGym.pdf
│   └── Task2.ipynb/                                    # class skeletons + 128 unit tests
├── README.md
├── Prompt Pattern Templates/
│   ├── Prompt Pattern Template Introduction.pdf
│   ├── prompt_Reflection.txt
│   ├── prompt_Alternative Approach.txt
│   ├── prompt_Cognitive Verifier.txt
│   ├── prompt_Few-Shot_Task_1.txt
│   └── prompt_Few-Shot_Task_2.txt
└── Survey_Link.txt
</code>

---

## Experiment Rules
You can find the detailed instructions on how to run this experiment in the Experiment Introduction file. It consists of a 100-minute experiment: 15-minute introduction + 70-minute problem solving + 15-minute survey.
If you would like to share your screen recording, please refer to the ScreenRecording Manual file. 
0. Before starting the experiment, you need to prepare the Jupyter Notebook and LLM interaction environment, including WebUI, APIs, etc. Also, you must set up which prompt patterns you will use based on the example templates.
1. You can start from any Task you would like to solve first; however, you must switch to the other one only if you pass 95% of the test cases (E.g., for the E-Commerce App task: 121 out of 128 test cases). Partial and switching task solving for the two tasks is not allowed.
2. When you interact with LLMs, you must follow the template structure of "Instruction", "Question", and "Reference" as defined in our Prompt Pattern Template examples. Any other templates or strategies are welcome to be applied.
3. You can only directly modify the code when you try three times to request with unsatisfactory or incorrect outcomes from the LLMs.
4. The 70 minutes allocated for task-solving must be adhered to. You need to demonstrate that you completed the tasks within this time. Failure to do so will result in the outcomes not being listed.

---

## Task Briefs
- Task E-Commerce Application

In this assignment, you will be tasked with completing the implementation of an e-commerce application. The application is designed to manage various aspects of an online shopping platform, focusing on user interactions, product management, and order processing. You will be provided with partial implementations of the `User`, `Product`, `ShoppingCart`, `Order`, and `EcommerceApp` classes. Each of these classes plays a crucial role in ensuring the smooth operation of the application, from user registration to order fulfillment.

Your goal is to write the code for each method within these classes, adhering closely to the provided specifications. These specifications detail the expected functionalities, constraints, and edge cases that you must consider during implementation. The provided documentation includes comprehensive descriptions of methods, parameters, return values, and examples to guide you in developing a robust and well-defined system.

- Task Smart Home Gym

In this assignment, you will be completing the implementation of a Smart Home Gym system. The system is designed to enhance users' fitness experiences through personalized exercise management and progress tracking. You will be provided with partial implementations of the `User` and `Feed` classes, while the rest of the classes (`MembershipRegistration`, `LoginSystem`, `Calendar`, `ExerciseSession`, and `Ranking`) will need to be fully implemented by you.

You are expected to write the code for each method in these classes following the provided descriptions. The provided code and class descriptions will guide you through the expected functionality, input/output requirements, and edge cases that you need to handle.

---

## Prompt Pattern Templates
We provide four different prompt templates: Reflection, Cognitive Verifier, Alternative Approach, and Few-Shot patterns. However, you can customize the Instruction part with your prompts and add different code generation examples and orders in the Example part. If you follow the given structure of "Instruction", "Question", "Reference", and "Example", you can customize any parts of the templates you will use for interacting with LLMs in this experiment.

---

## Experiment Finish & Submission Checklist
- [ ] Submitting your code outcome in "ipynb" files
- [ ] Proofs for problem-solving time (Screen Recording video is desirable)
- [ ] Finishing the Survey in the Survey_Link.txt (Survey outcome delivered automatically)
- [ ] Chat logs with your models used in this experiment (+ Screen Recording video)

If you need any suggestions or issue reports, please use the "Issues" tab in this repository or contact "dr.sangwon.hyun@gmail.com".
Your private data and information are secured by Ethical Approval from the University of Adelaide and will never be used publicly.
