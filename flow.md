# ShiftSync Product Development Flow

## Steps

1. **Intake** — Idea or user problem comes in.

2. **Problem framing** — If an idea: translate to *"What problem does this solve, and for whom?"*

3. **Strategy filter** — Does this align with business vision, strategy, OKRs, and roadmap? If no, park or discard.

4. **Value definition** — Define user value and business value. Answer: *"What does success look like from each perspective?"* Set measurable success metrics for both.

5. **Risk identification** — Identify technical, UX, and business risks. Rate each Low / Medium / High. Decide if risk level is acceptable before investing in discovery.

6. **Gather insights** — Run user interviews (store owner, store manager, staff). Gather input from internal stakeholders. Desk research. Analytics (when available). → Filter findings. → Prepare high-level stories in JTBD format. Use the Synthesis agent after interviews.

7. **Discuss with UI/UX and tech owner** — Present findings and stories. Collaborative discussion — not a handoff. Align on approach before prototyping.

8. **Prototype & test** — Build lightweight prototypes or wireframes. Validate with stakeholders.

9. **Iterate** — Run feedback loops with stakeholders until solution is validated.

10. **Write tickets** — Full specs in JTBD format, risks included, acceptance criteria defined. Prioritize into sprints.

11. **Groom with devs** — Walk through tickets. Devs ask questions, raise edge cases. Ticket must meet Definition of Ready before entering sprint.

12. **Develop**

13. **Test**

14. **Deploy**

15. **Retrospective** — What did we learn? What do we update in the flow, the product, or our assumptions?

---

## Definition of Ready (DoR)
A ticket is ready to groom when it has:
- [ ] JTBD story written
- [ ] Acceptance criteria defined
- [ ] Risks identified and rated
- [ ] Success metric linked
- [ ] No open blocking questions

## Definition of Done (DoD)
A feature is done when:
- [ ] Acceptance criteria all pass
- [ ] Tested (manual and/or automated)
- [ ] Deployed to production
- [ ] Success metric is measurable

---

## Agents in this flow

| Agent | Role |
|---|---|
| Store owner | Business decisions, ROI, final approvals |
| Store manager | Primary user — validates workflows, UI, scheduling behavior |
| Staff | End recipients — fairness, clarity, shift preferences |
| Tech owner | Feasibility, architecture, technical risk |
| UI/UX | Usability, design, interaction flows |
| Dev | Implementation, raises edge cases and spec gaps |
| Synthesis | Reads all interview outputs, extracts patterns and contradictions |
| Devil's advocate | Challenges assumptions and decisions before tickets are written |
