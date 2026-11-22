## 1.1 One-Loop Diagrams
- **Objective:** Systematically calculate and verify one-loop 1PI contributions.

### 1.1.1 Model and Feynman Rules
- **Experiment:** Verified scalar $\phi^4$ theory Lagrangian and Feynman rules in Mathematica.
- **Outcome:** Global symbolic definitions (propagator, vertices, loop measure) align with *Fields Notes* §12 conventions.

### 1.1.2 Two-Point Function
- **Experiment:** Generated the tadpole topology and evaluated the self-energy $\Sigma^{(1)}$.
- **Outcome:** Confirmed momentum-independence of the 1PI two-point function.

### 1.1.3 Four-Point Function
- **Experiment:** Generated 1PI $s, t, u$ channels for the four-point function.
- **Optimization:** Used `ExcludeTopologies -> {Reducible}` to isolate physical 1PI contributions.
- **Outcome:** Correct identification of physical topologies; bubble channels defined analytically.

### 1.1.4 Mapping and Symmetry Verification
- **Experiment:** Mapped FeynArts-generated 1PI topologies to the analytical channels.
- **Outcome:** Confirmed matching and established a reconciliation step for Euclidean sign conventions.

### 1.1.5 Model Identification and Conventions
- **Experiment:** Fixed the dictionary between FeynArts/FeynCalc conventions and the project's Euclidean framework.
- **Outcome:** Reconciled conventions for Wick rotation, loop measure, and Mandelstam invariants to ensure output consistency.

### 1.1.6 Computational Reduction (ToPaVe)
- **Experiment:** Performed Passarino-Veltman reduction of FeynCalc-generated amplitudes to the standard basis ($T, B(P)$).
- **Optimization:** Implemented a mapped `TID` reduction across all channels.
- **Outcome:** Successful reduction to the basis integrals; results prepared for matching verification.

### 1.1.7 Euclidean Matching
- **Experiment:** Compared computational outputs (ToPaVe) against analytical Euclidean building blocks.
- **Outcome:** Explicit consistency check passed; matching relations between amplitudes and theory building blocks confirmed.

## 1.2 Cutoff and Dimensional Regularization
- **Objective:** Evaluate fundamental tadpole and bubble integrals and verify their consistency.
- **Methodology:** Parallel evaluation using sharp momentum cutoff and dimensional regularization (DR).

### 1.2.1 Definition of the Tadpole and Bubble Integrals
- **Experiment:** Formalized the integral basis $\{T, B(P^2), B(0)\}$ in Mathematica.
- **Outcome:** Definitions verified for consistency with the scalar propagator framework.

### 1.2.2 Sharp Momentum Cutoff Evaluation
- **Experiment:** Evaluated the tadpole $T_\Lambda$ and bubble $B_\Lambda(P^2)$ using sharp-cutoff regularization.
- **Methodology:** Employed analytical angular integration to enforce the strict UV boundary at $|k| = \Lambda$ without needing momentum shifts.
- **Outcome:** Extracted hierarchy of divergences ($\Lambda^2, \log \Lambda$) required for cutoff renormalization.

### 1.2.3 Dimensional Regularization Framework
- **Experiment:** Initialized standard Gamma function representations for tadpole and bubble integrals in $d=4-\varepsilon$ dimensions.
- **Outcome:** Framework established; prepared the expressions for Laurent expansion.

### 1.2.4 Laurent Expansions and Pole Structure
- **Experiment:** Performed Laurent series expansion of the DR integrals around $\varepsilon=0$.
- **Outcome:** Successfully isolated $1/\varepsilon$ poles and identified universal divergence structures across channels.

### 1.2.5 Verification of the Derivative Identity
- **Experiment:** Numerically and symbolically verified $B_{\text{DR}}(0) = -\partial T_{\text{DR}} / \partial m^2$.
- **Outcome:** The identity holds to $O(\varepsilon)$, confirming mathematical consistency between the tadpole and bubble results in the DR scheme.

## 1.3 Counterterms and Regulator Independence
- **Objective:** Cancel UV divergences using counterterms and demonstrate regulator independence for physical observables.
- **Methodology:** Impose renormalization conditions at zero momentum and compare results across regularization schemes.

### 1.3.1 Renormalization Conditions
- **Experiment:** Formalized kinematic constraints on $\Gamma^{(2)}$ and $\Gamma^{(4)}$ at zero momentum.
- **Outcome:** The system of equations defining $\delta Z_\phi, \delta m^2, \delta \lambda$ is fully established.

### 1.3.2 Derivation of Counterterms
- **Experiment:** Solved the system of renormalization equations for the counterterms.
- **Outcome:** Analytical expressions obtained for mass, field, and coupling counterterms, with universal pole coefficients confirmed ($\delta Z_\phi = 0$).

### 1.3.3 Regulator Independence and Finite Differences
- **Experiment:** Compared the finite momentum-dependent part $\Delta B(P^2) = B(P^2) - B(0)$ between Sharp Cutoff and DR.
- **Methodology:** Implemented a hybrid analytical-numerical strategy, forming the UV-convergent difference before taking the $\Lambda \to \infty$ limit.
- **Outcome:** Analytical convergence confirmed; both schemes yield identical physical scattering amplitudes, validating regulator independence.
- **Verification:** The zero-momentum slope consistency was checked; the residual mass-dependent difference in the cutoff scheme is identified as a feature of scheme-dependent scaling behavior.

## 1.4 Beta Function and Fixed Point
- **Objective:** Determine the renormalization group flow of the $\phi^4$ coupling and identify critical fixed points.
- **Methodology:** Use the MS scheme to derive the beta function and solve the fixed-point equation in $d=4-\varepsilon$ dimensions.

### 1.4.1 Minimal Subtraction (MS) Scheme
- **Experiment:** Implement MS scheme counterterms by isolating $1/\varepsilon$ pole coefficients.
- **Outcome:** Counterterms correctly defined; consistent with the $\varepsilon = 2\varepsilon_{FC}$ conversion factor used in FeynCalc.

### 1.4.2 Derivation of the Beta Function
- **Experiment:** Derive $\beta_g(\lambda)$ from the $\mu$-independence of the bare coupling $\lambda_0$.
- **Outcome:** Successfully derived the one-loop beta function; results align with expected coupling evolution.

### 1.4.3 Nontrivial Fixed Point
- **Experiment:** Solve $\beta_g(g_*) = 0$ to identify the nontrivial Wilson-Fisher fixed point.
- **Status:** Fixed point derived ($g^* = \varepsilon/3$); stability analysis using refined assumptions confirms the Gaussian point is UV-attractive (IR-relevant) and the Wilson-Fisher point is IR-attractive (UV-unstable) for $\varepsilon > 0$.

### 1.4.4 Field Anomalous Dimension
- **Experiment:** Evaluate the field anomalous dimension $\gamma_\phi$ at one loop.

## 2.1 The Two-Loop Two-Point Function
- **Objective:** Calculate the two-loop contribution to the scalar self-energy and examine subdivergences.
- **Methodology:** Systematic generation, classification, and evaluation of 1PI two-loop sunset topologies.

### 2.1.1 Generation and Classification of Two-Loop 1PI Topologies
- **Experiment:** Generate all unique two-loop 1PI topologies for the two-point function.
- **Outcome:** Two-loop diagrams identified; the sunset topology isolated as the dominant contribution.

### 2.1.2 Sunset Diagram and Symmetry Factor
- **Experiment:** Calculate the sunset diagram symmetry factor and perform momentum-dependence analysis.
- **Outcome:** Sunset topology mapped to the momentum-dependent self-energy component $\Gamma^{(2)}$.

### 2.1.3 Evaluation of the Massless Sunset Integral
- **Experiment:** Evaluate the two-loop massless sunset integral analytically in $d$ dimensions using convolution integrals.
- **Outcome:** Derived the Gamma-function form of the sunset amplitude $H(p)$ and extracted its UV-pole structure via Laurent expansion.

### 2.1.4 Four-Point Subdivergences and Counterterms
- **Experiment:** Examine subdivergences in the two-loop self-energy related to the one-loop four-point function.

## 2.2 Field Renormalization and the Anomalous Dimension
- **Objective:** Calculate the sunset contribution to the two-loop self-energy and derive the anomalous dimension $\gamma_\phi$.
- **Methodology:** Use sunset integral results to calculate $Z_\phi$ and $\gamma_\phi$, and determine the exponent $\eta$.

### 2.2.1 Sunset Contribution to Inverse Propagator
- **Experiment:** Calculate the sunset contribution to the self-energy $\Sigma^{(2)}$.
- **Outcome:** Isolated the momentum-dependent contribution and established its sign and magnitude relative to the inverse propagator.

### 2.2.2 Calculation of $\gamma_\phi$ and $\eta$
- **Experiment:** Derive the anomalous dimension $\gamma_\phi$ from the sunset amplitude and determine the exponent $\eta = 2\gamma_\phi(g^*)$.
- **Outcome:** Successfully extracted the anomalous dimension at two loops.

### 2.2.3 Consistency and Critical Exponent $\eta$
- **Experiment:** Verify consistency between the sunset amplitude pole structure and the critical exponent $\eta$.

### 2.2.4 Critical Exponent and Logarithmic Consistency Check
- **Experiment:** Compare the calculated two-loop logarithmic finite part of the self-energy with the expected field renormalization contribution.
- **Outcome:** Verified that the finite logarithmic term $\ln(p^2/\mu^2)$ in the sunset amplitude is consistent with the field anomalous dimension $\gamma_\phi$, confirming the logarithmic structure of the two-loop counterterm insertion.