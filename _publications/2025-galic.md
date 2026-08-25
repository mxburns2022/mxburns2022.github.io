---
title: "GALIC: Hybrid Multi-Qubitwise Pauli Grouping for Quantum Computing Measurement"
authors: "Matthew X. Burns, Chenxu Liu, Samuel A. Stein, Bo Peng, Karol Kowalski, Ang Li"
venue: "Quantum Science and Technology 10, 015054"
date: 2025-01-01
paper: "https://doi.org/10.1088/2058-9565/ad9d74"
preprint: "https://arxiv.org/abs/2409.00576"
tags: [quantum-computing, measurement, quantum-chemistry]
# excerpt: "A hybrid strategy for grouping Pauli terms to reduce the measurement cost of quantum computations."
---

## Abstract
Observable estimation is a core primitive in NISQ-era algorithms targeting quantum chemistry applications. To reduce the state preparation overhead required for accurate estimation, recent works have proposed various simultaneous measurement schemes to lower estimator variance. Two primary grouping schemes have been proposed: full commutativity (FC) and qubit-wise commutativity (QWC), with no compelling means of interpolation. In this work we propose a generalized framework for designing and analyzing context-aware hybrid FC/QWC commutativity relations. We use our framework to propose a noise-and-connectivity aware grouping strategy: Generalized backend-Aware pauLI Commutation (GALIC). We demonstrate how GALIC interpolates between FC and QWC, maintaining estimator accuracy in Hamiltonian estimation while lowering variance by an average of 20% compared to QWC. We also explore the design space of near-term quantum devices using the GALIC framework, specifically comparing device noise levels and connectivity. We find that error suppression has a more than 10 × larger impact on device-aware estimator variance than qubit connectivity with even larger correlation differences in estimator biases.

