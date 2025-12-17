# SNF — Software Devel SNF

**SNF** is a minimalist software design philosophy and lightweight framework that treats the **browser as the platform**, not something to be replaced.

SNF is not a framework in the modern sense.  
It is a *discipline* for organizing HTML, CSS, and JavaScript so that programs remain **explicit, readable, inspectable, and humane** — even as they grow.

> SNF favors clarity of intent over cleverness of mechanism.

---

## Core Principles

### 1. The Browser Is the Runtime

SNF does not abstract away the browser.
It **embraces native web primitives**:

- HTML for structure
- CSS for presentation
- JavaScript for behavior
- The DOM as the UI tree
- ES modules as the composition unit

If the browser already solves a problem well, SNF does not replace it.

> The browser is already an operating system for documents.  
> SNF merely organizes its use.

---

### 2. Explicit Over Clever

SNF prioritizes **explicit intent** over indirection:

- No hidden lifecycle hooks
- No magical dependency injection
- No implicit state propagation
- No reactive black boxes

If something happens, you should be able to **search for the line of code** that causes it.

> Code should read like prose, not like a magic trick.

---

### 3. Minimal Abstraction Surface

Abstractions are introduced **only when they remove real duplication or confusion**.

SNF avoids:
- IoC theater
- Framework-driven architecture
- “Patterns” that exist only to justify themselves
- Overgeneralized configuration systems

Abstractions must earn their existence by:
- Reducing cognitive load
- Making behavior more local
- Improving debuggability

> Abstraction is a cost, not a virtue.

---

### 4. Composition via ES Modules

SNF uses **standard ES modules** as the primary unit of composition.

Benefits:
- Native lazy loading
- Clear dependency graphs
- Tooling-free modularity
- Natural code splitting

There is no custom module system.
There is no build-step-required DSL.

```js
import { showFeature } from "./features/report.js";
