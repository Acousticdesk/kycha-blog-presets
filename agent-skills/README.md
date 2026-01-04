# Agent Skills for AI Agents

A curated collection of **battle-tested Agent Skills (SKILL.md definitions)** used daily in real-world AI engineering and agent-assisted development. These skills encode **repeatable patterns for planning, specification writing, domain reasoning, safety constraints, and deterministic execution** — helping agents produce **predictable, maintainable, production-ready software** instead of vibe-driven improvisation.

Learn more: [https://kycha-blog.org/posts/how-to-build-software-using-ai-agents-2026](https://kycha-blog.org/posts/how-to-build-software-using-ai-agents-2026)

---

## 🚀 Installing Agent Skills

1. Create a `.claude/skills` directory in your repository
2. Copy each skill folder into `.claude/skills/<skill-name>`
3. The agent will automatically detect and load the skills

### Team Workflow Recommendation

Add `.claude` to `.gitignore` so every developer can:

- use only the skills they need
- customize skills locally
- avoid polluting the shared repository

Below are descriptions and usage recommendations for each included skill.

---

## 🎯 `feature-spec-generator`

Transforms vague feature ideas into **clear, enforceable, implementation-ready specifications** that eliminate ambiguity, scope drift, and accidental reinterpretation. Built for **spec-driven development**.

### Suggested Workflow

- Ask the agent to generate a feature spec
  Example:
  `Generate a SPEC.md for migrating from LangSmith to LangFuse.`
- Review and refine the generated `SPEC.md`
- Then ask the agent to implement the feature strictly according to the spec
  Example:
  `Implement the feature defined in .claude/skills/feature-spec-generator/SPEC.md`

---

## 🔗 `backend-integration`

Ensures the **frontend implementation stays fully aligned with the Backend API** by referencing and strictly following the **Server API Specification**.

### Suggested Workflow

1. Open the backend repository
2. Ask the agent to generate an `ENDPOINTS.md` file, including interfaces, DTOs, and response models
3. Copy the file to `.claude/skills/backend-integration/ENDPOINTS.md`
4. Ask the agent to implement backend integration for the feature

### Pairing With Spec-Driven Development

This skill works best when combined with `feature-spec-generator`:

- Generate the feature spec first
- Then implement backend integration **based on the same source-of-truth spec**

This creates **consistent, deterministic, and verifiable AI-assisted development workflows**.
