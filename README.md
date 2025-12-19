# Draw It or Lose It - Software Design Documentation
#### SNHU CS-230 Simulated Client Project

## Project Overview

This repository contains the software design documentation for **Draw It or Lose It**, a game application expansion project for **The Gaming Room**.

---

## Client and Software Specifications

**The Gaming Room** required the expansion of their existing Android-only drawing game into a distributed, multi-platform system. The objective was to create a web-based client that runs on modern browsers, supporting Windows, macOS, Linux, iOS, and Android seamlessly. Key requirements included support for multiple concurrent games, real-time data synchronization across different geographical locations, and the efficient rendering of a large 1.6GB image library.

---

## Strengths of the Design Documentation

 The most effective portion of this documentation is the **System Specification** and platform evaluation. The analysis provides a balanced comparison of Linux, Windows, and macOS architectures for both server and client environments. By weighing technical capabilities against licensing costs, team expertise, and maintenance requirements, the design recommends a solution that is not only technically viable but also cost-effective and sustainable for the client's specific resources.

---

## Value of Design Work

Developing the design document prior to implementation was instrumental in defining clear architectural boundaries. Specifically, ensuring the separation of **Storage** (static assets) from **Memory** (active game state) prevented potential bottlenecks. This pre-planning mandated the use of cloud object storage for the 1.6GB image library, ensuring the application server remains lightweight and responsive—a decision that would have been costly to reverse during active development.

---

## Areas for Revision

The **Operating Systems Architectures** section requires revision to better address failure scenarios. While it outlines the happy-path architecture, it lacks detail on system resilience. A revised version would include specific protocols for database failover, container orchestration recovery, and handling network interruptions. Adding a visual architectural diagram to illustrate these fault-tolerance mechanisms would significantly improve the document's utility for the development team.

---

## Interpreting User Needs

User needs were interpreted by translating high-level business goals into specific technical requirements. The client's request for "multi-user" and "platform-agnostic" access was implemented via a web-centric architecture using containerized microservices. This approach ensures a consistent user experience regardless of the player's device. Considering user needs is critical because it ensures the final architecture solves the actual business problem; technical complexity is only valuable if it serves the end-user's experience and accessibility.

---

## Design Approach and Strategy

The design strategy followed a structured methodology: **Requirements Analysis, Comparative Evaluation, and Architectural Decision**.
1.  **Analysis**: Decomposed the prompt into distinct technical challenges (concurrency, storage).
2.  **Evaluation**: Compared available technologies (e.g., REST vs. WebSockets, Relational vs. NoSQL) against specific project constraints.
3.  **Decision**: Selected the optimal stack based on the evaluation matrix.

For future applications, this strategy would be enhanced by incorporating formal decision matrices and creating visual data flow diagrams earlier in the process to identify potential bottlenecks before detailed specification begins.
