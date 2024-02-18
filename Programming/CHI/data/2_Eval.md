---
Author: AAM
Date: 2024-02-18
tags:
  - programming
  - other
---

---
# GUI Evaluation

[Back to index](/Programming/CHI/CHI.md)

---

## Definition

Based on cognitive psychology, we try to identify potential problems.

```mermaid
graph LR
	A((Cognitive Psycology)) --> B(Human Intelligence)
    A --> C(Language)
    A --> D(Thinking & Problem Solving)
    A --> E(Memory)
    A --> F(Attention)
    A --> G(Perception)
```

First identify a usability criteria (heuristics) and then study them.
Some common heuristics are:
- System behaviour is predictable.
- System behaviour is consistent (use conventions).
- Feedback is provided.
- System uses "real world" language.
- User control and freedom (undo & redo)
- Error prevention.

A review-based evaluation relies on experimental results and empirical evidence.

## Types of Evaluation

- **Observational methods:**
	- **Think aloud**. Users are asked to describe what they do and why.
	- **Cooperative evaluation**. Users and evaluator ask questions to each other.
	- **Protocol analysis**. Requires expert analysis of means of recording.
	- **Automated analysis**. Videotaping with automated annotation/response (quantitative).
	- **Post-talk walkthroughs**. Recording is played back to participants for comments.
- **Query techniques:**
	- **Interviews**. List of questions asked to the user one-to-one.
	- **Questionnaires**. List of questions to the users (less personal).
- **Physiological methods:**
	- **Eye tracking**.
	- **Physiological measurements**. Emotional response linked to physical changes.

## Automated acceptance tests

They are tests that can be run in front of a user to verify if the product meets the acceptance criteria.

- **Behaviour-Driven Development (BDD)** is a method that uses user stories and scenarios to define the features and expected outcomes of the product.
- **Cucumber** is a tool that allows writing user stories in a language called Gherkin and linking them to step definitions that can be executed to validate the user stories.
- **Selenium** is a tool that enables browser-based testing with JavaScript and can be integrated with Cucumber.