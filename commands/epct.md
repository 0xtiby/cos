---
description: EPCT Implementation Methodology - Streamlined
---

# EPCT: Explore - Plan - Code - Test

## Phase 1: EXPLORE

**Objective**: Gather comprehensive context efficiently

### Actions:

- **Codebase analysis**: Use parallel agents to map relevant files
- **Pattern identification**: Find similar implementations to follow
- **Dependency check**: Verify required tools/libraries exist

### Success criteria:

- Clear understanding of existing patterns
- Identified all files needing modification
- Found reference implementations

## Phase 2: PLAN

**Objective**: Design implementation strategy

### Create plan covering:

- **Scope**: What exactly will change
- **Approach**: How to implement (following existing patterns)
- **Testing**: Which tests to run/create
- **Risks**: Potential issues and mitigation

### Decision point:

- If scope is clear : proceed to CODE
- If unclear : ask targeted questions only

## Phase 3: CODE

**Objective**: Implement following project standards

### Implementation rules:

- **Follow existing patterns** (naming, structure, style)
- **Minimal scope** - change only what's necessary
- **Quality first** - readable code over clever code
- **Auto-format** when complete

### Quality gates:

- Code matches project conventions
- Passes linting/type checking
- No unnecessary changes

## Phase 4: TEST

**Objective**: Verify implementation works

### Testing strategy:

1. **Quick validation**: Run linting and type checking
2. **Focused testing**: Test only modified functionality
3. **Integration check**: Verify changes don't break existing features

### Escalation:

- Minor issues : fix and continue
- Major issues : return to PLAN phase

## Execution Principles

- **Parallel when possible**: Use multiple agents for independent tasks
- **Fail fast**: Catch issues early in each phase
- **Context aware**: Adapt methodology to project size/complexity
- **Incremental**: Prefer small, testable changes

## Success Metrics

Correctness > Completeness > Speed
Follows project standards
Minimal surface area of change
All quality gates passed
