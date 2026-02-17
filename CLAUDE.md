# CLAUDE.md - Rebuild nyxar.dev Portfolio

## mission

Rebuild nyxar.dev from scratch as a premium developer portfolio that accomplishes two things:
1. Showcases Nyxar as a top-tier Minecraft AND Hytale developer actively building HyRivals
2. Makes it dead obvious that commissions are open and drives people to reach out

The current site is fine but generic. The new site needs to scream "this person builds real things
that real players use" and make server owners think "I need to hire this person right now."

---

## identity

Name: Nyxar
Role: Full-Stack Game Server Developer
Tagline: "Building the infrastructure behind competitive gaming"
Discord: https://discord.com/users/1420522038740910083
Website: nyxar.dev
MC Head API: https://mc-heads.net/avatar/Nyxar_dev/80 (keep using this for avatar)

---

## design system

Follow the DESIGN.md system (dark luxury gaming aesthetic). Specifically:

### colors
```
--bg-primary:      #0A0A0F
--bg-secondary:    #12121A
--bg-tertiary:     #1A1A2E
--bg-elevated:     #222238
--border-subtle:   rgba(255, 255, 255, 0.06)
--border-default:  rgba(255, 255, 255, 0.10)
--text-primary:    #F0F0F5
--text-secondary:  #9090A8
--text-muted:      #5A5A72
--accent-gradient:  linear-gradient(135deg, #6366F1, #8B5CF6, #D946EF, #F43F5E)
--accent-glow:     0 0 20px rgba(139, 92, 246, 0.3)
--success:         #34D399
--warning:         #FBBF24
```

### fonts
- Display: "Plus Jakarta Sans", weight 700-800
- Body: "Plus Jakarta Sans", weight 400-500
- Mono/Stats: "JetBrains Mono"
- Import: https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap

### rules
- Dark mode ONLY, no light mode, no white backgrounds anywhere
- No Inter, Roboto, Arial
- Glass/frost effects on cards (backdrop-filter: blur)
- Subtle animations (fade-up on scroll, hover lifts on cards)
- Prism gradient accents sparingly (CTAs, active states, key highlights)
- No emojis in the actual site content
- Mobile responsive (this will be viewed on phones from Discord links)

---

## tech stack

Single-page site. One HTML file with inline CSS and JS. No frameworks, no build tools.
It needs to load instantly when someone clicks the link from Discord.

Libraries allowed (CDN only):
- Google Fonts (Plus Jakarta Sans, JetBrains Mono)
- No other dependencies. Pure HTML/CSS/JS.

---

## site structure

### 1. HERO SECTION

Full viewport height. This is the first thing anyone sees.

Layout:
- Left side: text content
- Right side: Minecraft skin render (use mc-heads.net body render)

Content:
- Small label above headline: "FULL-STACK GAME SERVER DEVELOPER" (uppercase, letter-spaced, muted color)
- Main headline: "I build the backends that power competitive servers."
- Subtext: "Currently developing the infrastructure behind HyRivals, the #1 competitive Hytale server. 10+ years shipping production game server code across Minecraft and Hytale."
- Two CTA buttons:
  - Primary (gradient): "Hire Me" -> scrolls to commission section
  - Secondary (ghost): "View My Work" -> scrolls to projects
- Status indicator: green dot + "Available for Commissions" (animated subtle pulse on the dot)

Stats bar below the hero text (horizontal row, 4 items):
- "10+" / "Years Experience"
- "50+" / "Projects Shipped"
- "100K+" / "Lines of Code"
- "1M+" / "Players Served"

Use JetBrains Mono for the numbers. Animate them counting up on page load.

### 2. FEATURED PROJECT: HYRIVALS (full-width spotlight)

This section exists to prove credibility. It's the crown jewel.

Background: subtle gradient or pattern to make it stand out from other sections.

Content:
- Section label: "CURRENTLY BUILDING"
- Project name: "HyRivals" (large, bold)
- Tagline: "The #1 Competitive Hytale Server"
- Description (2-3 sentences): "HyRivals launched Day 1 of Hytale's Early Access and was recognized by PCGamesN as 'the most fully developed Hytale server.' I architect the backend systems powering global leaderboards, ranked matchmaking, real-time duels, and performance-optimized APIs serving thousands of concurrent players."

Feature cards (grid of 4-6 small cards highlighting what I built):
- "Backend API" / "RESTful API with sub-2ms leaderboard queries, Redis caching, and pre-computed stats"
- "Ranked Duels" / "Full matchmaking system with ELO ratings, class-based filtering, and live stat tracking"
- "Leaderboard System" / "Global leaderboards with denormalized data, batch recalculation, and versioned cache keys"
- "Database Architecture" / "PostgreSQL schema design optimized for high-throughput competitive data"
- "Real-time Stats" / "Live K/D tracking, win streaks, and per-class performance analytics"
- "Web Dashboard" / "hyrivals.gg frontend with server status, player profiles, and leaderboard pages"

Press quote card (glass effect, stands out):
"HyRivals is actually the most fully developed Hytale server we've seen so far."
-- PCGamesN, "Best Hytale Servers" (January 2026)

Link to: play.hyrivals.gg | hyrivals.gg

### 3. SERVICES / COMMISSIONS SECTION

This is the money section. Make it absolutely clear what's for hire.

Section label: "COMMISSIONS OPEN"
Headline: "Let's build your server."

Three service tier cards side by side:

**Card 1: Plugin / Mod Development**
- Custom Minecraft plugins (Spigot/Paper)
- Hytale server plugins (Java 25)
- Custom enchants, minigames, economy systems
- Performance optimization and bug fixing
- Starting at: "DM for pricing"

**Card 2: Backend & API Development**
- REST APIs, database design, caching layers
- Player data systems, leaderboards, matchmaking
- Web dashboards and admin panels
- PostgreSQL, Redis, Node.js, Java
- Starting at: "DM for pricing"

**Card 3: Full Server Setup**
- Complete server infrastructure from scratch
- Proxy setup (Velocity/BungeeCord)
- Plugin configuration and custom development
- Staff training and management systems
- Starting at: "DM for pricing"

Below the cards, a single prominent CTA:
"Ready to start? Let's talk."
Button: "Contact on Discord" -> https://discord.com/users/1420522038740910083

### 4. SKILLS / TECH STACK

Clean grid showing technologies. Group them:

**Languages:** Java, JavaScript/TypeScript, SQL, HTML/CSS
**Frameworks:** Paper API, Hytale Plugin API, Node.js, Next.js, React, Express
**Databases:** PostgreSQL, MySQL, SQLite, Redis
**Infrastructure:** Docker, Velocity, Linux, Nginx, Git
**Tools:** Gradle, IntelliJ IDEA, VS Code, Claude Code

Each skill shown as a small pill/badge. No icons needed, just clean text pills
grouped under headers. The tech stack should feel dense and impressive.

### 5. PROJECT HISTORY

Grid of past project cards. Keep it tight, 4-6 projects max:

**HyRivals** (Hytale)
- Role: Lead Backend Developer
- "The #1 competitive Hytale server. Built the entire backend API, leaderboard system, and ranked matchmaking from scratch."
- Tags: Hytale, Java, PostgreSQL, Redis, REST API
- Status: Active / Ongoing

**PrismEnchants** (Minecraft)
- Role: Solo Developer
- "Premium custom enchantments plugin with 100+ enchants, web panel, and visual enchant builder. 299 files, compiles clean."
- Tags: Paper, Java, Next.js, SQLite
- Status: In Development

(Add 2-4 more placeholders for past MC server work. Use generic but real-sounding names.
The user can fill these in later. Structure them as:)

**[Server Name]** (Minecraft)
- Role: Developer / Staff Manager
- Brief description of what was built/managed
- Tags: relevant tech
- Status: Completed

### 6. TESTIMONIALS

Keep the testimonials section from the current site but restyle it to match the new design.
Use glass-effect cards with quote marks. If there are no testimonials yet, create
placeholder slots that say "Your testimonial here" with a note that says
"Worked with me? I'd love your feedback."

### 7. FOOTER

Simple, clean:
- "Nyxar" logo/text on left
- Links: Discord, GitHub (if applicable)
- "Available for commissions" repeated
- Copyright 2026

---

## animations and interactions

### on page load:
- Hero text fades up with stagger (headline first, then subtext, then CTAs)
- Stats count up from 0
- Skin render fades in slightly delayed

### on scroll:
- Each section fades up when it enters viewport (IntersectionObserver)
- Stagger children within sections (cards appear one by one)

### hover effects:
- Cards lift slightly (translateY -4px) with border glow
- CTA buttons: gradient shifts, shadow grows
- Project cards: border color transitions to accent

### the prism gradient border effect:
Use on the HyRivals spotlight card and the "Hire Me" button:
```css
background: linear-gradient(135deg, #6366F1, #8B5CF6, #D946EF, #F43F5E, #6366F1);
background-size: 300% 300%;
animation: prism-shift 4s ease infinite;
```

---

## critical requirements

1. The site MUST be a single HTML file. No separate CSS/JS files. Everything inline.
   This makes deployment dead simple (just upload one file).

2. Mobile responsive. Test at 375px width. The hero should stack vertically on mobile.
   Cards should go single-column. Everything must be readable on a phone.

3. Fast. No heavy assets. The only external requests are Google Fonts and mc-heads.net
   for the avatar/skin. Everything else is inline.

4. The "Hire Me" and "Contact on Discord" buttons must be the most visually prominent
   elements on the page. They should use the prism gradient and glow effect.

5. No placeholder text that looks like placeholder text. If content needs to be filled
   in later, make it look intentional (like "More projects coming soon" not "Lorem ipsum").

6. The HyRivals section must feel like a case study, not just a project card.
   It's the proof that this developer ships real production systems.

7. The PCGamesN quote is real and verified. Use it prominently. This is social proof
   from a major gaming publication.

8. Do NOT use em dashes anywhere. Use commas, periods, or restructure sentences instead.

9. The overall vibe: professional but not corporate. This is a freelance developer
   who builds gaming infrastructure, not a SaaS company. It should feel like talking
   to a skilled dev, not reading a marketing page.

---

## file output

Output a single file: index.html
This file contains ALL HTML, CSS (in <style>), and JS (in <script>).
Nothing external except Google Fonts and mc-heads.net images.

The file should be production-ready. Drop it on any web server and it works.
