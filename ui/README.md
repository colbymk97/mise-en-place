# ui/

Agents for reviewing and improving user interfaces.

## Agents

### [design-review](design-review.md)

Structured UI critique — use it when a component feels off, before a code review, or to audit an entire project for design consistency.

**Adapts to what you give it:**

| Input | What it does |
|---|---|
| Single component or description | Deep critique against standards and Designer Profile |
| Project directory | Adds cross-component consistency checks and convention discovery |
| + Brand palette | Also flags colors that don't comport with the palette |

**Key output sections:** Critical Issues · Minor Issues · Consistency Issues · Brand Palette Deviations · Aesthetic Flags · Verdict

The Designer Profile (aesthetic preferences) and Brand Palette are both customizable blocks inside the system prompt — clearly marked so you can swap in your own without touching the rest.
