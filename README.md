# SNF — Software Devel SNF

**SNF** is a minimalist software design philosophy and lightweight framework that treats the **browser as the platform**, not something to be replaced.

SNF is not a framework in the modern sense.  
It is a *discipline* for organizing HTML, CSS, and JavaScript so that programs remain **explicit, readable, inspectable, and humane** — even as they grow.

> SNF favors clarity of intent over cleverness of mechanism.

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

### 2. Explicit Over Clever

SNF prioritizes **explicit intent** over indirection:

- No hidden lifecycle hooks
- No magical dependency injection
- No implicit state propagation
- No reactive black boxes

If something happens, you should be able to **search for the line of code** that causes it.

> Code should read like prose, not like a magic trick.


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

>There is no custom module system.
>There is no build-step-required DSL.

### 5. UI as Structured DOM, Not Virtual Theater

SNF treats the DOM as the source of truth, not as an implementation detail.

 - DOM nodes are real
 - Events are real
 - State lives where it makes sense
 - Rendering is explicit

SNF does not require:

 - Virtual DOM diffing
 - Synthetic event systems
 - Reconciliation layers
 - Reactive signal graphs for CRUD apps

### 6. Progressive Construction, Not Grand Architecture

SNF applications grow incrementally:
 1. Start with static HTML
 2. Add behavior where needed
 3. Factor code only when repetition appears
 4. Load features dynamically when required

There is no “correct final architecture” imposed upfront.

> Programs should grow like cities, not like palaces.
### 7. Performance Through Sanity

SNF assumes:

 - UI performance bottlenecks are rarely algorithmic
 - Most performance wins come from not doing unnecessarywork
 - Network and layout dominate more than clever JavaScript

Thus SNF emphasizes:
 - Lazy loading
 - Minimal runtime overhead
 - Avoiding perpetual reactivity
 - Letting the browser optimize what it already knows how to do

> The fastest code is the code you never run.

### 8. Debuggability Is a Feature

SNF code should be debuggable with:
 - Browser DevTools
 - View Source
 - Console logs
 - Stack traces that make sense

If understanding a bug requires reading framework internals, the design has failed.

> A system that cannot be debugged is not finished.

### 9. No Sacred Build Step

SNF does not require:
 - Webpack
 - Babel
 - Vite
 - JSX
 - Transpilers
 - Code generators

Build tools may be added optionally for deployment or optimization, but SNF does not depend on them.

You should be able to:
 1. Open index.html
 2. Serve it
 3. Understand it


### 10. Teaching-Oriented by Design

SNF is intentionally suitable for:
 - Learning
 - Teaching
 - Exploration
 - Long-term maintenance

It is inspired by environments like:
 - VB6 / Delphi (visual clarity)
 - Early web development (directness)
 - Knuth’s literate philosophy (intent before machinery)

>If a beginner cannot reason about it, an expert should be suspicious of it.