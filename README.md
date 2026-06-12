# Contribution 1: Add a way of public view as member role (or similar)

**Contribution Number:** 1  
**Student:** Tiago  
**Issue:** https://github.com/bluewave-labs/checkmate/issues/2751  
**Status:** Phase I Complete

---

## Why I Chose This Issue

Checkmate is an open-source uptime/monitoring dashboard, and issue #2751 asks for a way to share a "public view" — a visitor role that can browse the dashboard and monitoring data without being able to change anything. Today the closest thing is the `demo` role, but it carries artificial restrictions (it can't be deleted, can't be assigned through the edit-user form, and isn't reachable via the normal invite flow) that keep it from serving as a real public viewer. The fix is to relax those unnecessary restrictions so the role behaves like a proper read-only member, while keeping every write operation (creating/editing monitors, managing team members) firmly blocked.

I chose this issue because it sits right in the role-based access control (RBAC) layer, which is something I want to understand deeply, and because the change is specific and bounded rather than a broad refactor. Checkmate enforces roles at four layers — the Mongoose schema enum, JWT middleware, the service layer, and client-side Joi validation — so working through it means tracing one concept cleanly from the database model up to the React/Redux UI. The codebase already has clear conventions to match (the existing four-role system and `canManageRole` logic), the affected files are well-scoped, and the security-sensitive nature of the change makes it a good exercise in reasoning carefully about what a user can *do* versus what they can *see*. I hope to come away more comfortable with full-stack permission systems and with contributing to an established open-source project's contribution workflow.

---

## Understanding the Issue

### Problem Description

[In your own words, what's broken or missing?]

### Expected Behavior

[What should happen?]

### Current Behavior

[What actually happens?]

### Affected Components

[Which parts of the codebase are involved?]

---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. [Step 1]
2. [Step 2]
3. [Observed result]

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
