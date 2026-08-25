---
title: "Augmenting an electronic Ising machine to effectively solve boolean satisfiability"
authors: "Anshujit Sharma, Matthew X. Burns, Andrew Hahn, Michael C. Huang"
venue: "Scientific Reports"
date: 2024-03-20
paper: "https://www.nature.com/articles/s41598-023-49966-6"
tags: [ising-machine, combinatorial-optimization, satisfiability]
---

## Abstract
With the slowdown of improvement in conventional von Neumann systems, increasing attention is paid to novel paradigms such as Ising machines. They have very different approach to solving combinatorial optimization problems. Ising machines have shown great potential in solving binary optimization problems like MaxCut. In this paper, we present an analysis of these systems in boolean satisfiability (SAT) problems. We demonstrate that, in the case of 3-SAT, a basic architecture fails to produce meaningful acceleration, largely due to the relentless progress made in conventional SAT solvers. Nevertheless, careful analysis attributes part of the failure to the lack of two important components: cubic interactions and efficient randomization heuristics. To overcome these limitations, we add proper architectural support for cubic interaction on a state-of-the-art Ising machine. More importantly, we propose a novel semantic-aware annealing schedule that makes the search-space navigation much more efficient than existing annealing heuristics. Using numerical simulations, we show that such an “Augmented” Ising Machine for SAT is projected to outperform state-of-the-art software-based, GPU-based and conventional hardware SAT solvers by orders of magnitude.
