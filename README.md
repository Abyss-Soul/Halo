# Halo

*A small eternity, squandered beneath the stars.*

Some nights, we stay beneath the stars long after there is anything left to say. We invent constellations, lend distant lights the names of people we miss, and let the hours go unaccounted for.

Halo is what we call the brightness that follows us home. It settles around ordinary things—a window, an unfinished letter, a name—and stays a little longer than it should.

We gave that name to this small corner of our work: a place where an idea can find something to lean on, the freedom to wander, and company through the long nights. Here, it has time to grow into something beautiful.

Every algorithm deserves a light of its own.

## What is Halo?

Halo is an infrastructure framework for placement and routing algorithms. It brings together foundational data structures, chip design models, task scheduling, and hardware resource management, giving algorithm developers a shared foundation for building and running their work.

Its intended role is similar to a game engine for game developers or a machine learning framework for researchers: provide the machinery so people can focus on their algorithms.

Halo is designed to provide:

- **Data:** geometry, graphs, spatial indexes, netlists, placement models, and routing resources.
- **Execution:** dependency-aware task scheduling, parallel execution, and resource coordination.
- **Hardware:** access to compute devices and memory through backend interfaces.
- **Integration:** language SDKs, a versioned C ABI, and a common algorithm registration interface.

The default developer experience will use **prebuilt Halo libraries**. Algorithm authors will build their own code and lightweight SDK wrappers without rebuilding the engine. Building Halo from source will remain an option.

> **Project status:** Halo is in the architecture and design phase. This repository currently contains project documentation and its license. The engine, SDKs, algorithms, and platform packages described below are planned; no runnable release is available yet.

## Roadmap

**✅ Completed · ⌛️ In progress · ⬜ Planned**

| Status | Area | Scope |
| :---: | --- | --- |
| ✅ | Project foundation | Name, project scope, initial documentation, and Apache-2.0 license. |
| ⌛️ | Architecture and API design | Module boundaries, ownership, language interfaces, and algorithm integration. |
| ⬜ | Foundational data structures | Typed IDs, arenas, geometry, graphs, and spatial indexes. |
| ⬜ | Placement and routing database | Cells, instances, pins, nets, layers, placement, tracks, routing grids, and blockages. |
| ⬜ | Task runtime | Task graphs, dependencies, parallel execution, cancellation, and completion tracking. |
| ⬜ | Resource scheduling | CPU execution budgets, memory requirements, and device-aware task submission. |
| ⬜ | Hardware backends | CPU support first; GPU backends as the compute interface develops. |
| ⬜ | Bulk data access | Batched reads and updates, with explicit ownership and access lifetimes across languages. |
| ⬜ | Language SDKs | C, C++, and Rust first; Python in a later phase. |
| ⬜ | Algorithm integration | A shared registry for built-in algorithms and optional extensions. |
| ⬜ | Binary distribution | Prebuilt engine and SDK packages, plus an optional source-build workflow. |
| ⬜ | Cross-platform support | Windows, Linux, and macOS builds and validation. |
| ⬜ | Quality and performance | Correctness tests, SDK compatibility checks, and reproducible benchmarks. |

## Implementation and SDKs

The core infrastructure will be written in **Rust**. Algorithm implementations may use **C, C++, or Rust**, with **Python** support planned later.

| Layer / SDK | Design | Status |
| --- | --- | :---: |
| Rust engine | Data storage, execution runtime, hardware interfaces, and engine services. | ⬜ |
| C SDK | Public headers and a versioned C ABI over the prebuilt engine. | ⬜ |
| C++ SDK | C++ types, RAII, and callback adapters over the C ABI. | ⬜ |
| Rust SDK | Safe Rust wrappers over the prebuilt engine's C ABI. | ⬜ |
| Python SDK | Python APIs and prebuilt native components for supported platforms. | ⬜ Later |

Prebuilt packages will target specific operating systems and architectures. SDK and engine versions will declare their compatibility requirements.

## Target platforms

| Operating system | Status |
| --- | --- |
| Windows | ⬜ Planned |
| Linux | ⬜ Planned |
| macOS | ⬜ Planned |

Hardware backend availability will be documented separately for each platform.

## Algorithms and extensions

Research algorithms are developed in **independent repositories** against the Halo SDK. They can be considered for integration after technical and licensing review.

| Category | Role | Delivery |
| --- | --- | --- |
| Research | New methods, experiments, and academic implementations maintained outside Halo. | Independent projects using the SDK. |
| Built-in | Reviewed algorithms whose licensing permits inclusion in the main Halo distribution. | Built and shipped with Halo, ready to call. |
| Extension | Reviewed integrations with separate licensing, including research-use algorithms that require additional commercial authorization. | Optional adapters and separately obtained or distributed implementation packages. |

Extensions retain their own license terms. Halo will distribute an extension's source or binaries only when the relevant permissions cover that distribution. Otherwise, users obtain the implementation from its rights holder and connect it through the adapter.

Algorithm authors will use the same registration contract wherever practical, allowing a research implementation to become a built-in algorithm or extension without requiring a change of implementation language.

## License

Halo is licensed under [Apache-2.0](LICENSE). Incorporated third-party components retain any required license notices. Separately licensed extensions are governed by their own terms.

## After Hours 😈

*Experimental romance. Peer review pending.*

1. You can't hide loving one person. But if you love two, you'd better hide it well!!! 🤫😈
2. When loving two people becomes impossible to hide, fall for a third and redistribute the drama. 🔀😈
3. Never ask a woman if she's single. If she likes you, she's single. 😉😈

