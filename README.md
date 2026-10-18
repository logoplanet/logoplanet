## Marcus Thorne [`logoplanet`]

Compiler engineer & AST tinkerer located in Montreal, Canada.  
Working on dialect parsers, SQL linters, refactoring algorithms, and syntax tree transformations.

---

### ⚡ Selected Open Source Patches

| Target | Subsystem | Reference | Status | Impact |
|---|---|---|---|---|
| **[sqlfluff/sqlfluff](https://github.com/sqlfluff/sqlfluff)** | Reflow / Respace | [PR #8776](https://github.com/sqlfluff/sqlfluff/pull/8776) | `In Review` | Prevents collapsing consecutive bitwise `~` into `~~` (LIKE operator) in LT01 rule |
| **[agronholm/anyio](https://github.com/agronholm/anyio)** | Concurrency | Audit Suite | `Inspected` | Exception lifecycle and shielded cancellation propagation |

---

### 🔬 How I Build & Audit

When modifying syntax tree transformers and linters, unintended token fusion changes semantic meaning.  
I enforce strict compiler invariant checks:
- Token-boundary collision guards (`_PROHIBITED_FUSED_TOKENS`).
- Zero unintended whitespace collapse across dialect-specific operators.
- Automated diff validation and lint verification powered by [ZeroSlop™ CI](https://github.com/marketplace/actions/zeroslop-by-ribbsaeter-systems).
