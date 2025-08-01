# MiSSOC algorithm

This repository is associated with the following paper:

> Cuesta, M., D’Ambrosio, C., Durban, M., Guerrero, V., & Trindade, R. S. (2025).  *On leveraging constrained smooth additive regression models for global optimization*. Manuscript submitted for publication.

## Abstract

Many real-world decision-making processes rely on solving mixed-integer nonlinear 
programming (MINLP) problems. However,  finding high-quality solutions to MINLPs 
is often computationally demanding.  This has motivated the development of 
specialized algorithms that take advantage of the structure of some MINLPs to 
improve their tractability. In this work, we propose the  Mixed-integer Smoothing
Surrogate Optimization with Constraints (MiSSOC) approach, a novel optimization 
algorithm that builds and solves surrogate problems for complex MINLPs which are 
more tractable in practice. MiSSOC integrates statistical modeling into mathematical
optimization by approximating complex functions in an MINLP using smooth additive 
regression models with $B-$splines.  Expert knowledge can be incorporated into the
building phase of the approximating functions through shape constraints related to
sign (or bounds), monotonicity and convexity over the observed domain. Thus, MiSSOC 
fills a gap in the literature by building surrogates that are both data-driven and
knowledge-driven. The surrogate problem is formulated by replacing the original
complex functions with their approximations. The proposed MiSSOC algorithm is 
evaluated through a set of experiments, including benchmark instances and a 
real-world case study. MiSSOC is tested with different state-of-the-art solvers 
and with the tailored Sequential Convex MINLP (SC-MINLP) algorithm. The latter 
exploits the separable structure of the  surrogate functions, which results 
from the approximating functions being sums of piecewise univariate polynomials. 
MiSSOC is benchmarked against solving the original MINLPs directly. The results 
show that MiSSOC is an effective approach for addressing complex MINLPs through 
surrogate modeling, particularly when used in combination with the SC-MINLP algorithm.

## Overview

This repository is organized into two main folders:

- `shape_constrained_smooth_additive_regression_model/`: Python code to fit shape-constrained smooth additive regression models using B-splines.
  
- `surrogate_optimization/`: Python code to construct and solve surrogate optimization problems using the fitted models for the Hydro Unit Commitment problem.

Each folder is self-contained and includes its own documentation.
