# 🌐 Moayed Ghanmi - Interactive Developer Portfolio & CMS

A complete, high-performance interactive developer portfolio and password-protected admin dashboard for **Moayed Ghanmi**. Built with **Next.js 16 (App Router)**, **React 19**, **Tailwind CSS**, **HTML5 Canvas & 3D Math**, and **Supabase (PostgreSQL)**, optimized for zero-latency deployment on **Vercel**.

---

## ✨ Features

### 🎮 3D Canvas Animations & Creative UI
- **Hero 3D Particle Constellation**: Interactive particle starfield with depth scaling, velocity interpolation, radial gradient glowing nodes, and proximity connection lines tracking cursor coordinates.
- **About 3D Geometric Sphere**: Interactive rotating 3D sphere composed of glowing violet and cyan nodes with golden spiral projection reacting to mouse movements.
- **3D Card Perspective Tilt**: Physics-based perspective tilt (`rotateX`, `rotateY`, `scale3d`) applied to all featured project cards.
- **Dark Glassmorphism Styling**: Replicated the exact dark theme (`#0a0a0a`), glassmorphic panels (`backdrop-blur-xl bg-neutral-950/70 border-b border-white/5`), and gradient accents.
- **Expertise Skills Matrix**: 8 categorized technology cards (React, Node.js, Figma, Three.js, PostgreSQL, TypeScript, AWS, Git) with glowing hover micro-interactions.
- **Interactive Contact Form**: Client-side validated contact form with submission feedback.

### 🔐 Password-Protected Admin Dashboard & CMS
- **Route Protection**: Next.js proxy/middleware protecting `/admin/dashboard` with session verification.
- **Admin Authentication**: Secure login at `/admin/login` using HTTP-only cookies and bcrypt/hash comparison.
- **Full Projects & Skills CRUD**:
  - **Projects Management**: Create, view, search, edit, and delete projects with real-time sync to the public showcase.
  - **Skills Management**: Add new technologies, pick custom gradient swatches, select from preset Lucide/Iconify icons, edit categories, and delete with live portfolio reflection.
- **Settings & Security**:
  - Change and update the admin password directly from the dashboard.
- **Resilient Fallback Mode**: Works 100% out-of-the-box in local demo mode, and automatically connects to live PostgreSQL when Supabase environment variables are provided.

---

## 🚀 Quick Start

### 1. Installation & Local Development

```bash
# Clone the repository
git clone https://github.com/moayed-ghanmi/portfolio.git
cd portfolio

# Install dependencies
npm install

# Start development server on port 3030
npm run dev
```

Visit **[http://localhost:3030](http://localhost:3030)** in your browser.

---

## 🔐 Admin Portal Credentials

- **URL**: [http://localhost:3030/admin/login](http://localhost:3030/admin/login)
- **Default Password**: `admin123456`
- **Dashboard**: [http://localhost:3030/admin/dashboard](http://localhost:3030/admin/dashboard)

---

## 🗄️ Supabase Cloud Database Setup

To connect live cloud PostgreSQL:

1. Create a project at [supabase.com](https://supabase.com).
2. Go to the **SQL Editor** in your Supabase dashboard.
3. Open [`supabase/schema.sql`](./supabase/schema.sql), copy its content, and click **Run**.
4. In Supabase, go to **Project Settings** -> **API**, and copy your credentials into `.env.local`:
   ```env
   NEXT_PUBLIC_SUPABASE_URL=https://your-project-id.supabase.co
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key-here
   SUPABASE_SERVICE_ROLE_KEY=your-service-role-key-here
   ```
5. Restart your development server (`npm run dev`).

---

## 🚢 GitHub & Vercel Deployment Guide

### Step 1: Push to GitHub

```bash
git init
git add .
git commit -m "feat: complete interactive developer portfolio and admin dashboard for Moayed Ghanmi"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin main
```

### Step 2: Deploy to Vercel

1. Log in to [Vercel](https://vercel.com) and click **"Add New..."** &rarr; **Project**.
2. Import your GitHub repository.
3. In the **Environment Variables** section, add:
   - `NEXT_PUBLIC_SUPABASE_URL` = `https://your-project.supabase.co`
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY` = `your-anon-key`
   - `SUPABASE_SERVICE_ROLE_KEY` = `your-service-role-key`
   - `ADMIN_PASSWORD` = `your-custom-admin-password`
4. Click **Deploy**. Vercel will build and launch your production site with a global CDN and edge caching!

---

## 📜 License
MIT License. Created for **Moayed Ghanmi**.
