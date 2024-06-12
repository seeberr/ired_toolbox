# The Implicit Robust Exact Differentiator (IRED) Toolbox

This toolbox provides a Matlab/Simulink implementation of the implicit robust
exact differentiator (IRED) introduced in [1], which is an implicit (i.e.,
backward Euler) discrete-time implementation of the sliding-mode based robust
exact differentiator (RED) [2, 3] that exhibits neither discretization
chattering nor bias errors.

The IRED Simulink block in the toolbox numerically computes up to $m$ time
derivatives of a sampled input signal with fixed sampling time $T$. The
differentiator provides provides good robustness to additive measurement noise
that may be present and and the only information required about the signal to
be differentiated is an upper bound $L$ on the absolute value of its $(m+1)$-th
time derivative. Increasing the single tuning parameter $\kappa > 1$ allows to
increase the convergence speed at the cost of increasing sensitivity to
measurement noise.

Tuning the four parameters differentiation order $m$, bound $L$, sampling time
$T$, and tuning parameter $\kappa$ allows to easily use the toolbox without
requiring any detailed knowledge of its design. For users that are more
familiar with the topics presented in [1], the toolbox also features an
advanced parametrization mode that allows to fine-tune some internal parameters
of the IRED, if desired.

[1] R. Seeber: Proper Implicit Discretization of Arbitrary-Order Robust
Exact Differentiators, [arXiv:2404.02770 (2024)](https://arxiv.org/abs/2404.02770)

[2] A. Levant: Robust exact differentiation via sliding mode technique,
Automatica 34 (1998)

[3] A. Levant: Higher-order sliding modes, differentation and output-feedback control, International Journal of Control 76 (2003)
