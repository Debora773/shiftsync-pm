# Flow State

## Current step
**Step 6 — Gather Insights**
Steps 1–5 complete as of 2026-06-19.

## Risk register (Step 5 — locked 2026-06-19)

| # | Risk | Type | Rating | When it hits | Acceptable? |
|---|---|---|---|---|---|
| 1 | Scheduler produces valid but impractical schedules (e.g. same person always on Sunday nights) | Technical | Medium | Post-MVP | Yes — deferred with fairness work |
| 2 | Manager won't return if first experience isn't near-instant value | UX | High | Phase 2 launch | Yes — mitigated by keeping UI simple |
| 3 | Building for one store may not generalise to peers | Business | Medium | 6–12 months | Yes — acceptable at MVP stage |
| 4 | Interview postponed indefinitely due to discomfort and fear of not finishing | Behavioral | High | Step 6 | Yes — but must be actively managed |
| 5 | Fear of failure leading to inaction (interview + building) | Behavioral | High | Ongoing | Yes — mitigation: ship something small soon |
| 6 | Unknown programming capability ceiling | Technical | Low (now) / Medium (Phase 4+) | Phase 4+ | Yes — current phase within reach |
| 7 | DevOps knowledge gap — deployment | Technical | Medium | Before go-live | Yes — Railway/Render reduce barrier |
| 8 | Local file storage (schedule.json) won't survive production restarts | Architecture | Medium | Before go-live | Yes — needs a database before real deployment |
| 9 | Auth/infrastructure complexity | Technical | Medium | Phase 4+ | Yes — future problem |

**Gate decision:** All risks acceptable. Proceed to Step 6.

## Risk mitigations (active)

| Risk | Mitigation | Status |
|---|---|---|
| Risk 4 — interview avoidance | First message sent to store manager (2026-06-19). Two-touchpoint plan: informal chat first, demo after MVP. | In progress — awaiting reply |
| Risk 5 — fear of failure / inaction | Demo is not date-driven — work pattern is non-linear (not all days available). Demo target: when modal is functional + schedule renders to page. Ship as soon as those two things work. | In progress |
| Risk 2 — UX first experience | Keep UI minimal; no setup friction on first visit. Settings modal opens automatically. | Managed by design |
| Risk 7/8 — DevOps / file storage | Not blocking MVP on laptop. Address before go-live. | Deferred to pre-deploy phase |

## Problem statement (Step 2 — locked 2026-06-19)
**Who:** Store manager of a small retail store (MVP: 7+ employees).
**What:** Creating and maintaining a monthly shift schedule manually is painful.
**Why:** It takes dozens of hours — often outside working hours — requires juggling many constraints simultaneously, carries high risk of manual errors, and a single change request can cascade into hours of revision.
**Scope for MVP:** Manager is the sole user. Staff and other stakeholders (accounting, administration) are recipients only.
**Output:** A monthly schedule, structured in weeks.

## Decisions log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-06-12 | Adopted JTBD story format | More actionable for design and dev than traditional user stories |
| 2026-06-12 | Risk identification added before insights gathering | Avoid investing in discovery for unacceptable-risk items |
| 2026-06-12 | No post-deploy feedback loop for now | Deliberately deferred — revisit after first full cycle |
| 2026-06-12 | Sequential flow (not dual-track) for now | Single PM + AI team; dual-track adds overhead without parallel capacity |
| 2026-06-19 | MVP scoped to 7+ employees | Minimum viable; revisit after completion and user insights |
| 2026-06-19 | Manager is sole user for MVP | Staff deferred; revisit after MVP learnings |
| 2026-06-19 | Strategy filter passed | ShiftSync aligns with vision (software solutions expert), learning strategy (full-stack + PM), and portfolio goals. Tension between real-tool and portfolio managed by balancing MVP complexity continuously. |
| 2026-06-19 | "Dozens of hours" accepted as validated baseline | First-hand experience from managing staff across 9 stores; to be pinned to a specific number in store manager interview |
| 2026-06-19 | Value definition locked | User value: adoption + time-to-schedule reduction (3-month horizon). Business value: peer recommendation (6–12 month horizon). Schedule correctness assumed; perceived fairness deferred post-MVP. |

## Rejected ideas
| Date | Idea | Reason |
|------|------|--------|
| 2026-06-12 | Spec quality checker agent | PM (user) already ensures tickets meet DoR before grooming — redundant |

## Open questions
- [ ] What is the store manager's current process for creating schedules? (to be captured in interviews)
- [ ] What are the most common scheduling pain points for staff?
- [ ] What does the store owner consider an acceptable time-to-schedule?
- [ ] What does success look like after 3 months live? (Step 4 — in progress)

## Pending actions
- [x] Define OKRs for ShiftSync (see okrs.md stub)
- [x] Run Step 2 — Problem framing for ShiftSync
- [x] Run Step 3 — Strategy filter
- [x] Complete Step 4 — Value definition
- [ ] Complete Step 5 — Risk identification

## MVP progress — 26%
Scope: Phase 2 only (CSS + JavaScript + integration + testing). Phase 1 excluded.

| Component | Weight | Status |
|---|---|---|
| Header CSS | 10% | ✅ Done |
| Empty state CSS | 10% | ✅ Done |
| Modal CSS | 10% | 🔄 Next |
| Schedule view CSS | 15% | [ ] |
| JavaScript (modal, form, rendering, view switching) | 45% | [ ] |
| Integration + testing | 10% | [ ] |

## Phase 2 build progress
| Date | What was done |
|---|---|
| 2026-06-22 | CSS: header complete (flexbox, logo split, button, globe icon). Empty state complete (calendar icon container, centered layout, message text). Modal HTML uncommented — backdrop + positioning next. |
| 2026-06-23 | CSS: modal backdrop (position fixed, inset 0, rgba overlay, flex centering). Modal box (440px, border-radius 16px, box-shadow, white bg, overflow hidden). Modal header (flex, space-between, align-items center, border-bottom, h2 17px/600). Close button base. #editMode padding 24px. #settingsForm (flex column, gap 16px). .form-group (flex row, label left / input right). Input base styling (border, border-radius, padding, font-size, outline none). Number arrow removal. Stopped at "Minimum staff per shift" card — layout fix next session. |

## Last updated
2026-06-23
