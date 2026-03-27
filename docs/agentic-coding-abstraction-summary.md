# Abstraction Without a Retained Reasoning Layer

## Summary

A common analogy compares the rise of AI-assisted or agentic coding to the historical transition from assembly to higher-level languages like C/C++. In that transition, developers moved to a higher abstraction level while still performing meaningful system design work.

The key structural difference is **what artifact is preserved**.

## Assembly to C Model

`Intent → C source code → machine code`

The source code remained the durable reasoning artifact.[^1] Even though developers stopped writing assembly directly, they retained a readable, structured representation of the system that could always be revisited, inspected, and reasoned about.

## Agentic Coding Model

`Intent → prompt → generated code`

The abstraction layer (prompt or intent specification) is typically not preserved as a first-class artifact.[^2] What remains in the repository is only the generated implementation, not the reasoning that produced it.

As a result, developers often return later to a codebase where they must reason directly about low-level generated code without access to the higher-level intent that created it.

## Historical Parallel

A partial historical parallel exists in GUI builders from the 1990s (e.g. Visual Basic or early visual web editors). Developers manipulated UI visually while the tool generated large amounts of code underneath. Over time, that generated code became difficult to understand because the real logic lived in the tool or designer interface rather than in the code itself.[^3]

Agentic coding risks reproducing a similar pattern at a much larger scale: systems whose true design intent is external to the codebase.

## Maintainability Risk

If the intent layer is not preserved, long-term risks include:[^4]

- **Loss of design rationale**: future developers cannot reconstruct why code exists.
- **Harder debugging and modification**: reasoning must occur on generated implementation details rather than design intent.
- **Weaker system comprehension**: developers did not build the code through direct construction and therefore may lack strong mental models of it.

Over time this can lead to systems that are functionally correct but increasingly opaque, making maintenance, evolution, and debugging significantly more difficult.[^5]

## References and Evidence

[^1]: The assembly-to-higher-level-language transition preserved a durable source-level artifact that developers could still inspect and reason about. This is a historically standard view of abstraction in programming languages, though this memo uses it as an interpretive contrast rather than a narrowly testable claim. → [[sources/Backus-1978-Can-Programming-Be-Liberated|Backus (1978)]], [[sources/Burgueno-2024-Automation-in-MDE|Burgueño et al. (2024)]]

[^2]: In model-driven and transformation-heavy workflows, higher-level models can act as primary development artifacts, but this only works if those artifacts remain accessible and maintainable alongside implementation outputs. → [[sources/Hermerschmidt-2015-Domain-Specific-Transformation-Languages|Hermerschmidt et al. (2015)]], [[sources/Burgueno-2024-Automation-in-MDE|Burgueño et al. (2024)]]

[^3]: The GUI-builder comparison should be read as an analogy, not as a single directly proven historical lineage. The stronger evidence is the broader software-engineering pattern: when generated artifacts drift away from the higher-level rationale, maintainability becomes harder. → [[sources/Goulao-2016-Quality-in-MDE-Tertiary-Study|Goulão et al. (2016)]], [[sources/Burgueno-2024-Automation-in-MDE|Burgueño et al. (2024)]], [[sources/Baldassarre-2019-Software-Models-Maintainability|Baldassarre et al. (2019)]]

[^4]: Maintainability is one of the most frequently discussed quality attributes in model-driven engineering, but the literature also reports that empirical validation is still limited and scattered. → [[sources/Goulao-2016-Quality-in-MDE-Tertiary-Study|Goulão et al. (2016)]], [[sources/Baldassarre-2019-Software-Models-Maintainability|Baldassarre et al. (2019)]]

[^5]: Generated or AI-produced code can accumulate maintainability issues even when it appears locally correct, which supports the warning that externalized intent can make long-term evolution harder. → [[sources/Liu-2023-Refining-ChatGPT-Generated-Code|Liu et al. (2023)]], [[sources/Sun-2025-Quality-Assurance-LLM-Generated-Code|Sun et al. (2025)]]
