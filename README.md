# Rasmus Ladefoged - Software developer from Copenhagen, Denmark

I am a Software Developer with 5 years of professional IT experience and a Computer Science degree from Copenhagen University. 

I thrive on solving complex architectural problems, optimizing performance, and building clean, maintainable systems. Currently, my engineering focus is split between modern full-stack web architectures and performance-critical systems development.

### 🚀 Current Focus Areas
.
* **Systems & Algorithmic Thinking:** Developing a complex **2D Dungeon Crawler** from scratch in Python. Rather than relying on a commercial engine, I am building the core mechanics myself—focusing on advanced AI pathfinding, real-time raycasting, and custom spatial partitioning to optimize performance under heavy entity loads.
* **Architecture & Maintainability:** Practicing rigorous software engineering patterns to manage a large-scale codebase as complexity scales. The engine leverages **Component Composition** over deep inheritance hierarchies, separating game state, rendering logic, and physical boundaries into decoupled subsystems. By utilizing patterns like **Data-Driven Factories** for entity spawning and **Lazy Instantiation** for resource management, the architecture minimizes memory overhead and remains highly extensible as new mechanics are introduced.

Below are some of my notable projects, followed by the toolset I use to build them.

---
### **[Custom 2D Dungeon Crawler Engine](https://github.com/RasmusLC1/Kobold_Clash/)** — *Python, Pygame*
A custom-built game engine powering a procedurally generated 2D world with real-time AI, dynamic lighting, and zero external engine dependencies.

* **Load-Balanced AI:** Supports 100+ simultaneous enemies utilizing $A^*$ pathfinding coupled with a frame-distributed request queue to eliminate frame stuttering and maintaining 60+ FPS.
* **Spatial Knowledge Hub:** Designed a centralized tile grid system where tiles cache local boundaries and entities, dropping situational queries down to $O(1)$ complexity.
* **Dynamic AI Director:** Features a systemic difficulty engine ("The Awakening") that monitors player noise and environmental density to dynamically manipulate spawns and traps.
* **Automated Testing:** Backed by an automated test suite leveraging `pytest` and mock architectures covering pathfinding and procedural map generation.

---
### **[Bookstore Webshop (Booky)](https://github.com/RasmusLC1/Booky)** — *Next.js, TypeScript, Supabase, Prisma*
![Booky product page](data/bookstore.png)

A full-stack, self-publishing platform built to simulate a high-traffic e-commerce environment with an emphasis on security and administrative control.

* **Core Features:** Complete user lifecycle management via Next-Auth, Stripe payment streams, and an isolated Admin Dashboard for automated platform moderation.
* **Security & Resilience:** Implemented strict HTML sanitization to eliminate XSS risks, data validation via Zod, and secure media uploads using EdgeStore filters.
* **Infrastructure:** Leveraging Supabase (PostgreSQL) via Prisma ORM for relational integrity, hosted and continuously deployed via Vercel.

### 🧮 **[Bachelor Project: Polynomial Multiplication](https://github.com/RasmusLC1/Polynomial-Multiplication)** — *Algorithmic Optimization*
![Bachelor Screenshot](data/bachelor.png)
Academic research analyzing the real-world efficiency of advanced algebraic algorithms.
* Achieved a **14x performance improvement** by optimizing Karatsuba's multiplication algorithm.
* Refactored a recursive Fast Fourier Transform (FFT) into an iterative layout, resulting in a **2.5x speedup**.

### 🕹 **[3D Wolfenstein Renderer](https://github.com/RasmusLC1/Wolfenstein-Renderer)** — *C#, .NET*
![Wolfenstein](data/wolfenstein.png)
A retro-inspired 3D raycaster projecting a 2D map matrix into a simulated 3D space, featuring localized lighting depth and enemy tracking logic.

---

## 🧰 Languages and Tools
<img align="left" alt="TypeScript" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-plain.svg" />
<img align="left" alt="JavaScript" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-plain.svg" />
<img align="left" alt="React" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" />
<img align="left" alt="Next.js" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg" />
<img align="left" alt="NodeJS" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" />
<img align="left" alt="SQL" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azuresqldatabase/azuresqldatabase-original.svg" />
<img align="left" alt="Python" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-plain.svg" />
<img align="left" alt="C#" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/csharp/csharp-original.svg" />
<img align="left" alt=".NET" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/dotnetcore/dotnetcore-original.svg" />
<img align="left" alt="C++" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg" />
<img align="left" alt="Linux" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" />
<br />


