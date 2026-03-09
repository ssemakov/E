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
