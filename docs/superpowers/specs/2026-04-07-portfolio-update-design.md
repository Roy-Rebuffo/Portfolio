# Portfolio Update Design Spec
**Date:** 2026-04-07  
**Status:** Approved

## Overview

Update Roy Rebuffo Tabacman's portfolio (`index.html`) with three focused changes: full English translation, experience update to 1 year, and project section overhaul. No aesthetic changes, no framework changes, EmailJS contact stays intact.

## Scope

Single file: `index.html`. No new files, no dependencies added.

## Changes

### 1. Navigation & Section Labels
- Nav links: Inicio → Home, Sobre mí → About, Habilidades → Skills, Proyectos → Projects, Contacto → Contact
- Mobile menu: same translations
- Mono comments: translate all `// ...` labels in section headers

### 2. Hero Section
- `"Hola, soy"` → `"Hi, I'm"`
- Hero description → `"Passionate about building incredible digital experiences with clean code and elegant design"`
- `"Ver Proyectos"` → `"View Projects"`, `"Contactar"` → `"Contact Me"`
- Mono label: `"// Welcome to my portfolio"`

### 3. About Section
- Section title: `"Sobre mí"` → `"About Me"`, mono label → `"// Get to know me"`
- About text (English, 1 year experience): `"I'm a Full Stack Developer with 1 year of hands-on experience building web applications and software solutions. I work primarily with Java, Python, JavaScript, and modern frameworks like React and FastAPI. I enjoy building functional, well-structured projects and continuously expanding my skill set."`
- Stat card: `"0"` → `"1+"`, `"Años"` → `"Years of Experience"`
- `"15+ Proyectos"` → `"15+ Projects"` (label translated)

### 4. Skills Section
- Title: `"Habilidades"` → `"Skills"`, mono label → `"// My tech stack"`

### 5. Projects Section (main change)
- Title: `"Proyectos Destacados"` → `"Featured Projects"`, mono label → `"// My work"`
- **Remove**: E-Commerce Platform card, Simulación Bancaria card
- **Keep**: ERP Peluquería (translate text to English)
- **Add 4 new cards**:

**ERP Peluquería (translated)**
- Title: `"Barbershop ERP"`
- Description: `"Complete ERP system for barbershop management including service and product administration."`
- Tags: Python
- Link: existing GitHub link

**FinSight**
- Title: `"FinSight — AI Portfolio Analyst"`
- Description: `"Full-stack AI-powered investment portfolio analyst. Queries investments in real time, fetches live market data, and calculates quantitative risk metrics through a LangGraph conversational agent."`
- Tags: FastAPI, React, LangGraph, PostgreSQL, Docker
- Link: https://github.com/Roy-Rebuffo/FinSight

**mini_Jira**
- Title: `"mini_Jira — Task Manager"`
- Description: `"A personal task manager inspired by Jira. Features JWT authentication, Kanban-style dashboard, and full task CRUD. Built to learn modern full-stack development."`
- Tags: FastAPI, React, PostgreSQL, JWT
- Link: https://github.com/Roy-Rebuffo/mini_Jira

**SweetDash**
- Title: `"SweetDash — Bakery Manager"`
- Description: `"Bakery management application that automates order tracking, customer management, product inventory, and stock control — replacing manual calendar and spreadsheet workflows."`
- Tags: Java, JavaScript
- Link: https://github.com/Roy-Rebuffo/SweetDash

**Planning Agent**
- Title: `"Planning Agent — AI Scheduler"`
- Description: `"Intelligent weekly planning agent that analyses a to-do list and generates a prioritised weekly schedule using AI. Built with LangChain, Groq LLaMA, and Streamlit."`
- Tags: Python, LangChain, Streamlit, Groq
- Link: https://github.com/Roy-Rebuffo/Planning_Agent

### 6. Contact Section
- Title: `"Contacto"` → `"Contact"`, mono label → `"// Let's connect"`
- Subtitle: `"¡Hablemos!"` → `"Let's Talk!"`
- Body text: `"I'm always open to new opportunities and interesting projects. Feel free to reach out if you want to collaborate or just talk tech."`
- Form labels: `"Nombre"` → `"Name"`, `"Mensaje"` → `"Message"`, placeholder `"Tu nombre"` → `"Your name"`, etc.
- Button: `"Enviar Mensaje"` → `"Send Message"`, sending state → `"Sending..."`
- Success/error messages translated to English
- **EmailJS untouched**: `init("NK4xcLsaVg5vb557I")`, `service_e5434lt`, `template_knaqgo5`

### 7. Footer
- `"Hecho con 💜"` → `"Made with 💜"`
- Year stays 2024 (or update to 2025 — user to confirm, left as-is for now)

## Constraints
- No new CSS classes, no new JS logic
- EmailJS service/template IDs and public key not touched
- Grid layout unchanged (new cards follow exact same HTML structure as existing cards)
- No external dependencies added
