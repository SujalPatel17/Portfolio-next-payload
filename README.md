# Portfolio-next-payload
CMS-powered personal portfolio built with Next.js 15, Payload CMS v3, Tailwind CSS v4, and PostgreSQL.

# Sujal Patel — Personal Portfolio

A modern, CMS-powered personal portfolio built with **Next.js 15**, **Payload CMS 3**, **Tailwind CSS 4**, and **PostgreSQL**. All content (projects, skills, hero section, site metadata) is managed through a built-in admin panel — no code changes needed to update the site.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Next.js 15 (App Router) |
| CMS | Payload CMS v3 |
| Database | PostgreSQL |
| Styling | Tailwind CSS v4 |
| Animations | GSAP, Framer Motion, Motion |
| Language | TypeScript + JSX |

---

## Features

- **CMS-driven content** — Projects, Skills, Hero section, and Site metadata all managed via Payload admin panel
- **Scroll animations** — GSAP ScrollTrigger for sticky project cards with fade/blur effect
- **Type animation** — Cycling role titles on the hero section
- **Cursor blob** — Custom animated cursor effect
- **Responsive** — Mobile-first design across all sections
- **Contact form** — Built-in contact section
- **Scroll to top** — Smooth scroll-to-top button

---

## Project Structure

```
├── app/
│   ├── (frontend)/         # Portfolio site (page.tsx, layout.tsx)
│   └── (payload)/          # Payload CMS admin panel & API routes
│       ├── admin/          # Admin UI
│       └── api/[...slug]/  # REST API
├── src/
│   └── components/         # All React components
│       ├── About.jsx       # Hero section (CMS-driven)
│       ├── Projects.jsx    # Projects section (CMS-driven)
│       ├── Expertise.jsx   # Skills section (CMS-driven)
│       ├── Contact.jsx
│       ├── Header.jsx
│       └── Footer.jsx
├── payload.config.ts        # Payload CMS config (collections & globals)
├── next.config.ts
└── scripts/                 # DB seed scripts
```

---

## Getting Started

### Prerequisites

- Node.js 18+
- PostgreSQL database

### 1. Clone the repo

```bash
git clone https://github.com/SujalPatel17/portfolio-react.git
cd portfolio-react
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

Create a `.env.local` file in the root:

```env
DATABASE_URI=postgresql://username:password@localhost:5432/portfolio
PAYLOAD_SECRET=your-secret-key-here
NEXT_PUBLIC_SERVER_URL=http://localhost:3000
```

### 4. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the portfolio.
Open [http://localhost:3000/admin](http://localhost:3000/admin) to access the CMS.

---

## CMS Collections & Globals

| Type | Slug | Description |
|---|---|---|
| Collection | `projects` | Portfolio projects with images, links, tags |
| Collection | `skills` | Expertise cards with icon names and categories |
| Collection | `media` | Uploaded images |
| Global | `hero` | Hero section: name, bio, roles, social links, resume |
| Global | `site-settings` | Site title and meta description |

---

## Seed Data

To seed initial skills and globals into the database:

```bash
node scripts/seed-skills.mjs
node scripts/seed-globals.mjs
```

---

## Deployment

Designed to deploy on **Vercel** with a managed PostgreSQL database (e.g., Neon, Supabase, Vercel Postgres).

1. Push to GitHub
2. Import project on Vercel
3. Add environment variables (`DATABASE_URI`, `PAYLOAD_SECRET`, `NEXT_PUBLIC_SERVER_URL`)
4. Deploy

---

## License

MIT
