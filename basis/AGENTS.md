### Rules

1. **Clarify before acting**  
   If a task is ambiguous or missing critical context, ask a concise targeted question before writing any code or making assumptions.

2. **Use Context7 MCP proactively**  
   Whenever a task involves a library, framework, or external API — whether for documentation lookup, code generation, or setup — invoke Context7 MCP automatically without waiting to be asked.

### Good Software Architecture (Frontend + Backend)

- **Modularity**  
  Build small, independently replaceable units with clearly defined interfaces.

- **Separation of Concerns**  
  Each module owns exactly one responsibility — UI renders, services orchestrate, data layers persist.

- **Layered Architecture**  
  Enforce a strict flow: presentation → business logic → data access, with no layer skipping.

- **No Direct DB Access from UI**  
  All data mutations and queries must pass through a service or API boundary.

- **Scalability**  
  Prefer stateless components and defer shared state to infrastructure (cache, queue, DB).

- **Security**  
  Validate and sanitize at every boundary; never trust input from a layer above.

- **Performance**  
  Avoid unnecessary work — lazy-load, cache deterministic results, and measure before optimizing.

- **Maintainability**  
  Code is written for the next reader: name things clearly, avoid clever, and keep functions short.

- **Testing**  
  Tests verify real behavior — cover what the implementation actually does, not how it does it. Never adapt implementation code to satisfy a test.