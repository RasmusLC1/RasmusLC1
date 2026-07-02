# Rasmus Ladefoged - Software developer from Copenhagen, Denmark

I am a Software Developer with 5 years of experience in IT from Ireland and a degree in Computer Science from Copenhagen University.

I love problem-solving and learning new skills. Currently, I am focusing on full-stack development by building a Next.js Webshop for books, incorporating features like secure payments, dynamic routing, secure sign-in, automated emails, product search, database hosting and many more things. It is still under development and continually updated.

Alongside web development, I'm working on a 2D Dungeon Crawler Game, enhancing my algorithmic thinking and ability to write clean, scalable and maintainable code. From building the game engine to implementing features like AI, combat, and interactable environments, this project has significantly sharpened my problem-solving skills.

Below are some of my notable projects and the technologies I’ve used to build these projects:

---
**Dungeon Crawler Game**

A custom-built game engine powering a procedurally generated 2D dungeon crawler with real-time AI, dynamic lighting, and a full loot and progression system. Built entirely from scratch in Python without a commercial game engine to progress my skills as a software developer and architect.

**Features**

- Advanced enemy AI supporting 100+ simultaneous enemies, using A* pathfinding, spatial partitioning, and a load-balanced request queue that distributes pathfinding calculations across frames to prevent frame stutter
- Procedural dungeon generation using cellular automata, producing natural cave layouts with placed rooms, loot, traps, and boss arenas each run
- Dynamic AI Director ("The Awakening") that escalates difficulty in real time based on player noise and area density — spawning enemies, buffing them, locking doors, and replacing chests with mimics
- Real-time raycasting lighting system with additive light contributions per tile and fog-of-war exploration using Pre-computed ray vectors for performance
- Full inventory system supporting weapons, runes, consumables, and stackable loot with automatic merging
- Tile grid system acting as a centralised spatial knowledge hub — each tile caches its neighbours, physics boundaries, light contributions, and entity occupants, allowing enemies, items, and the raycaster to query local world state in O(1) rather than scanning the full map
- Status effect system with 20+ interactive effects including fire, poison, frozen, electric, and vampiric — with cross-effect interactions such as fire being cancelled by wet or amplifying incoming damage
- - Automated test suite covering core engine systems including AI pathfinding, tilemap logic, status effects, raycasting, and procedural generation, written with pytest and unittest.mock

**Technology**

- Language: Python / Pygame
- Algorithms: A*, Cellular Automata, Raycasting, Squared Distance Spatial Partitioning
- Patterns: Component composition, lazy instantiation, load-balanced queues, data-driven spawning factories

### Performance Metrics
- Stable 60 fps
- Optimized for 100+ enemies without noticeable performance degradation
- Map size is limited to 120 X 120 for gameplay, but can be increased to 500X500 without performance decrease
- There are no known game breaking bugs or unexpected crashes

### Development Notes

This project has been in active development for two years alongside university and work. Earlier systems (inventory, weapons) reflect where my skills were at the start of the project and are due for a refactor. Newer systems (AI, lighting, effects, tile architecture) reflect more current design thinking and are where I'd point for code quality. The git history shows the progression of myself as a developer.


---
# Websites:
**[Interactive Book Store!](https://booky-mu.vercel.app/)**  
**[Portfolio Website!](https://rasmuslc1.github.io/portfolio_website/#)**  

#
## 🧰 Languages and Tools

<img align="left" alt="TypeScript" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-plain.svg" />
<img align="left" alt="JavaScript" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-plain.svg" />
<img align="left" alt="React" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" />
<img align="left" alt="Next.js" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg" />
<img align="left" alt="NodeJS" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" />
<img align="left" alt="SQL" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azuresqldatabase/azuresqldatabase-original.svg" />
<img align="left" alt="CSS" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-plain.svg" />
<img align="left" alt="Python" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-plain.svg" />
<img align="left" alt="Numpy" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/numpy/numpy-original.svg" />
<img align="left" alt="C#" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/csharp/csharp-original.svg" />
<img align="left" alt=".NET" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/dotnetcore/dotnetcore-original.svg" />
<img align="left" alt="C++" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg" />
<img align="left" alt="Linux" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" />
<img align="left" alt="Github" width="30px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/github/github-original.svg" />
<br />

#

# Interesting Projects

## 💻 **[Bookstore Webshop](https://github.com/RasmusLC1/Booky)**  
![Booky product page](data/bookstore.png)

A full-stack web application for buying, uploading, searching, and managing books, built with Next.js. The platform offers a seamless user experience through secure payments, user accounts, automated emails, dynamic routing, and more.

### Link
https://booky-mu.vercel.app/

### Features
- 👤 **User Accounts** with profile pages and order history
- 💳 **Secure Payment Processing** using the **Stripe API**
- 🔒 **Secure Sign-In** and authorization with **Next-Auth** and **bcrypt** for encryption
- 🔐 **Password Reset Emails** with secure, time-limited dynamic links and encrypted password updates via the **Resend API**
- 📧 **Automated Emails** for account actions and order details via the **Resend API**
- 📂 **Secure File Uploads** via the **EdgeStore API** with validation filters to prevent malicious content
- 🗄️ **Database Integration** with Prisma ORM and SQLite for efficient backend storage
- 👩‍💻 **HTML Sanitization** to prevent XSS attacks and ensure safe user input when creating their account and adding recipes
- 🔗 **Dynamic URL Routing** with randomized product IDs to enhance security
- 👮‍♀️ **Admin Dashboard** for managing users, products, and orders, handling user feedback, and moderating reported products
- 🔍 **Product search** and filtering
- ☁ **Database Hosting** using **Supabase** for scalable and reliable backend services
- 🌐 **Website Hosting** using **Vercel** for fast, secure, and continuous deployment.


### Technology
- **Language:** TypeScript
- **Frontend:** React, Next.js
- **Backend:** Node.js, NextAuth
- **Database:** Supabase (via Prisma ORM)
- **APIs:** Stripe, Resend, EdgeStore
- **Security:** HTML Sanitization, bcrypt, Zod
- **Hosting**: Vercel

### Goal
Booky is a full-stack bookstore platform that enables users to upload, manage, and self-publish their books securely and efficiently. The platform offers a user-friendly solution for organizing and sharing books, with robust features for both end-users and administrators.
#

#

## 🧮 **[Bachelor Project in Polynomial Multiplication](https://github.com/RasmusLC1/Polynomial-Multiplication)**  
![Bachelor Screenshot](data/bachelor.png)
Research into the effectiveness of efficient algorithmic implementation with focus on polynomial multiplication

### Features
- 📈 Karatsuba's algorithm implemented for polynomial multiplication and optimised for 14 X improved performance
- 🔄 Recursive FFT algorithm implemented
- 🔁 Iterative FFT algorithm implemented for 2.5 X improved performance
- 🧪 Extensive Unit testing for correctness and performance

#

## 🕹 **[3D Wolfenstein Renderer](https://github.com/RasmusLC1/Wolfenstein-Renderer)**  
![Wolfenstein](data/wolfenstein.png)

A 3D renderer built in C# using .NET, inspired by the original Wolfenstein 3D game.

### Features
- 👁 3D view of a 2D map
- 💡 Lighting engine to simulate depth
- 🧠 Enemy AI that pathfinds to and targets the player
- 🗺️ 2D perspective of the map with raycaster for field of view
- 🕹 Early demo for the Dungeon Crawler game I later wrote in Python

### Technology
- Language: C#


