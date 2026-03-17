**Here's a focused learning and practice plan** until AgenC reaches mainnet and ecosystem relevance (based on the current repo state from `docs/ROADMAP.md` and `TODO.MD`).

### 1. Master the Current AgenC Codebase (Immediate Priority)
**Read (start here):**
- `docs/ROADMAP.md` (current state, gaps, what's production-ready)
- `TODO.MD` (durable autonomous runtime vision, OpenAI background/deep research patterns, explicit task contracts)
- Docs in `docs/` directory
- Key architecture files in `runtime/`, `sdk/`, `programs/`, `mcp/`

**Explore:**
- Solana program (42 instructions, PDAs for agents/tasks/skills/reputation/governance)
- TypeScript SDK (v1.3.0, already production-ready)
- Agent runtime + MCP server (tool use, prompts, skills)
- ZK VM (RISC Zero Groth16)

### 2. Core Technical Skills to Deepen
- **Solana Program Development**: Accounts, PDAs, CPIs, events, errors. Study the existing program heavily (it's audit-ready).
- **Advanced TypeScript / Node.js**: The runtime is ~216k lines with 5000+ vitest tests.
- **Durable Agent Runtime Patterns**: Background jobs, state persistence, wake reasons, verification loops, pause/resume, auditability (heavily referenced in TODO).
- **MCP (Model Context Protocol)**: Tool standardization, role-based access, skill registration.
- **ZK / Verifiable Compute**: RISC Zero, proof integration (already production-ready in the stack).
- **Reputation, Skills Registry, Governance**: On-chain mechanics for agent coordination and rewards (SPL tokens).

### 3. Supporting Fundamentals
- Rust (if contributing to program side)
- Solana web3.js + wallet integration
- Agentic AI patterns (tool calling, long-running tasks, verification, memory)
- Security best practices (`security_best_practices_report.md` in repo)

### 4. Practice Plan (Build Real Value Now)
- Fix the broken CI/CD (highest leverage gap)
- Implement missing MCP tools (skills, team, reputation, governance)
- Add test coverage to web app and complete mobile app
- Wire real media pipeline (Whisper STT, image description)
- Run and extend `agenc-eval-test.cjs` + existing tests
- Build custom skills/tools and test agent runs locally
- Initialize protocol locally and test task/agent lifecycle once ready

### Suggested Order
1. Read ROADMAP + TODO + core docs (today)
2. Deep dive into SDK + Solana program
3. Work on one concrete gap (CI/CD or MCP tools)
4. Study durable runtime patterns from the referenced OpenAI guides

The Solana program and SDK are already very mature. The main blockers to mainnet/relevance are polish, testing, CI, full skill registry, and ecosystem adoption (agents actually using it for paid tasks).