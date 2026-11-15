> **PRIMARY PROJECT CONTEXT** — Read this file before work. Keep it concise, current, and actionable. Do not use README.md as development context or edit it without explicit user authorization.

# CatalystUI Project Contract

`lib-catalyst-c` is the native C ABI implementation of the CatalystUI model. The model describes the categorization (Domains), representation (Stack), and transformation (Connectors) of information between humans and information systems. Implement the model as specified; do not invent new semantics or architectural requirements.

## Working Rules

- Inspect relevant source, instructions, and Git state first. Preserve unrelated changes and keep work narrowly scoped to the user's request.
- Prefer simple, explicit implementations. Avoid speculative abstractions, duplicate systems, dependencies, and unnecessary layers. Do not add unrequested implementations or scaffolding.
- Consult the applicable CatalystUI specifications and `lib-core-c` contracts before defining overlapping concepts. Do not duplicate foundational types, status codes, memory, or text APIs. Do not add a dependency without authorization.
- Use public C ABI contracts in `include/` and implementations in `src/`. Keep native platform details private where practical. Document ownership, lifetimes, invariants, and errors at public API boundaries.
- Preserve portability and the language standards selected by each target preset. Do not assume native integer widths, pointer sizes, byte order, or host/target equivalence.
- Reuse the pinned `build-cmake` submodule and existing target conventions. Keep authored configuration separate from generated files and build artifacts; do not commit generated output.
- Relevant builds are allowed. Do not create automated tests, test harnesses, or custom CI workflows unless explicitly requested. The programmer owns manual verification. Report actual checks and unverified behavior; suggest at most 2–3 focused manual checks when applicable.
- Preserve Apache-2.0 licensing and required attribution. Preserve the existing Git author/committer identity where supported; every created or amended commit must include `Co-authored-by: Codex <noreply@openai.com>`.
- Keep documentation focused on current contracts and architecture, not task histories or agent memory. Maintain persistent instructions here; keep README.md human-facing.
