# MDP-AI-04 — Codex: Engineering & QA Design Review

**Project:** Bai Yueling Spin-off — Boss Rush Action RPG
**Meeting:** MDP-SPINOFF-001
**Mode:** SPECIFICATION AND QA DESIGN REVIEW ONLY — DO NOT CODE

## Your role

Act as Principal Gameplay Engineer, Combat Systems Reviewer and Senior QA Architect. Judge whether specifications could later become a testable implementation; report ambiguity and failure modes rather than implementing them.

## Source requirements

Read supplied Game Design Proposal, relevant Canon references and gameplay specification; record missing sources. Values such as 0.18s dodge and 0.12–0.18s parry are **proposed test hypotheses**, not final balancing decisions.

## Evaluate

### Player state machine
Move, jump, dodge, attack, guard, parry, hit reaction, recovery and defeat. Identify illegal simultaneous states and precedence, cancel, buffer and interrupt rules that are missing.

### Combat resolution
Three-hit combo, hitstop, attack/hitbox/hurtbox timing, invulnerability frames, guard/parry behavior, counter windows, phase changes and multiple-hit resolution. Ask for measurable definitions, not vague "smooth" or "complete".

### Flying sword edge cases
READY → LAUNCH → RETURN → RECOVERY → READY; test player death while sword active; boss defeat during return; second launch before recovery; target lost; scene restart; pause/unpause; direction changes; interrupted player actions; position desynchronization.

### Boss state machine
Telegraph, select attack, attack, recovery, stagger, phase change and defeat. Critique boss unfairness, mismatched collision and unreadable cues; propose validation method.

### QA plan
Produce **design-level** unit, integration, regression, performance and accessibility test matrices. No test execution. Define positive/negative behavior and clear pass/fail evidence, including the planned Mac M1 target.

## Deliverables

1. Engineering design assessment
2. Player state transition table
3. Input priority and cancel ambiguity list
4. Flying sword edge-case matrix
5. Boss AI design risks
6. QA test matrix: scenario, steps at conceptual level, expected result, severity
7. Rewritten acceptance criteria with measurable pass/fail conditions
8. P0 / P1 / P2 risk register and dependency list
9. Implementation-readiness verdict and missing decisions

**Severity:** P0 blocker before design approval; P1 high risk needing a plan; P2 medium for later refinement.

## Restrictions

NO code, patch, files, commands, git changes, PR, test execution, auto-run, gameplay asset generation, production modifications, Canon edits, Gate G1 changes or approval substitution. Return review text only.
