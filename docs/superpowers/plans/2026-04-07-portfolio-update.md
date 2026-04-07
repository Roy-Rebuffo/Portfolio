# Portfolio Update Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Translate the entire portfolio to English, update experience to 1 year, and replace the projects section with 5 cards (ERP Peluquería translated + 4 new projects).

**Architecture:** Single-file edit on `index.html`. All changes are content/text replacements and one structural replacement (projects grid). EmailJS service/template IDs and public key are never touched.

**Tech Stack:** HTML, Tailwind CSS, vanilla JS, EmailJS (existing, untouched)

---

## File Map

| File | Action | What changes |
|------|--------|--------------|
| `index.html` | Modify | All text translations, stat update, projects grid replacement |

---

### Task 1: Translate Navigation & section anchors

**Files:**
- Modify: `index.html` (lines 131–141)

- [ ] **Step 1: Replace nav links text (desktop)**

Find this block (around line 132):
```html
<a href="#inicio" class="nav-link text-gray-300 hover:text-white text-sm">Inicio</a> <a href="#sobre-mi" class="nav-link text-gray-300 hover:text-white text-sm">Sobre mí</a> <a href="#habilidades" class="nav-link text-gray-300 hover:text-white text-sm">Habilidades</a> <a href="#proyectos" class="nav-link text-gray-300 hover:text-white text-sm">Proyectos</a> <a href="#contacto" class="nav-link text-gray-300 hover:text-white text-sm">Contacto</a>
```

Replace with:
```html
<a href="#inicio" class="nav-link text-gray-300 hover:text-white text-sm">Home</a> <a href="#sobre-mi" class="nav-link text-gray-300 hover:text-white text-sm">About</a> <a href="#habilidades" class="nav-link text-gray-300 hover:text-white text-sm">Skills</a> <a href="#proyectos" class="nav-link text-gray-300 hover:text-white text-sm">Projects</a> <a href="#contacto" class="nav-link text-gray-300 hover:text-white text-sm">Contact</a>
```

- [ ] **Step 2: Replace mobile menu links text**

Find (around line 138):
```html
<a href="#inicio" class="text-gray-300 hover:text-white">Inicio</a> <a href="#sobre-mi" class="text-gray-300 hover:text-white">Sobre mí</a> <a href="#habilidades" class="text-gray-300 hover:text-white">Habilidades</a> <a href="#proyectos" class="text-gray-300 hover:text-white">Proyectos</a> <a href="#contacto" class="text-gray-300 hover:text-white">Contacto</a>
```

Replace with:
```html
<a href="#inicio" class="text-gray-300 hover:text-white">Home</a> <a href="#sobre-mi" class="text-gray-300 hover:text-white">About</a> <a href="#habilidades" class="text-gray-300 hover:text-white">Skills</a> <a href="#proyectos" class="text-gray-300 hover:text-white">Projects</a> <a href="#contacto" class="text-gray-300 hover:text-white">Contact</a>
```

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "translate nav links to english"
```

---

### Task 2: Translate Hero section

**Files:**
- Modify: `index.html` (lines 143–169)

- [ ] **Step 1: Translate mono label and greeting**

Find:
```html
<p class="mono text-indigo-400 text-sm mb-4 tracking-wider">// Bienvenido a mi portfolio</p>
```
Replace with:
```html
<p class="mono text-indigo-400 text-sm mb-4 tracking-wider">// Welcome to my portfolio</p>
```

Find:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-4">Hola, soy <span id="hero-name" class="gradient-text">Roy Rebuffo Tabacman</span></h1>
```
Replace with:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-4">Hi, I'm <span id="hero-name" class="gradient-text">Roy Rebuffo Tabacman</span></h1>
```

- [ ] **Step 2: Translate hero description**

Find:
```html
<p id="hero-description" class="text-gray-400 text-lg max-w-xl mb-8 leading-relaxed">Apasionado por crear experiencias digitales increíbles con código limpio y diseño elegante</p>
```
Replace with:
```html
<p id="hero-description" class="text-gray-400 text-lg max-w-xl mb-8 leading-relaxed">Passionate about building incredible digital experiences with clean code and elegant design</p>
```

- [ ] **Step 3: Translate CTA buttons**

Find:
```html
<a href="#proyectos" class="btn-primary px-8 py-4 rounded-xl text-white font-semibold text-center"> Ver Proyectos </a> <a href="#contacto" class="btn-secondary px-8 py-4 rounded-xl text-gray-300 font-semibold border-2 border-gray-600 text-center"> Contactar </a>
```
Replace with:
```html
<a href="#proyectos" class="btn-primary px-8 py-4 rounded-xl text-white font-semibold text-center"> View Projects </a> <a href="#contacto" class="btn-secondary px-8 py-4 rounded-xl text-gray-300 font-semibold border-2 border-gray-600 text-center"> Contact Me </a>
```

- [ ] **Step 4: Commit**

```bash
git add index.html
git commit -m "translate hero section to english"
```

---

### Task 3: Translate About section + update stats

**Files:**
- Modify: `index.html` (lines 172–203)

- [ ] **Step 1: Translate section header**

Find:
```html
<p class="mono text-indigo-400 text-sm mb-2">// Conóceme</p>
<h2 class="text-4xl md:text-5xl font-bold text-white">Sobre mí</h2>
```
Replace with:
```html
<p class="mono text-indigo-400 text-sm mb-2">// Get to know me</p>
<h2 class="text-4xl md:text-5xl font-bold text-white">About Me</h2>
```

- [ ] **Step 2: Replace about text**

Find:
```html
<p id="about-text" class="text-gray-400 text-lg leading-relaxed mb-8">Soy estudiante de Desarrollo de Aplicaciones Multiplataforma con interés en el desarrollo de software y aplicaciones web. Trabajo principalmente con Java, MySQL y JavaScript, y estoy en proceso de seguir ampliando mis conocimientos y experiencia práctica. Me gusta aprender nuevas tecnologías y mejorar mis habilidades desarrollando proyectos funcionales y bien estructurados.</p>
```
Replace with:
```html
<p id="about-text" class="text-gray-400 text-lg leading-relaxed mb-8">I'm a Full Stack Developer with 1 year of hands-on experience building web applications and software solutions. I work primarily with Java, Python, JavaScript, and modern frameworks like React and FastAPI. I enjoy building functional, well-structured projects and continuously expanding my skill set.</p>
```

- [ ] **Step 3: Update stat cards**

Find:
```html
<div class="text-5xl font-bold gradient-text mb-2">
         15+
        </div>
        <div class="text-gray-400">
         Proyectos
        </div>
```
Replace with:
```html
<div class="text-5xl font-bold gradient-text mb-2">
         15+
        </div>
        <div class="text-gray-400">
         Projects
        </div>
```

Find:
```html
<div class="text-5xl font-bold gradient-text mb-2">
         0
        </div>
        <div class="text-gray-400">
         Años
        </div>
```
Replace with:
```html
<div class="text-5xl font-bold gradient-text mb-2">
         1+
        </div>
        <div class="text-gray-400">
         Years of Experience
        </div>
```

- [ ] **Step 4: Commit**

```bash
git add index.html
git commit -m "translate about section, update experience to 1 year"
```

---

### Task 4: Translate Skills section

**Files:**
- Modify: `index.html` (lines 205–274)

- [ ] **Step 1: Translate section header**

Find:
```html
<p class="mono text-indigo-400 text-sm mb-2">// Mi stack tecnológico</p>
<h2 class="text-4xl md:text-5xl font-bold text-white">Habilidades</h2>
```
Replace with:
```html
<p class="mono text-indigo-400 text-sm mb-2">// My tech stack</p>
<h2 class="text-4xl md:text-5xl font-bold text-white">Skills</h2>
```

- [ ] **Step 2: Commit**

```bash
git add index.html
git commit -m "translate skills section to english"
```

---

### Task 5: Replace Projects section

**Files:**
- Modify: `index.html` (lines 276–351)

- [ ] **Step 1: Translate section header**

Find:
```html
<p class="mono text-indigo-400 text-sm mb-2">// Mi trabajo</p>
<h2 class="text-4xl md:text-5xl font-bold text-white">Proyectos Destacados</h2>
```
Replace with:
```html
<p class="mono text-indigo-400 text-sm mb-2">// My work</p>
<h2 class="text-4xl md:text-5xl font-bold text-white">Featured Projects</h2>
```

- [ ] **Step 2: Replace the entire projects grid**

Find the entire grid div (from `<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">` down to its closing `</div>` before `</section>`) and replace with:

```html
<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8"><!-- ERP Barbershop -->
      <div class="project-card relative rounded-2xl overflow-hidden border border-gray-700/50 bg-gradient-to-br from-gray-800/50 to-gray-900/50">
       <div class="aspect-video bg-gradient-to-br from-purple-500/20 to-pink-500/20 flex items-center justify-center">
        <svg class="w-20 h-20 text-purple-400" viewbox="0 0 24 24" fill="currentColor"><path d="M3 3h8v8H3V3zm10 0h8v8h-8V3zM3 13h8v8H3v-8zm15 0h-2v3h-3v2h3v3h2v-3h3v-2h-3v-3z" /> <rect x="5" y="5" width="4" height="4" fill="currentColor" /> <rect x="15" y="5" width="4" height="4" fill="currentColor" /> <rect x="5" y="15" width="4" height="4" fill="currentColor" />
        </svg>
       </div>
       <div class="project-overlay absolute inset-0 bg-gradient-to-t from-black/90 via-black/60 to-transparent opacity-0 flex flex-col justify-end p-6">
        <div class="project-content">
         <h3 class="text-xl font-bold text-white mb-2">Barbershop ERP</h3>
         <p class="text-gray-300 text-sm mb-4">Complete ERP system for barbershop management including service and product administration.</p>
         <div class="flex flex-wrap gap-2 mb-4"><span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">Python</span>
         </div><a href="https://github.com/Roy-Rebuffo/Trabajo-Grupal-Python" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-indigo-400 hover:text-indigo-300 text-sm font-medium">
          <svg class="w-4 h-4" viewbox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
          </svg> View Code </a>
        </div>
       </div>
       <div class="p-6">
        <h3 class="text-xl font-bold text-white mb-2">Barbershop ERP</h3>
        <div class="flex flex-wrap gap-2"><span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">Python</span>
        </div>
       </div>
      </div><!-- FinSight -->
      <div class="project-card relative rounded-2xl overflow-hidden border border-gray-700/50 bg-gradient-to-br from-gray-800/50 to-gray-900/50">
       <div class="aspect-video bg-gradient-to-br from-indigo-500/20 to-blue-500/20 flex items-center justify-center">
        <svg class="w-20 h-20 text-indigo-400" viewbox="0 0 24 24" fill="currentColor"><path d="M3.5 18.49l6-6.01 4 4L22 6.92l-1.41-1.41-7.09 7.97-4-4L2 16.99z"/>
        </svg>
       </div>
       <div class="project-overlay absolute inset-0 bg-gradient-to-t from-black/90 via-black/60 to-transparent opacity-0 flex flex-col justify-end p-6">
        <div class="project-content">
         <h3 class="text-xl font-bold text-white mb-2">FinSight — AI Portfolio Analyst</h3>
         <p class="text-gray-300 text-sm mb-4">Full-stack AI-powered investment portfolio analyst. Queries investments in real time, fetches live market data, and calculates quantitative risk metrics through a LangGraph conversational agent.</p>
         <div class="flex flex-wrap gap-2 mb-4"><span class="px-3 py-1 rounded-full bg-indigo-500/20 text-indigo-300 text-xs">FastAPI</span> <span class="px-3 py-1 rounded-full bg-blue-500/20 text-blue-300 text-xs">React</span> <span class="px-3 py-1 rounded-full bg-purple-500/20 text-purple-300 text-xs">LangGraph</span> <span class="px-3 py-1 rounded-full bg-emerald-500/20 text-emerald-300 text-xs">PostgreSQL</span> <span class="px-3 py-1 rounded-full bg-gray-500/20 text-gray-300 text-xs">Docker</span>
         </div><a href="https://github.com/Roy-Rebuffo/FinSight" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-indigo-400 hover:text-indigo-300 text-sm font-medium">
          <svg class="w-4 h-4" viewbox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
          </svg> View Code </a>
        </div>
       </div>
       <div class="p-6">
        <h3 class="text-xl font-bold text-white mb-2">FinSight — AI Portfolio Analyst</h3>
        <div class="flex flex-wrap gap-2"><span class="px-3 py-1 rounded-full bg-indigo-500/20 text-indigo-300 text-xs">FastAPI</span> <span class="px-3 py-1 rounded-full bg-blue-500/20 text-blue-300 text-xs">React</span> <span class="px-3 py-1 rounded-full bg-purple-500/20 text-purple-300 text-xs">LangGraph</span> <span class="px-3 py-1 rounded-full bg-emerald-500/20 text-emerald-300 text-xs">PostgreSQL</span> <span class="px-3 py-1 rounded-full bg-gray-500/20 text-gray-300 text-xs">Docker</span>
        </div>
       </div>
      </div><!-- mini_Jira -->
      <div class="project-card relative rounded-2xl overflow-hidden border border-gray-700/50 bg-gradient-to-br from-gray-800/50 to-gray-900/50">
       <div class="aspect-video bg-gradient-to-br from-blue-500/20 to-cyan-500/20 flex items-center justify-center">
        <svg class="w-20 h-20 text-blue-400" viewbox="0 0 24 24" fill="currentColor"><path d="M13 2.05v2.02c3.95.49 7 3.85 7 7.93 0 3.21-1.81 6-4.72 7.72L13 17v5l5-3c3.12-1.76 5-5.03 5-8.97.02-5.46-3.97-9.97-10-10.98zM11 2.05C4.97 3.06 1 7.57 1 13.03c0 3.94 1.88 7.21 5 8.97l5 3v-5l-2.28 1.7C6.81 19.07 5 16.25 5 13.03c0-4.08 3.05-7.44 7-7.93V2.05z"/>
        </svg>
       </div>
       <div class="project-overlay absolute inset-0 bg-gradient-to-t from-black/90 via-black/60 to-transparent opacity-0 flex flex-col justify-end p-6">
        <div class="project-content">
         <h3 class="text-xl font-bold text-white mb-2">mini_Jira — Task Manager</h3>
         <p class="text-gray-300 text-sm mb-4">A personal task manager inspired by Jira. Features JWT authentication, Kanban-style dashboard, and full task CRUD. Built to learn modern full-stack development.</p>
         <div class="flex flex-wrap gap-2 mb-4"><span class="px-3 py-1 rounded-full bg-green-500/20 text-green-300 text-xs">FastAPI</span> <span class="px-3 py-1 rounded-full bg-blue-500/20 text-blue-300 text-xs">React</span> <span class="px-3 py-1 rounded-full bg-emerald-500/20 text-emerald-300 text-xs">PostgreSQL</span> <span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">JWT</span>
         </div><a href="https://github.com/Roy-Rebuffo/mini_Jira" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-indigo-400 hover:text-indigo-300 text-sm font-medium">
          <svg class="w-4 h-4" viewbox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
          </svg> View Code </a>
        </div>
       </div>
       <div class="p-6">
        <h3 class="text-xl font-bold text-white mb-2">mini_Jira — Task Manager</h3>
        <div class="flex flex-wrap gap-2"><span class="px-3 py-1 rounded-full bg-green-500/20 text-green-300 text-xs">FastAPI</span> <span class="px-3 py-1 rounded-full bg-blue-500/20 text-blue-300 text-xs">React</span> <span class="px-3 py-1 rounded-full bg-emerald-500/20 text-emerald-300 text-xs">PostgreSQL</span> <span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">JWT</span>
        </div>
       </div>
      </div><!-- SweetDash -->
      <div class="project-card relative rounded-2xl overflow-hidden border border-gray-700/50 bg-gradient-to-br from-gray-800/50 to-gray-900/50">
       <div class="aspect-video bg-gradient-to-br from-pink-500/20 to-rose-500/20 flex items-center justify-center">
        <svg class="w-20 h-20 text-pink-400" viewbox="0 0 24 24" fill="currentColor"><path d="M18.06 22.99h1.66c.84 0 1.53-.64 1.63-1.46L23 5.05h-5V1h-1.97v4.05h-4.97l.3 2.34c1.71.47 3.31 1.32 4.27 2.26 1.44 1.42 2.43 2.89 2.43 5.29v8.05zM1 21.99V21h15.03v.99c0 .55-.45 1-1.01 1H2.01c-.56 0-1.01-.45-1.01-1zm15.03-7c0-8.01-15.03-8.01-15.03 0h15.03zM1.02 17h15v2h-15z"/>
        </svg>
       </div>
       <div class="project-overlay absolute inset-0 bg-gradient-to-t from-black/90 via-black/60 to-transparent opacity-0 flex flex-col justify-end p-6">
        <div class="project-content">
         <h3 class="text-xl font-bold text-white mb-2">SweetDash — Bakery Manager</h3>
         <p class="text-gray-300 text-sm mb-4">Bakery management application that automates order tracking, customer management, product inventory, and stock control — replacing manual calendar and spreadsheet workflows.</p>
         <div class="flex flex-wrap gap-2 mb-4"><span class="px-3 py-1 rounded-full bg-orange-500/20 text-orange-300 text-xs">Java</span> <span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">JavaScript</span>
         </div><a href="https://github.com/Roy-Rebuffo/SweetDash" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-indigo-400 hover:text-indigo-300 text-sm font-medium">
          <svg class="w-4 h-4" viewbox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
          </svg> View Code </a>
        </div>
       </div>
       <div class="p-6">
        <h3 class="text-xl font-bold text-white mb-2">SweetDash — Bakery Manager</h3>
        <div class="flex flex-wrap gap-2"><span class="px-3 py-1 rounded-full bg-orange-500/20 text-orange-300 text-xs">Java</span> <span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">JavaScript</span>
        </div>
       </div>
      </div><!-- Planning Agent -->
      <div class="project-card relative rounded-2xl overflow-hidden border border-gray-700/50 bg-gradient-to-br from-gray-800/50 to-gray-900/50">
       <div class="aspect-video bg-gradient-to-br from-green-500/20 to-teal-500/20 flex items-center justify-center">
        <svg class="w-20 h-20 text-green-400" viewbox="0 0 24 24" fill="currentColor"><path d="M19 3h-4.18C14.4 1.84 13.3 1 12 1c-1.3 0-2.4.84-2.82 2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 0c.55 0 1 .45 1 1s-.45 1-1 1-1-.45-1-1 .45-1 1-1zm-2 14l-4-4 1.41-1.41L10 14.17l6.59-6.59L18 9l-8 8z"/>
        </svg>
       </div>
       <div class="project-overlay absolute inset-0 bg-gradient-to-t from-black/90 via-black/60 to-transparent opacity-0 flex flex-col justify-end p-6">
        <div class="project-content">
         <h3 class="text-xl font-bold text-white mb-2">Planning Agent — AI Scheduler</h3>
         <p class="text-gray-300 text-sm mb-4">Intelligent weekly planning agent that analyses a to-do list and generates a prioritised weekly schedule using AI. Built with LangChain, Groq LLaMA, and Streamlit.</p>
         <div class="flex flex-wrap gap-2 mb-4"><span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">Python</span> <span class="px-3 py-1 rounded-full bg-green-500/20 text-green-300 text-xs">LangChain</span> <span class="px-3 py-1 rounded-full bg-teal-500/20 text-teal-300 text-xs">Streamlit</span> <span class="px-3 py-1 rounded-full bg-orange-500/20 text-orange-300 text-xs">Groq</span>
         </div><a href="https://github.com/Roy-Rebuffo/Planning_Agent" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-indigo-400 hover:text-indigo-300 text-sm font-medium">
          <svg class="w-4 h-4" viewbox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
          </svg> View Code </a>
        </div>
       </div>
       <div class="p-6">
        <h3 class="text-xl font-bold text-white mb-2">Planning Agent — AI Scheduler</h3>
        <div class="flex flex-wrap gap-2"><span class="px-3 py-1 rounded-full bg-yellow-500/20 text-yellow-300 text-xs">Python</span> <span class="px-3 py-1 rounded-full bg-green-500/20 text-green-300 text-xs">LangChain</span> <span class="px-3 py-1 rounded-full bg-teal-500/20 text-teal-300 text-xs">Streamlit</span> <span class="px-3 py-1 rounded-full bg-orange-500/20 text-orange-300 text-xs">Groq</span>
        </div>
       </div>
      </div>
     </div>
```

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "overhaul projects section: remove 2 old, translate ERP, add 4 new projects"
```

---

### Task 6: Translate Contact section

**Files:**
- Modify: `index.html` (lines 352–416)

- [ ] **Step 1: Translate section header**

Find:
```html
<p class="mono text-indigo-400 text-sm mb-2">// Conectemos</p>
<h2 class="text-4xl md:text-5xl font-bold text-white mb-4">Contacto</h2>
<h3 class="text-2xl text-gray-300">¡Hablemos!</h3>
```
Replace with:
```html
<p class="mono text-indigo-400 text-sm mb-2">// Let's connect</p>
<h2 class="text-4xl md:text-5xl font-bold text-white mb-4">Contact</h2>
<h3 class="text-2xl text-gray-300">Let's Talk!</h3>
```

- [ ] **Step 2: Translate contact body text**

Find:
```html
<p class="text-gray-400 text-lg mb-8 leading-relaxed">Estoy siempre abierto a nuevas oportunidades y proyectos interesantes. No dudes en contactarme si quieres colaborar o simplemente charlar sobre tecnología.</p>
```
Replace with:
```html
<p class="text-gray-400 text-lg mb-8 leading-relaxed">I'm always open to new opportunities and interesting projects. Feel free to reach out if you want to collaborate or just talk tech.</p>
```

- [ ] **Step 3: Translate form labels and placeholders**

Find:
```html
<label for="name" class="block text-gray-300 text-sm mb-2">Nombre</label> <input type="text" id="name" name="name" required class="w-full px-4 py-3 rounded-xl bg-gray-900/50 border border-gray-700 text-white placeholder-gray-500 transition-all" placeholder="Tu nombre">
```
Replace with:
```html
<label for="name" class="block text-gray-300 text-sm mb-2">Name</label> <input type="text" id="name" name="name" required class="w-full px-4 py-3 rounded-xl bg-gray-900/50 border border-gray-700 text-white placeholder-gray-500 transition-all" placeholder="Your name">
```

Find:
```html
<label for="email" class="block text-gray-300 text-sm mb-2">Email</label> <input type="email" id="email" name="email" required class="w-full px-4 py-3 rounded-xl bg-gray-900/50 border border-gray-700 text-white placeholder-gray-500 transition-all" placeholder="tu@email.com">
```
Replace with:
```html
<label for="email" class="block text-gray-300 text-sm mb-2">Email</label> <input type="email" id="email" name="email" required class="w-full px-4 py-3 rounded-xl bg-gray-900/50 border border-gray-700 text-white placeholder-gray-500 transition-all" placeholder="you@email.com">
```

Find:
```html
<label for="message" class="block text-gray-300 text-sm mb-2">Mensaje</label> <textarea id="message" name="message" rows="5" required class="w-full px-4 py-3 rounded-xl bg-gray-900/50 border border-gray-700 text-white placeholder-gray-500 transition-all resize-none" placeholder="Tu mensaje..."></textarea>
```
Replace with:
```html
<label for="message" class="block text-gray-300 text-sm mb-2">Message</label> <textarea id="message" name="message" rows="5" required class="w-full px-4 py-3 rounded-xl bg-gray-900/50 border border-gray-700 text-white placeholder-gray-500 transition-all resize-none" placeholder="Your message..."></textarea>
```

- [ ] **Step 4: Translate submit button and JS status messages**

Find:
```html
<span id="btn-text">Enviar Mensaje</span>
```
Replace with:
```html
<span id="btn-text">Send Message</span>
```

Find in the JS block:
```js
btnText.textContent = 'Enviando...';
```
Replace with:
```js
btnText.textContent = 'Sending...';
```

Find:
```js
formMessage.textContent = '¡Mensaje enviado con éxito! Te contactaré pronto.';
```
Replace with:
```js
formMessage.textContent = 'Message sent successfully! I\'ll get back to you soon.';
```

Find:
```js
formMessage.textContent = `Error: ${error.text}. Revisa la consola o usa el email directamente.`;
```
Replace with:
```js
formMessage.textContent = `Error: ${error.text}. Check the console or contact me directly by email.`;
```

Find:
```js
formMessage.textContent = 'Error de conexión. Verifica tu conexión a internet.';
```
Replace with:
```js
formMessage.textContent = 'Connection error. Please check your internet connection.';
```

Find:
```js
formMessage.textContent = `Error (${error.status || 'desconocido'}). Por favor, usa el email directamente: rebufforoy@gmail.com`;
```
Replace with:
```js
formMessage.textContent = `Error (${error.status || 'unknown'}). Please contact me directly at: rebufforoy@gmail.com`;
```

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "translate contact section and form messages to english"
```

---

### Task 7: Translate Footer + update defaultConfig description

**Files:**
- Modify: `index.html` (lines 417–422 and JS defaultConfig block ~line 429)

- [ ] **Step 1: Translate footer**

Find:
```html
<p class="text-gray-500">© 2024 Roy Rebuffo Tabacman. Hecho con 💜</p>
```
Replace with:
```html
<p class="text-gray-500">© 2025 Roy Rebuffo Tabacman. Made with 💜</p>
```

- [ ] **Step 2: Update defaultConfig about_description**

Find:
```js
about_description: 'Soy un desarrollador full stack con más de 3 años de experiencia creando aplicaciones web modernas y escalables. Me especializo en JavaScript, React, Node.js y bases de datos. Mi pasión es transformar ideas complejas en soluciones digitales elegantes y funcionales.',
```
Replace with:
```js
about_description: 'I\'m a Full Stack Developer with 1 year of hands-on experience building web applications and software solutions. I work primarily with Java, Python, JavaScript, and modern frameworks like React and FastAPI. I enjoy building functional, well-structured projects and continuously expanding my skill set.',
```

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "translate footer, update defaultConfig description"
```
