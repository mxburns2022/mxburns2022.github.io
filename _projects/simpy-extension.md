---
title: "SimPy: Simulation Framework"
description: "A Python-based discrete event simulation framework for modeling complex systems."
github: "https://github.com/example/simpy-extension"
language: Python
status: Active
tags: [simulation, python, discrete-events]
---

## Overview

SimPy is a powerful framework for discrete-event simulation. This project extends SimPy with additional features for scientific computing applications.

## Features

- **Event scheduling**: Flexible event-based simulation kernel
- **Resource management**: Model queuing, congestion, and resource contention
- **Data collection**: Built-in support for collecting and analyzing results
- **Parallel batch runs**: Run multiple simulations in parallel
- **Visualization tools**: Generate plots and animations from simulation results

## Installation

```bash
pip install simpy-extended
```

## Quick Start

```python
import simpy
from simpy_extended import Simulation

def customer_process(env, name):
    yield env.timeout(1.0)
    print(f"{name} completed at {env.now}")

env = simpy.Environment()
env.process(customer_process(env, "Customer 1"))
env.run()
```

## Applications

- Queue simulation and optimization
- Network modeling
- Manufacturing systems
- Healthcare systems
- Telecommunications

## Documentation

Full documentation with examples and tutorials available at [GitHub](https://github.com/example/simpy-extension).
