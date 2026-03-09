# Abstraction Without a Retained Reasoning Layer

## Summary

A common analogy compares the rise of AI-assisted or agentic coding to the historical transition from assembly to higher-level languages like C/C++. In that transition, developers moved to a higher abstraction level while still performing meaningful system design work.

The key structural difference is what artifact is preserved.

## Assembly to C Model

`Intent -> C source code -> machine code`

The source code remained the durable reasoning artifact. Even though developers stopped writing assembly directly, they retained a readable, structured representation of the system that could always be revisited, inspected, and reasoned about.

## Agentic Coding Model

`Intent -> prompt -> generated code`

The abstraction layer (prompt or intent specification) is typically not preserved as a first-class artifact. What remains in the repository is only the generated implementation, not the reasoning that produced it.

As a result, developers often return later to a codebase where they must reason directly about low-level generated code without access to the higher-level intent that created it.

## Historical Parallel

A partial historical parallel exists in GUI builders from the 1990s (for example Visual Basic or early visual web editors). Developers manipulated UI visually while the tool generated large amounts of code underneath. Over time, that generated code became difficult to understand because the real logic lived in the tool or designer interface rather than in the code itself.

Agentic coding risks reproducing a similar pattern at a much larger scale: systems whose true design intent is external to the codebase.

## Maintainability Risk

If the intent layer is not preserved, long-term risks include:

- Loss of design rationale: future developers cannot reconstruct why code exists.
- Harder debugging and modification: reasoning must occur on generated implementation details rather than design intent.
- Weaker system comprehension: developers did not build the code through direct construction and therefore may lack strong mental models of it.

Over time this can lead to systems that are functionally correct but increasingly opaque, making maintenance, evolution, and debugging significantly more difficult.
