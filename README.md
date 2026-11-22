# Rasmus Ladefoged: Software Developer in Copenhagen

I'm a backend-focused developer with a B.Sc. in Computer Science from Copenhagen University, working as a consultant at Netcompany. I like building complete systems and understanding how they work underneath: a .NET web API for a bookstore, a 2D game engine written from scratch, and a stock screener that scores companies from financial data are some of my main projects.

Before development I spent several years in IT support and QA for Microsoft, Google and Apple in Ireland.

📫 [LinkedIn](https://linkedin.com/in/rcarlsen853/) · [Email](mailto:rasmus.lc3@gmail.com)


### 🚀 Current Focus Areas

* **Systems & Algorithmic Thinking:** Developing a complex **2D Dungeon Crawler** from scratch in Python. Rather than relying on a commercial engine, I am building the core mechanics myself—focusing on advanced AI pathfinding, real-time raycasting, and custom spatial partitioning to optimize performance under heavy entity loads.
* **Architecture & Maintainability:** Practicing rigorous software engineering patterns to manage a large-scale codebase as complexity scales. The engine leverages **Component Composition** over deep inheritance hierarchies, separating game state, rendering logic, and physical boundaries into decoupled subsystems. By utilizing patterns like **Data-Driven Factories** for entity spawning and **Lazy Instantiation** for resource management, the architecture minimizes memory overhead and remains highly extensible as new mechanics are introduced.

Below are some of my notable projects, followed by the toolset I use to build them.

---
### ⚔️ **[Custom 2D Dungeon Crawler Engine (Kobold Clash)](https://github.com/RasmusLC1/Kobold_Clash/)** — *Python, Pygame*
<img src="data/kobold.gif" alt="Kobold Clash" width="50%" />


A custom-built game engine powering a procedurally generated 2D world with real-time AI, dynamic lighting, and zero external engine dependencies.
* **Load-Balanced AI:** Supports 100+ simultaneous enemies utilizing $A^*$ pathfinding coupled with a frame-distributed request queue to eliminate frame stuttering while maintaining 60+ FPS.
* **Spatial Knowledge Hub:** Designed a centralized tile grid system where tiles cache local boundaries and entities, dropping situational queries down to $O(1)$ complexity.
* **Dynamic AI Director:** Features a systemic difficulty engine ("The Awakening") that monitors player noise and environmental density to dynamically manipulate spawns and traps.
* **Raycasting & Lighting:** Implements a 360° raycasting system for fog-of-war exploration with additive per-source tile lighting, pre-computed ray vectors, and cached tile surfaces to minimise redraws.
* **Automated Testing:** Backed by a pytest suite covering core engine systems including AI pathfinding, tilemap spatial queries, raycasting, status effect interactions, and procedural generation pipelines, using mock architectures to isolate components without requiring a live game instance.

---
### 💻 **[Bookstore Webshop (Booky)](https://github.com/RasmusLC1/Booky)**: *C#, ASP.NET Core, EF Core, SQLite, TypeScript, Next.js*
<img src="data/bookstore.png" alt="Booky product page" height="250" />

A full-stack online bookstore with a custom **ASP.NET Core Web API** backend, migrated from a Next.js/Prisma implementation while keeping the existing frontend working throughout.

* **Architecture:** Layered .NET Web API (controllers, services, EF Core) behind a Next.js frontend. Session checks stay in Next.js, and the API accepts only requests carrying a shared service key.
* **Core Features:** Accounts with Google sign-in, Stripe payments (test mode), password-reset and order-history emails, product reviews, and an admin area for managing products, users and orders.
* **Security:** Purchase-verified download tokens that expire after 24 hours and stream the file without exposing storage URLs, bcrypt password hashing, Zod validation and Upstash rate limiting.
* **Delivery:** Frontend on Vercel, with tests and a GitHub Actions pipeline.

---
### 📈 **[Stock Analysis Tool](https://github.com/RasmusLC1/stock_analysis)** — *Python, TypeScript, React, Vite, SQLite*
<img src="data/screener.png" alt="Stock Analysis Tool" height="250" />

Full-stack investment screening and backtesting application that scores companies (~200+ tickers) across fundamental dimensions from financial data to surface compounders and filter out cyclical value traps.
- **Architecture:** React/TypeScript (Vite) frontend paired with a Python REST backend, separating data retrieval, SQLite caching, metric calculations, and multi-lens scoring into modular components.
- **Multi-Lens Scoring:** Evaluates companies across thematic lenses (**Growth, Quality, Health, Value, GARP, and Scale Disruptor**) using normalized financial data to produce a weighted 0–100 composite score.
- **Capital-Intensive Calibration:** Adjusts financial health scaling—such as cash buffer thresholds—to account for capital-intensive business models without issuing false penalties.
- **SQLite Caching & Performance:** Uses a local SQLite database (`stock_summaries.db`) to cache fetched financial summaries, reducing redundant external API calls and speeding up repeated screening and backtest runs.
- **Testing & Backtesting:** Backed by unit-tested scoring logic and backtesting scripts that correlate historical scores with subsequent performance, compute multi-year CAGR metrics, and export portfolio valuations to CSV.

---
### 🏝️ **[Procedural Town Simulator (Towns-End)](https://github.com/RasmusLC1/townsend/)** — *Godot 4, C#*
<img width="50%" height="640" alt="image" src="https://github.com/user-attachments/assets/eb1a2909-d6ca-49c6-8fd7-a59e581b69b8" /><img width="50%" height="625" alt="image" src="https://github.com/user-attachments/assets/efa3c303-a95f-418f-a10c-78a30904edcb" />


A procedurally generated 3D island town-builder built on Godot's GridMap, combining custom terrain generation, coastline-aware biome placement, and a fully decoupled tool-based editing system.
* **Procedural Terrain Generation:** Layered simplex noise combined with a radial falloff mask carves a bounded island silhouette; a dual-cache system (full-column data for cliffs/caves, a dedicated surface-tile index for everything else) keeps ground lookups at $O(1)$ instead of scanning every buried layer.
* **Coastline-Aware Biome Placement:** A multi-source BFS flood-fill computes each land tile's true shortest-path distance to open water, banding sand within a configurable ring thickness — replacing a naive "low elevation = beach" heuristic that misplaced sand in inland valleys.
* **Day/Night Cycle:** Drives Godot's animation system to simulate dynamic lighting and sky color shifts over a configurable real-time day length, exposing a normalized time-of-day interface (with day/night transition signals) for future gameplay and AI systems to react to.
* **Extensible Feature Spawning:** A Template Method-based spawner hierarchy (trees, rocks, plants, crates) shares candidate filtering and placement logic, using per-mesh AABB analysis to ground props correctly regardless of source pivot or scale, instead of hand-tuned offsets per asset.
* **Decoupled Grid Editing Tools:** An `IGridTool` interface lets mouse input (click, drag-select with a live rectangle outline) delegate entirely to swappable tool implementations — the input handler has zero knowledge of what a selection actually does, so new tools (paint, build, bulldoze) require no changes to input code.

---
### 🧮 **[Bachelor Project: Polynomial Multiplication](https://github.com/RasmusLC1/Polynomial-Multiplication)** — *Algorithmic Optimization in C*
<img src="data/bachelor.png" alt="Bachelor Screenshot" height="250" />
Academic research benchmarking five polynomial multiplication algorithms implemented from scratch in C using GMP for arbitrary-precision arithmetic.

* **Algorithms implemented:** Naïve O(n²), DFT, recursive FFT, iterative FFT, and Karatsuba — each with a full forward/inverse transform pipeline and a systematic runtime test harness for direct comparison across input sizes.
* **14x improvement on Karatsuba:** Tuned the base-case threshold through empirical benchmarking to find the crossover point where schoolbook 
  multiplication outperforms the recursive overhead, reducing runtime by 14x over the unoptimised implementation.
* **2.5x improvement on FFT:** Refactored the recursive FFT into an iterative layout using bit-reversal permutation and a single upfront memory allocation passed through the call stack, eliminating per-call malloc overhead and improving cache locality.

---

### 🕹 **[3D Wolfenstein Renderer](https://github.com/RasmusLC1/Wolfenstein-Renderer)** — *C#, .NET*
<img src="data/wolfenstein.png" alt="Wolfenstein" height="250" />
* **3D Wolfenstein Renderer** — *C#, .NET* — A retro raycaster built in 2023 as the technical predecessor to *Kobold Clash*. 

* **Features:** Implemented $A^*$ pathfinding, raycasting-based fog of war, and a real-time ray-traced shooting system.
* **Architectural Takeaway:** The structural and scaling limitations encountered during this project directly influenced the decision to switch to a strict component-based architecture for *Kobold Clash*.

---
## 🧰 Languages and Tools

<p>
  <img alt="C#" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/csharp/csharp-original.svg" />
  <img alt=".NET" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/dotnetcore/dotnetcore-original.svg" />
  <img alt="Java" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" />
  <img alt="TypeScript" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-plain.svg" />
  <img alt="Python" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-plain.svg" />
  <img alt="C" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/c/c-original.svg" />
  <img alt="React" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" />
  <img alt="Next.js" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg" />
  <img alt="SQLite" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/sqlite/sqlite-original.svg" />
  <img alt="Git" width="30" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" />
</p>
