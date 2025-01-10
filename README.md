# Rasmus Ladefoged - Software developer from Copenhagen, Denmark

I am a Software Developer with 5 years of experience in IT from Ireland and a degree in Computer Science from Copenhagen University.

I love problem-solving and learning new skills. Currently, I am focusing on full-stack development by building a Next.js Webshop for managing recipes, incorporating features like secure payments, dynamic routing, automated emails and product search. Next I will work on secure sign in, user interaction and hosting.

Alongside web development, I'm working on a 2D Dungeon Crawler Game, enhancing my algorithmic thinking and ability to write clean, scalable and maintainable code. From building the game engine to implementing features like AI, combat, and interactable environments, this project has significantly sharpened my problem-solving skills.

Below are some of my notable projects and the technologies I’ve used to build these projects:

---
# Portfolio Website:
**[Check out my portfolio website!](https://rasmuslc1.github.io/portfolio_website/#)**  

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

### **[Recipe App](https://github.com/RasmusLC1/Recipe-App)**  
![Landing Page of Recipe App](data/recipe_app.png)
A full-stack web application for uploading, searching, and managing recipes, built with Next.js. The app delivers a seamless user experience by integrating secure payment, automated emails, and dynamic routing.

### Features
- 👤 **User Accounts** with profile pages and order history
- 💳 **Secure Payment Processing** using the **Stripe API**
- 📧 **Automated Emails** for account actions and order details via the **Resend API**
- 📂 **Secure File Uploads** via the **EdgeStore API** with validation filters to prevent malicious content
- 🗄️ **Database Integration** with Prisma ORM and SQLite for efficient backend storage
- 👩‍💻 **HTML Sanitization** to prevent XSS attacks and ensure safe user input when creating their account and adding recipes
- 🔗 **Dynamic URL Routing** with randomized product IDs to enhance security
- 👮‍♀️ **Admin Dashboard** for managing users, products, and orders, handling user feedback, and moderating reported products
- 🔍 **Product search** and filtering

### Technology
- Language: TypeScript
- Libraries: React, Next.js,  Node.js 
- Database: SQLite (via Prisma ORM)
- APIs: Stripe, Resend, EdgeStore

### Goal
A full-stack recipe-sharing platform designed to help users upload, search, and manage personalized recipes. The app solves the problem of organizing and sharing recipes by providing a secure, user-friendly platform with powerful features for both users and administrators.

#

## **[Dungeon Crawler Game](https://github.com/RasmusLC1/Dungeon-Crawler)**  
![Dungeon Game Screenshot](data/dungeongame.png)
This project showcases a custom-built game engine powering a procedurally generated 2D dungeon crawler featuring real-time AI, dynamic lighting, and interactive gameplay mechanics.

### Features
- 🧠 Advanced Enemy AI optimized to handle hundreds of enemies simultaneously using A* for pathfinding and Spatial Hash Grid for fast lookups. The AI dynamically scales its decision-making by checking fewer parameters when enemies are far from the player, minimizing computational overhead.
- 🏰 Procedural Dungeon Generation using cellular automata and custom rulesets
- 🗺️ Spatial Hash Grid for efficient collision detection and entity lookups
- 🌟 Real-Time Dynamic Lighting that updates as the player explores the dungeon
- 🎮 State manager to handle game events
- 🎒 Interactive Inventory System for managing loot, equipment, and consumables
- ⚔️ Combat and Magic System with state-driven effects and animations

### Technology
- Language: Python
- Algorithms: A*, Spatial Hash Grid, Custom Lighting Algorithm, Cellular Automata, Raycasting

### Performance Metrics
- Stable 60 fps
- Optimized for 100+ enemies without noticeable performance degradation
- Map size is limited to 120 X 120 for gameplay, but can be increased to 500X500 without performance decrease
- There are no known game breaking bugs or unexpected crashes

### Goal
To create an engaging dungeon crawler with infinite replayability through procedurally generated dungeons and dynamic challenges. The game aims to provide a balance of strategy and action to keep players engaged across multiple playthroughs. The long-term objective is to publish the game on Steam, delivering a polished and optimized experience to players.

### Gameplay loop
Players enter a randomized dungeon floor, fighting enemies and managing resources to progress to the next level. Each floor increases in difficulty, requiring players to balance risk and reward. Combat is tactical, encouraging players to preserve health and manage inventory while deciding whether to engage enemies for potential rewards or avoid unnecessary danger.

#

## **[Bachelor Project in Polynomial Multiplication](https://github.com/RasmusLC1/Polynomial-Multiplication)**  
![Bachelor Screenshot](data/bachelor.png)
Research into the effectiveness of efficient algorithmic implementation with focus on polynomial multiplication

### Features
- 📈 Karatsuba's algorithm implemented for polynomial multiplication and optimised for 14 X improved performance
- 🔄 Recursive FFT algorithm implemented
- 🔁 Iterative FFT algorithm implemented for 2.5 X improved performance
- 🧪 Extensive Unit testing for correctness and performance

#

## **[3D Wolfenstein Renderer](https://github.com/RasmusLC1/Wolfenstein-Renderer)**  
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

# Contact
Currently open to job offers, feel free to reach out if my skillset is of interest.

Email: rasmus.lc3@gmail.com


