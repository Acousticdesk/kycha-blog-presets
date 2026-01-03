# Agent Skills for AI Agents

A curated collection of battle-tested Agent Skills (SKILL.md definitions) that I use daily in real-world AI engineering workflows. These skills encode repeatable patterns for planning, specs, domain reasoning, safety constraints, and deterministic execution - helping agents produce predictable, maintainable, and production-ready output instead of vibe-driven improvisation.

https://kycha-blog.org/posts/how-to-build-software-using-ai-agents-2026

## Installing Agent Skills

- Create a `.claude/skills` directory in your project repository (create the `.claude` folder first if it does not exist).
- Copy the entire skill folder into `.claude/skills/<skill-name>` so the agent can automatically detect and load it.

## Installation Recommendations

When working in a team, add the `.claude` folder to the `.gitignore` file. This helps each developer on the team use only the skills they need and they can customize the how they see fit.

Below you can find description and recommendations for each skill in the repository.

## feature-spec-generator

Turns vague feature ideas into clear, enforceable, implementation-ready specifications that prevent ambiguity, scope drift, and accidental re-interpretation during development. For **spec-driven development**.

### Development Workflow

- Ask the agent to create a spec for the feature. Example: `Let's generate a spec for the feature to migrate from LangSmith to LangFuse`.
- Find the generated `SPEC.md` file in the `.claude` repository.
- Review the spec file and make changes
- Ask the agent to implement the feature. Example `Implement the feature defined in the .claude/skills/feature-spec-generator/SPEC.md` file.

## backend-integration

Ensures that the **front-end implementation** remains fully compatible with the Backend Server API by referencing and strictly adhering to the Server API Specification.

### Development Workflow

- Switch to the backend repo.
- Ask the agent to generate an `ENDPOINTS.md` file. Example:
  `Rigorously review all the server endpoints and create an ENDPOINTS.md file where you capture all the endpoints interfaces and data models used in this endpoints including DTOs and responses`.
- Copy the `ENDPOINTS.md` file and put it into the `.claude/skills/backend-integration/ENDPOINTS.md` file.
- Ask the agent to implement a backend-integration for the feature

**Note**: This skill can be paired with the `feature-spec-generator` skill to develop in the spec-driven fashion.

Just ask add the `feature-spec-generator` skill and ask the agent to create a spec for the feature. Then, ask the agent to implement backend-integration for the feature defined in the `.claude/skills/feature-spec-generator/SPEC.md` file.
