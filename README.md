# Multi-Class-LLM-CodeGen-Benchmark
This repository presents two thoroughly designed Multi-Class-level Code Generation tasks for evaluating Human-LLM interaction (HLI) strategies, including different prompting patterns, context curation methods, various models, etc.
These tasks are designed to test how well **LLM + developer** pairs can interact and generate **multi-class Python applications** that satisfy an extensive test suite.  

It currently includes two independent tasks:

| Task | Domain | Classes to Implement | Test Suite |
|------|--------|---------------------|-------------------|
| **Task 1 – E-Commerce Application** | On-line retail (No GUI) | `User`, `Product`, `ShoppingCart`, `Order`, `EcommerceApp` | 128 Test Cases (Branch & Line Coverage: 100%) |
| **Task 2 – Smart Home Gym** | Personal fitness (No GUI) | `User`, `Feed`, `MembershipRegistration`, `LoginSystem`, `Calendar`, `ExerciseSystem`, `Ranking` | 100 Test Cases (Branch & Line Coverage: 100%) |

---

## Table of contents

1. [Goals](#goals)
2. [Repository layout](#repository-layout)
3. [Experiment rules](#experiment-rules)
4. [Detailed task briefs](#detailed-task-briefs)
   1. [Task 1 – E-Commerce Application](#task-1--e-commerce-application)
   2. [Task 2 – Smart Home Gym](#task-2--smart-home-gym)
5. [Prompt-pattern toolkit](#prompt-pattern-toolkit)
6. [Submission checklist](#submission-checklist)
7. [License](#license)

---

## Goals

* **Specification adherence** – every public method listed in the design document must be implemented, including validation and error handling rules.  
  *Example*: the `Order` class must reject invalid status transitions such as `Delivered → Processing`.
* **Edge-case robustness** – tests cover boundary values (e.g., cart quantity `1‒100`).
* **Test Prompt Engineering Methods** – encourages use of pre-defined or customized prompting patterns (Reflection, Cognitive-Verifier, Alternative-Approach, Few-Shot) to validate the effectiveness of your own HLI strategies.
* **Human-in-the-loop Iteration on Process** – you can establish the iterative process by applying different software development processes, like Waterfall, Test-Driven Development, etc.

---

## Repository layout
<code>.
├── task1_ecommerce/
│   ├── Design Description_E-commerce_Application.pdf   # authoritative requirements
│   └── Task1.ipynb/                                    # class skeletons + 128 unit tests
├── task2_smarthomegym/
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
