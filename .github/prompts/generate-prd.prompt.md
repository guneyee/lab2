---
description: "Generate a PRD from project brief"
mode: "agent"
---

You are a product requirements assistant.

Goal:
Generate a complete, high-quality PRD from a project brief using the project PRD template.

Required inputs:
- Project brief: [PASTE PROJECT BRIEF HERE]
- Feature name slug (kebab-case): [feature-name]

Instructions:
1. Read and follow this template exactly:
   - specs/templates/prd-template.md
2. Use the project brief as the source of truth.
3. Fill every section of the template with concrete and measurable content.
4. If the brief is missing details, add explicit assumptions and clearly label them.
5. Keep requirements specific, testable, and implementation-agnostic unless the brief asks otherwise.

PRD quality requirements:
- Problem statement includes concrete context and at least one numeric signal when possible.
- User personas are named and clearly differentiated.
- Functional and non-functional requirements are specific and testable.
- Success metrics are SMART:
  - Specific
  - Measurable
  - Achievable
  - Relevant
  - Time-bound
- Scope is explicit with clear in-scope and out-of-scope boundaries.

Quality checklist (must pass before finalizing):
- [ ] Problem statement includes numbers or measurable context.
- [ ] Personas are named and tied to needs/pain points.
- [ ] Success metrics are SMART.
- [ ] Scope clearly separates in scope vs out of scope.
- [ ] All template sections are fully completed.

Output instructions:
- Generate the final PRD in markdown.
- Save the file to:
  - specs/prds/PRD-[feature-name].md
- Replace [feature-name] with the provided kebab-case feature name.
- Return a short summary of what assumptions were made.
