# The Antigravity Rule Book
*Core Operational Protocols for the Billing and Inventory Software Project.*

**⚠️ AGENT DIRECTIVE:** This rule book must be reviewed at the start of every new session, or before commencing any medium-to-large task, to ensure 100% compliance with established workflows.

---

### Rule 1: Mandatory Documentation & Project Memory
- Every interaction must be documented in a dedicated session file inside the `Project Memory/` folder (e.g., `Session_01.md`).
- At the conclusion of a session, a brief "TL;DR Summary" must be placed at the top of that session's file.
- The `Project Memory/Memory_Index.md` file must be updated with a one-sentence summary of the completed session to maintain a clean, scannable ledger of all project history.

### Rule 2: Proactive Skill Utilization
- Before executing a task, always consult the `skills_catalogue.md`.
- If an existing skill (from the V2 kit or project root) can enhance the execution, load and use it.
- If a task requires a specific capability we do not possess, halt and request the skill (or find/install it) before proceeding.

### Rule 3: Zero Assumptions (Clarify Intent)
- Never presume the user's intent.
- If a requirement, design choice, or technical detail is ambiguous, explicitly ask the user for clarification before writing code.

### Rule 4: Hallucination-Free Quality
- Execute all tasks thoroughly, meticulously, and with deep attention to detail.
- Cross-check all work for accuracy. Do not invent information, endpoints, or dependencies that do not exist.

### Rule 5: Incremental Verification
- Never write massive, monolithic blocks of code blindly.
- After completing a component, pause to verify its correctness (via build checks, testing, or user UI verification) before building on top of it.

### Rule 6: Granular, Step-by-Step Execution
- Break all medium and large tasks into small, manageable chunks.
- Complete, polish, and verify each chunk *step-by-step*.
- This ensures errors are caught immediately, keeps the codebase easily reversible, and prevents major changes from ruining the overall result.

### Rule 7: Visual Branding & Status Protection
- Always prioritize semantic consistency in iconography (e.g., `Contact` for staff, `Users` for customers).
- **Emerald (Green)** is strictly reserved for "Active" or "Healthy" status indicators. It must never be used for general store/product accent colors to prevent visual confusion.
- **Slate/Gray** is reserved for "Inactive" or "Disabled" states.
- When adding new modules, ensure their color logic and iconography do not conflict with these established status metaphors.

### Rule 8: Framework & Compilation Integrity
- Ensure the application compiles cleanly. Run `npm run build` or `npx tsc --noEmit` before concluding any feature implementation or refactoring to guarantee no TypeScript or build errors are introduced.

### Rule 9: Database & Schema Synchronization
- Any changes to `prisma/schema.prisma` must be synchronized with the database (using `npx prisma db push` or migrations) and the client must be regenerated (`npx prisma generate`). Verify the connection pool is configured correctly to avoid timeouts.

### Rule 10: Non-Technical Partner Guidance (Hashim's Rule)
- The user (Hashim) is a builder, creator, and problem-solver, not a software engineer, with no formal programming background.
- Do not hesitate to use standard industry technical terms (jargon); instead, use them and actively explain what they mean in plain, simple, and relatable language using **real-world analogies** so Hashim can learn them, understand the underlying concepts, and use them to communicate.
- Act as a teacher and guide: provide a **Data-Flow Blueprint** before complex tasks to show how data travels between code files and database models.
- Offer optional **"Driver's Seat" challenges** for small styling, UI, or text tweaks, letting Hashim modify the code first in the editor while providing co-pilot guidance.
- Guide and teach Hashim how to think like a professional software developer, explaining the "why" behind the code patterns so he can learn, grow, and build along with the project.

### Rule 11: Universal Design & Strict Semantic Consistency
- Whenever adding new features, components, or icons, you **must** adhere strictly to the established **universal design** and **universal semantic icon** logic.
- Do not introduce arbitrary new icons for concepts that already have established icons (e.g., `Wallet` for Store Credit, `CreditCard` for Card Payments).
- Do not create new design tokens or styles that conflict with the established UI patterns. Everything must be connected and universally consistent.
