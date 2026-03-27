# Memo: Hybrid Workflow for AI-Assisted (Agentic) Coding

## Purpose

Preserve the speed benefits of AI-assisted coding while maintaining deep internalization of system behavior, architecture, and implementation details. This workflow treats AI as an implementation accelerator while ensuring the developer remains responsible for system reasoning.

## Core Principle

Use AI to accelerate typing and repetitive implementation, but force human reasoning at the stages that build mental models: problem definition, algorithm design, and system validation.

## Recommended Workflow

1. Human problem modeling: define inputs, outputs, constraints, invariants, performance targets, and failure modes.
2. Architecture exploration: ask AI to propose multiple designs and compare tradeoffs.
3. Human algorithm design: write pseudocode or a structured outline of the core logic.
4. AI implementation: generate code for the defined algorithm and supporting components.
5. Human simplification pass: rewrite or compress generated code to align with architecture and style.
6. AI test generation: create edge-case tests, fuzz tests, and stress scenarios.
7. Adversarial review: ask AI to critique the design and identify possible bugs or race conditions.

## Cognitive Goals of the Workflow

- Maintain deep internalization of system invariants and data flow.
- Avoid passive code review mode by forcing active reasoning steps.
- Keep implementation speed benefits provided by AI tools.
- Encourage architectural thinking and adversarial design validation.

## References and Evidence

- Claim: AI coding assistants can reduce toil and save time on repetitive work, documentation, testing, and related coding tasks, but their gains are uneven across task types and codebase contexts. References: [Pandey et al., 2024, "Transforming Software Development: Evaluating the Efficiency and Challenges of GitHub Copilot in Real-World Projects"](https://arxiv.org/abs/2406.17910), [Bakal et al., 2025, "Experience with GitHub Copilot for Developer Productivity at Zoominfo"](https://arxiv.org/abs/2501.13282).
- Claim: Generated code quality cannot be assumed from functional correctness alone; maintainability, readability, and non-functional quality remain active concerns in both research and practice. References: [Liu et al., 2023, "Refining ChatGPT-Generated Code: Characterizing and Mitigating Code Quality Issues"](https://arxiv.org/abs/2307.12596), [Sun et al., 2025, "Quality Assurance of LLM-generated Code: Addressing Non-Functional Quality Characteristics"](https://arxiv.org/abs/2511.10271), [Molison et al., 2025, "Is LLM-Generated Code More Maintainable & Reliable than Human-Written Code?"](https://arxiv.org/abs/2508.00700).
- Claim: The memo's "human owns the reasoning, AI accelerates implementation" workflow is partly an engineering prescription rather than a settled empirical result. The strongest direct support comes from studies showing that prompt style, interaction mode, and task decomposition materially affect developer workload and outcomes. References: [Brandebusemeyer et al., 2025, "Developers' Experience with Generative AI -- First Insights from an Empirical Mixed-Methods Field Study"](https://arxiv.org/abs/2512.19926), [Pandey et al., 2024](https://arxiv.org/abs/2406.17910).
- Claim: The internalization argument is an inference from memory research: people tend to retain self-generated material better than passively consumed material. Applying that mechanism to coding is plausible, but it is still an extrapolation rather than a direct coding-specific proof. References: [Slamecka and Graf, 1978, "The generation effect: Delineation of a phenomenon"](https://doi.org/10.1037/0278-7393.4.6.592), [MacLeod et al., 2010, "The production effect: Delineation of a phenomenon"](https://doi.org/10.1037/a0018785).
