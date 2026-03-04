# Portfolio
[Visit Portfolio](https://waqasahmedportfolio.netlify.app/)
# 🌐 Waqas Ahmed — Personal Portfolio Website

> A fully responsive, single-file personal portfolio for **Waqas Ahmed** — AI Developer & Full Stack Engineer — featuring a dark/light theme toggle, skills filtering, scroll animations, an AI-powered chatbot assistant, and three role-specific downloadable CVs.

---

## 📌 Overview

This is a clean, professional portfolio website built with **vanilla HTML, CSS, and JavaScript** — no frameworks, no build tools. It showcases Waqas's background as an AI/ML researcher, mobile developer, and web engineer — with interactive sections for skills, projects, experience, publications, and contact.

A standout feature is the **Groq-powered AI chatbot** embedded in the bottom-right corner, which represents Waqas to visitors, answers questions on his behalf, and uses live LLM inference to respond to recruiters and clients — even when Waqas is offline.

---

## ✨ Features

- 🌗 **Dark / Light Mode** — Persistent theme toggle with `localStorage` + `prefers-color-scheme` support
- 🤖 **AI Chatbot Assistant** — Groq-powered chatbot representing Waqas using `llama-3.3-70b-versatile`, with conversation history, quick-chip prompts, and graceful error handling
- 📄 **3 Role-Specific CVs** — Dropdown to download AI, Web, or Mobile App resume variants
- 🎛️ **Skills Filter** — Toggle between All / AI/ML / Mobile / Web skill categories with smooth fade animations
- 📜 **Scroll Reveal Animations** — Cards and sections animate in using `IntersectionObserver`
- 📱 **Fully Responsive** — Mobile-first design that collapses gracefully to hamburger nav on small screens
- 📬 **Working Contact Form** — Integrated with [Formspree](https://formspree.io) for serverless email delivery with client-side validation
- 🔝 **Back to Top Button** — Fixed bottom-left button with pulse animation when near the page bottom
- 🧭 **Active Nav Tracking** — Highlights the current section in the navbar as the user scrolls
- 🎓 **Publications Section** — Dedicated section for research papers with journal and author details
- ⌨️ **Keyboard Shortcut** — `Ctrl + ↑` scrolls to top from anywhere on the page

---

## 🖥️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Structure** | HTML5 (single file) |
| **Styling** | CSS3 with custom properties (design tokens) |
| **Interactivity** | Vanilla JavaScript (ES2020+) |
| **UI Framework** | Bootstrap 5.3 (grid, navbar, dropdown) |
| **Icons** | Font Awesome 6.4 |
| **Fonts** | Poppins (Google Fonts) |
| **AI Chatbot** | Groq API — `llama-3.3-70b-versatile` |
| **Contact Form** | Formspree (serverless) |

---

## 📁 Project Structure

```
Portfolio/
├── index.html                        # Entire site — HTML + CSS + JS
├── style.css                         # External stylesheet (supplemental)
├── script.js                         # External JS (supplemental)
├── chatbot.js                        # Chatbot logic (supplemental)
├── contact.php                       # PHP contact handler (optional backend)
│
├── assets/
│   └── images/
│       ├── dp.png                    # Profile photo (hero + chatbot avatar)
│       ├── logo.png                  # Site logo
│       ├── eeg.jfif                  # EEG project thumbnail
│       ├── lung.jfif                 # Lung disease project thumbnail
│       └── web.jfif                  # Hospital system project thumbnail
│
└── resumes/
    ├── WAQAS AHMED - AI.pdf          # AI-focused resume
    ├── WAQAS AHMED - WEB.pdf         # Web development resume
    └── WAQAS AHMED - MOB APP.pdf     # Mobile development resume
```

---

## 🚀 Getting Started

### Option A — Open Directly (No Server)

```bash
# Clone the repository
git clone https://github.com/waqasahmed5554/portfolio.git
cd portfolio

# Open in browser
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

### Option B — Local Dev Server (Recommended)

```bash
# Using Python
python3 -m http.server 8080

# Using Node.js
npx serve .

# Then visit
http://localhost:8080
```

---

## 🤖 AI Chatbot Configuration

The portfolio includes an embedded Groq chatbot in the bottom-right corner. It represents Waqas to visitors using a custom system prompt loaded with his full profile — skills, projects, experience, and availability.

### Setup Your Own Key

1. Get a free API key at [console.groq.com](https://console.groq.com)
2. Open `index.html` and find the chatbot config block near the bottom:

```javascript
const GROQ_API_KEY = 'YOUR_GROQ_API_KEY_HERE';
const GROQ_MODEL   = 'llama-3.3-70b-versatile';
```

3. Replace with your key and save.

### Chatbot Capabilities

| Prompt | Response |
|--------|---------|
| "His skills" | Lists all technical skills by category |
| "Recent projects" | Describes the 3 featured projects |
| "Available for hire?" | Explains availability and domains |
| "Contact details" | Provides email, phone, and GitHub |
| Any custom question | LLM responds from the profile knowledge base |

> ⚠️ **Security Note:** The API key is embedded in the HTML. Do not commit it to a public repo. Use a proxy backend or environment variable injection for production deployments.

---

## 🎨 Design System

The site uses CSS custom properties for a consistent, themeable design:

| Token | Light | Dark |
|-------|-------|------|
| `--bg-color` | `#ffffff` | `#0f172a` |
| `--primary` | `#2563eb` | `#3b82f6` |
| `--text-color` | `#1e293b` | `#f1f5f9` |
| `--card-bg` | `#ffffff` | `#1e293b` |
| `--border-color` | `#e2e8f0` | `#334155` |

Theme preference is saved to `localStorage` and respects the OS `prefers-color-scheme` setting automatically.

---

## 📬 Contact Form Setup

The contact form posts to [Formspree](https://formspree.io). To use your own endpoint:

1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form and copy your endpoint URL
3. In `index.html`, update the form action:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

---

## 📸 Sections at a Glance

| Section | Description |
|---------|-------------|
| **Hero** | Name, title, description, social links, CV download dropdown |
| **About** | Bio, personal info grid, stats (experience, projects, publications) |
| **Skills** | Filterable skill cards across AI/ML, Mobile, and Web categories |
| **Projects** | 3 featured project cards with tags, descriptions, and tech stack chips |
| **Experience** | Alternating timeline of education and work history |
| **Publications** | Research paper card with journal and link |
| **Contact** | Info cards + working Formspree-integrated contact form |

---

## 🔗 Live Links

| Platform | Link |
|----------|------|
| **GitHub** | [github.com/waqasahmed5554](https://github.com/waqasahmed5554) |
| **Google Scholar** | [View Publications](https://scholar.google.com/citations?user=W3NTHlUAAAAJ&hl=en) |
| **Email** | waqasahmed.rk@gmail.com |

---

## 🤝 Contributing

Found a bug or want to suggest an improvement?

1. Fork the repository
2. Create your branch: `git checkout -b fix/your-fix`
3. Commit changes: `git commit -m 'Fix: description'`
4. Push: `git push origin fix/your-fix`
5. Open a Pull Request

---

---

<p align="center">Designed & developed by <strong>Waqas Ahmed</strong> · Sargodha, Pakistan 🇵🇰</p>
