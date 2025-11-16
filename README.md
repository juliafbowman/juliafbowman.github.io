# ₊˚⊹ My Personal Website ˚⊹₊

My SvelteKit personal website, built to feel personal and expressive.  
It features Wikipedia-inpsired layouts, a custom Finder UI, and a mix of academic, professional, and personal sections.

Hosted on **GitHub Pages**.

## About Me

I’m **Julia Bowman**, a Computer student at UIC and a software engineer who appreciates  
thoughtful UI design and building tools that help people.

I care a lot about:
<p style="margin-left: 16px;">✦ accessible interfaces </p>
<p style="margin-left: 16px;">✦ organizing information creatively </p>
<p style="margin-left: 16px;">✦ unique coding projects  </p>

This site is my attempt in expressing my appreciation for the things that I care about 🎐

## Features

### 🪼 Finder-Style Navigation
A custom `Finder.svelte` component provides:
- Sidebar navigation (Experience, Academics, Personal)
- Scrollable content window
- Responsive and mobile-friendly design

### 🫧 Background Pages
Pages like `/contact` and `/inmybag/bag` include:
- Wikipedia-style background image grids
- A contact card centered on the page
- Individual captions with links

### 🪷 Static GitHub Pages Deployment
Using `@sveltejs/adapter-static`, the site builds to static HTML.

## Tech Stack

<p style="margin-left: 16px;"><strong>🃖 SvelteKit</strong></p>

<p style="margin-left: 16px;"><strong>🃚 JavaScript / TypeScript</strong></p>

<p style="margin-left: 16px;"><strong>🃜 Vite</strong></p>

<p style="margin-left: 16px;"><strong>🃁 @sveltejs/adapter-static</strong></p>

<p style="margin-left: 16px;"><strong>🂺 GitHub Pages</strong></p>

## Local Development 

Clone the repository:

```bash
git clone https://github.com/juliafbowman/website.git
```

Install dependencies:

```
npm install
```

Start the dev server:
```
npm run dev
```

Build for production:
```
npm run build
```

Preview the built site:
```
npm run preview
```

## Deployment (GitHub Pages)

This project uses a dynamic base path in svelte.config.js:
```
paths: {
  base: process.env.NODE_ENV === 'production' ? '/website' : ''
}
```
To deploy:
- Run ```npm run build```
- Commit and push the build changes
- Go to Settings → Pages
- Select the branch where build outputs
- GitHub Pages publishes automatically

---




<p align="left">
  <img src="https://img.shields.io/badge/SvelteKit-FF3E00?style=for-the-badge&logo=svelte&logoColor=white" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Pages-181717?style=for-the-badge&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/HTML%20%26%20CSS-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
</p>

