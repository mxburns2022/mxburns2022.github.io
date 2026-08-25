---
title: "Limitations in parallel Ising machine networks: Theory and practice"
authors: "Matthew X. Burns and Michael C. Huang"
venue: "Physical Review Applied"
date: 2025-08-19
paper: "https://journals.aps.org/prapplied/abstract/10.1103/gpg9-3tjj"
tags: [ising-machine, combinatorial-optimization, parallel-computing]
---

## Abstract
Analog Ising machines (IMs) occupy an increasingly prominent area of computer architecture research, offering high-quality, low-latency, and low-energy solutions to intractable computing tasks; however, IMs have a fixed capacity, with little to no utility in out-of-capacity problems. Previous works have proposed parallel, multi-IM architectures to circumvent this limitation [A. Sharma, et al., in Proceedings of the 49th Annual International Symposium on Computer Architecture, ISCA ’22 (Association for Computing Machinery, New York, NY, USA, 2022), p. 508; R. Santos, et al., Enhancing quantum annealing via entanglement distribution, ArXiv:2212.02465]. In this work, we theoretically and numerically investigate trade-offs in parallel IM networks to guide researchers in this burgeoning field. We propose formal models of parallel IM execution models, and we then provide theoretical guarantees for probabilistic convergence. Numerical experiments illustrate our findings and provide empirical insights into the high- and low-synchronization-frequency regimes. We also provide practical heuristics for parameter and model selection, informed by our theoretical and numerical findings.