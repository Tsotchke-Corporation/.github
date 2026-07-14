<div align="center">

# Tsotchke Corporation

### Computational research, made executable.

**Quantum computing · scientific machine intelligence · compilers and runtimes · accelerated systems**

[Website](https://tsotchke.net) · [Public research](https://github.com/tsotchke) · [Live QRNG API](https://api.tsotchke.net/v1/docs/) · [Repositories](https://github.com/Tsotchke-Corporation?tab=repositories) · [Contact](mailto:dev@tsotchke.net)

</div>

Tsotchke Corporation is the engineering home around a public research
portfolio spanning quantum computing, many-body physics, machine learning,
programming languages, numerical methods, and low-level systems. We build the
parts that ambitious computational ideas usually leave implicit: the compiler,
the native kernel, the simulator, the validation harness, and the interface
that makes the result usable.

Our most characteristic work crosses boundaries. Neural networks become
variational wavefunctions for quantum spin systems. Representation theory
becomes a low-dependency C library. Calculus becomes a compiler primitive.
Quantum algorithms are exercised through state-vector, Clifford, tensor-network,
and noisy-system models. Transformer inference is pushed both upward into Apple
GPU matrix units and downward into fixed-point BASIC on DOS-class machines.

## The portfolio in one view

| Layer | What we build | Representative public work |
| --- | --- | --- |
| **Mathematical foundations** | Executable geometry, symmetry, differentiation, topology, and numerical methods | [Eshkol](https://github.com/tsotchke/eshkol), [libirrep](https://github.com/tsotchke/libirrep), [Quantum Geometric Tensor](https://github.com/tsotchke/quantum_geometric_tensor) |
| **Scientific models** | Neural quantum states, spin Hamiltonians, quantum circuits, tensor networks, error models, and PDE-constrained learning | [Spin-Based Neural Computation](https://github.com/tsotchke/spin_based_neural_network), [Moonlab](https://github.com/tsotchke/moonlab), [PINN](https://github.com/tsotchke/PINN), [PIMC](https://github.com/tsotchke/PIMC) |
| **Compute systems** | Native compilers, GPU kernels, quantized inference, portable runtimes, and multi-model orchestration | [Tensorcore](https://github.com/tsotchke/tensorcore), [GPT2-BASIC](https://github.com/tsotchke/gpt2-basic), [LLM Arbitrator](https://github.com/tsotchke/llm-arbitrator) |
| **Running software** | Versioned APIs, supervised browser workers, integration contracts, health checks, and reproducible deployment | [Quantum RNG API](https://github.com/Tsotchke-Corporation/Quantum-RNG-API), [ULG](https://github.com/Tsotchke-Corporation/ulg) |

## Flagship research

### Spin-Based Neural Computation Framework

**Neural computation used as an instrument for many-body physics—not merely as a predictor.**

[Spin-Based Neural Computation](https://github.com/tsotchke/spin_based_neural_network)
is a pure-C research environment built around neural-network quantum states,
classical spin models, topological quantum computing, and physics-informed
learning. Its MLP, RBM, and complex-RBM variational wavefunctions are trained
with stochastic reconfiguration across TFIM, Heisenberg, XXZ, J1–J2,
Kitaev–Heisenberg, and kagome Heisenberg Hamiltonians. Learned states can be
checked against finite-system Lanczos references, lattice symmetries, fidelity
diagnostics, and topological observables rather than evaluated by loss alone.

The same codebase includes Berry phase, Chern/TKNN and winding calculations;
Hilbert-space Majorana braiding; toric-code error-correction primitives;
Kitaev–Preskill topological entanglement entropy; classical Ising, Kitaev, and
disordered-spin substrates; and PDE residual losses for Schrödinger, Maxwell,
heat, wave, and Navier–Stokes systems. The important contribution is the bridge
between machine-learned ansätze, exact numerical methods, symmetry, and
topological quantum structure in one inspectable C framework.

### Moonlab

**A multi-regime quantum-computing laboratory with a native C core.**

[Moonlab](https://github.com/tsotchke/moonlab) goes substantially beyond a
single state-vector demo. It combines dense state-vector simulation, an
Aaronson–Gottesman Clifford backend, matrix-product-state and density-operator
methods, DMRG/TDVP, noise channels, measurement models, error mitigation,
entanglement metrics, and topology-oriented band-structure primitives. Its
algorithm and application surfaces include Grover, VQE, QAOA, QPE, Bell tests,
quantum chemistry, quantum error correction, and post-quantum cryptographic
primitives, with Python, Rust, and JavaScript bindings around the C runtime.

Moonlab is the clearest expression of our quantum-computing systems work: not a
claim of physical quantum hardware, but a set of explicit computational models
whose assumptions, numerical paths, and validation tests can be inspected.

### Quantum Geometric Tensor Library

**Geometry treated as an executable optimization and systems abstraction.**

[Quantum Geometric Tensor](https://github.com/tsotchke/quantum_geometric_tensor)
is a broad C framework for hybrid classical–quantum learning. It organizes
quantum-state geometry, natural-gradient methods, Berry curvature, tensor
networks, error-correction and algorithm modules, distributed execution, and
heterogeneous CPU/CUDA/Metal backends behind a common computational substrate.
Its value is architectural: it investigates how geometric information can
shape optimization, state representation, compilation, and distributed
learning rather than remaining an after-the-fact diagnostic.

### libirrep

**Representation theory lowered into practical systems infrastructure.**

[libirrep](https://github.com/tsotchke/libirrep) is a dependency-light C11
library for SO(3), SU(2), O(3), and SE(3) representation theory. It exposes
spherical harmonics, Wigner matrices, Clebsch–Gordan coupling, tensor products,
equivariant-network layers, lattice and point-group tools, spin Hamiltonians,
exact diagonalization, entanglement diagnostics, and a substantial stabilizer
quantum-error-correction substrate through a guarded C ABI. It is also a live
dependency of the spin-based neural framework, where abstract symmetry becomes
an operational part of a larger scientific workflow.

## Languages, learning, and compute

### Eshkol

**A language built around the idea that calculus belongs in the compiler.**

[Eshkol](https://github.com/tsotchke/eshkol) is a Scheme-derived language for
mathematical computing and AI, compiled through LLVM and also delivered through
a WebAssembly runtime. Symbolic, forward-mode, reverse-mode, and higher-order
automatic differentiation are language-level capabilities alongside vector
calculus, numerical and machine-learning libraries, a REPL, package tooling,
and deterministic arena-based memory management. The project asks what
scientific software looks like when differentiable programming is part of the
language semantics rather than a framework layered on top.

### Tensorcore

**A CUDA-like kernel layer for Apple Silicon's matrix hardware.**

[Tensorcore](https://github.com/tsotchke/tensorcore) presents GEMM, attention,
convolution, normalization, RoPE, optimizer, quantized GEMV, GGUF, and
collective-communication primitives through a compact C ABI. It dispatches
across Apple GPU families while retaining CPU portability and explicit
correctness/benchmark gates. The broader goal is to make Metal matrix units a
usable training and inference substrate instead of a collection of isolated
application-specific kernels.

### GPT2-BASIC

**A study in substrate portability, not a claim about model scale.**

[GPT2-BASIC](https://github.com/tsotchke/gpt2-basic) implements a local,
fixed-point transformer and assistant runtime in BASIC for FreeDOS/486-class
systems. It includes integer inference, DOS-loadable model artifacts,
hot-swappable local knowledge packs, indexed recall, quantized and streamed
weight modes, and machine-readable QEMU validation. The result demonstrates
that the transformer execution model can survive severe constraints without a
GPU, Python, a cloud service, or even a modern operating system.

## Quantum randomness: from research code to a live API

The randomness work has a visible technical lineage:

1. [Quantum RNG](https://github.com/tsotchke/quantum_rng) provides the compact
   C implementation: state-vector evolution, Born-rule measurement, Grover and
   Bell/CHSH experiments, hardware/OS entropy collection, continuous health
   tests, and CPU/GPU execution paths.
2. [Moonlab](https://github.com/tsotchke/moonlab) carries that work into a
   larger quantum-computing simulator with additional simulation regimes,
   algorithms, noise models, and cryptographic primitives.
3. [Quantum RNG API](https://github.com/Tsotchke-Corporation/Quantum-RNG-API)
   turns the current engine into a versioned, tested, automatically deployed
   service with explicit provenance, typed outputs, OpenAPI documentation, and
   runtime health information.

The public service is available at
[api.tsotchke.net](https://api.tsotchke.net/v1/docs/). Its documentation is
deliberate about scope: the quantum behavior is simulated, CHSH validates the
simulation model, and output is conditioned with health-tested operating-system
and CPU entropy. It does not imply access to physical quantum hardware.

## Corporate public laboratories

| Project | What is actually public |
| --- | --- |
| [ULG](https://github.com/Tsotchke-Corporation/ulg) | A browser-native scientific-computing integration lab: supervised service workers, explicit capability probes, WebGPU/CPU parity and fallback evidence, closure-table contracts, and scoped Eshkol/Moonlab WASM handoffs. It is presented as an integration scaffold, not as a finished multiphysics solver. |
| [SolanaQuantumFlux](https://github.com/Tsotchke-Corporation/SolanaQuantumFlux) | TypeScript SDK source, integration examples, and documentation for an on-chain randomness service. |
| [Quantum Quake](https://github.com/Tsotchke-Corporation/quantum-quake) | A public research adaptation exploring auditable quantum and quantum-inspired computation inside a QuakeSpasm runtime. |
| [OBLITERATUS](https://github.com/Tsotchke-Corporation/OBLITERATUS) | A maintained public fork used for reproducible refusal-geometry and mechanistic-interpretability experiments. |
| [Logo Lab](https://github.com/Tsotchke-Corporation/logo-lab) | A browser-based Möbius-material, rendering, and visual-identity laboratory. |

## More open-source work

The broader [@tsotchke](https://github.com/tsotchke) portfolio also includes:

| Project | Contribution |
| --- | --- |
| [PINN](https://github.com/tsotchke/PINN) | A C implementation of physics-informed neural-network losses for Schrödinger, Maxwell, heat, wave, and Navier–Stokes equations. |
| [PIMC](https://github.com/tsotchke/PIMC) | An interactive Java path-integral Monte Carlo environment for quantum particles in harmonic, Morse, double-well, and anharmonic potentials. |
| [LLM Arbitrator](https://github.com/tsotchke/llm-arbitrator) | A TypeScript/MCP framework for capability-based routing and coordination across local language-model providers. |
| [Classical RNG](https://github.com/tsotchke/classical_rng) | A compact C random-number utility with examples for games and security-oriented applications. |
| [Simple MNIST](https://github.com/tsotchke/simple_mnist) | A deliberately small, readable two-hidden-layer neural network in C. |
| [Asteroids](https://github.com/tsotchke/asteroids) | A compact C implementation of the classic game, reflecting the portfolio's continued interest in understandable native software. |
| [Homebrew Eshkol](https://github.com/tsotchke/homebrew-eshkol) / [Homebrew Moonlab](https://github.com/tsotchke/homebrew-moonlab) | Distribution taps for installing current public releases. |

## How the work connects

- **Symmetry becomes computation:** libirrep supplies representation-theory and
  physics primitives consumed by the spin-based neural framework.
- **A research line becomes infrastructure:** Quantum RNG led into Moonlab and
  then into the live, versioned Quantum RNG API.
- **Languages meet execution backends:** Eshkol, Tensorcore, and the broader
  native-compute work explore the path from mathematical expression to compiled
  and accelerated execution.
- **Research becomes observable:** ULG and the API projects expose capability,
  fallback, provenance, and health information instead of hiding runtime state
  behind a demo.

## Engineering posture

We prefer evidence to spectacle. Public repositories are expected to separate
implemented capability from roadmap, simulation from physical hardware,
measured performance from aspiration, and research evidence from production
assurance. Tests, numerical references, benchmark artifacts, ABI contracts,
health checks, and reproducible build paths are part of the work—not release
ceremony around it.

Project maturity varies from live service to pre-release research library and
explicit integration scaffold. Each repository is the authority for its current
status, supported claims, license, and verification commands.

## Work with us

We are open to research collaboration, technical partnerships, scientific
software development, and focused work on compilers, quantum-computing systems,
native ML infrastructure, or reproducible computational research.

For collaboration, licensing, or security inquiries, contact
[dev@tsotchke.net](mailto:dev@tsotchke.net).
