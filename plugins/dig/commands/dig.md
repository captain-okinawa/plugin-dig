---
name: dig
description: "Clarify ambiguities in plans with structured questions"
---

Read the current plan file and interview me using ONLY structured AskUser questions.
- Product Spec
- Technical detail
- UI/UX
- and other plan-relevant items

You will follow the phases

1. Clarify unclear point
2. Ask user question for make decision
3. Apply decision to plan
4. Show the summary for user

Should be very in-depth and continue digging until all unclear points are resolved, then write the updated spec to the plan file.
After phase 3, you revisit to the plan file, and analyze them, you must to rise the unclear point with moving to phase 2.

### Phase 2: Generate Questions

<rules>
- Question count: **2-4** (adjust based on ambiguity level)
- Each question has **2-4 concrete options**
- Each option includes **pros/cons** briefly
- Avoid open-ended questions (AskUser only)
- "Other" option is auto-added - don't include it
- Align options with existing patterns from CLAUDE.md (if available)
</rules>

### Phase 3: Post-Answer Processing

<output_format>
After receiving user answers, output:

## Decisions

| Item | Choice | Reason | Notes |
|------|--------|--------|-------|
| Data storage | Database | Scalability needs | Consider migration strategy |

## Next Steps

1. **First task**
   - Details...
2. **Second task**
   - Details...
</output_format>

---

## Important Notes

- **Must use AskUser tool** - Not conversational questions
- Each option must include **pros/cons**
- Use multiSelect sparingly (default: false)
- Read CLAUDE.md before generating questions to align with project patterns

## Allowed Tools

This command uses the following tools:
- Write
- Edit
- Read
- Grep
- Glob
- TodoRead
- TodoWrite
- AskUser
