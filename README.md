# STUDENT — Personal Portfolio Website

A high-performance single-page personal portfolio engineered with a zero-bloat philosophy, light theme aesthetics, and native web standards.

**Owner**: STUDENT  
**Role**: Computer Science Student | Developer | Technology Enthusiast  
**Education**: B.Tech Computer Science and Engineering, KL University (2025–2029)  
**Location**: Vijayawada, Andhra Pradesh, India  

---

## Technical Stack & Constraints

- **Frontend**: HTML5, CSS3, JavaScript (ES6+), React 18, ReactDOM, Vite.
- **Backend**: Node.js utilizing **native HTTP modules** (`node:http`, `node:url`, `node:fs`, `node:path`, `node:stream`).
- **Strict Compliance**:
  - Zero CSS frameworks (No Tailwind, No Bootstrap, No Material UI).
  - Pure CSS Custom Properties design system with strict light-mode palette.
  - Zero backend frameworks (No Express.js, No Fastify).
  - Zero TypeScript (Pure ES6+ JavaScript).
  - No external database dependencies.

---

## Architecture Overview

```
PORTFOLIO/
├── index.html                  # Semantic HTML5 entry, SEO/OG tags & web font loaders
├── vite.config.js              # Vite bundler & backend API proxy configuration
├── package.json                # Project dependencies and operational scripts
├── public/
│   └── resume.pdf              # Valid PDF academic and project summary
├── server/                     # Native Node.js HTTP Backend
│   ├── index.js                # Server entry point, port binding, graceful shutdown
│   ├── router.js               # Native URL router & static asset streamer
│   ├── controllers/
│   │   ├── contactController.js# Stream body parser, validation, honeypot filter
│   │   ├── dataController.js   # Health check & system metadata telemetry
│   │   └── githubController.js # GitHub proxy & profile telemetry
│   └── utils/
│       ├── bodyParser.js       # Safe chunked stream reader with size limits
│       └── response.js         # Standard JSON, CORS headers, error response helpers
├── src/                        # Modular Client Architecture
│   ├── main.jsx                # React DOM root initialization
│   ├── App.jsx                 # Single-page layout & in-page modal state manager
│   ├── config/
│   │   └── siteConfig.js       # Centralized metadata, navigation, & social links
│   ├── data/                   # Decoupled content layer
│   │   ├── profile.js          # Verified biography and technical focus areas
│   │   ├── education.js        # KL University B.Tech CSE details
│   │   ├── experience.js       # Real development journey and milestone timeline
│   │   ├── skills.js           # Categorized engineering competencies
│   │   ├── projects.js         # Authentic projects (DeviceBridge, SHORTCUT, SAPAS, DIAI, AXION, MY WORKS)
│   │   ├── services.js         # Technical offerings & collaboration areas
│   │   └── articles.js         # Technical writing & honest under-preparation state
│   ├── services/
│   │   └── api.js              # Native fetch client for backend endpoints
│   ├── styles/
│   │   ├── variables.css       # Design tokens (colors, spacing, shadows, typography)
│   │   ├── base.css            # Semantic reset, accessible focus, reduced motion rules
│   │   ├── components.css      # Handcrafted modular UI component styles
│   │   └── index.css           # Consolidated stylesheet bundle
│   └── components/
│       ├── common/             # Reusable UI primitives
│       │   ├── Navbar.jsx      # Fixed header with scrollspy, mobile menu & PDF resume
│       │   ├── SectionHeader.jsx # Standardized category eyebrow & headings
│       │   ├── Badge.jsx       # Status and technology pill indicators
│       │   ├── Modal.jsx       # Accessible dialog (ESC key, focus trap, scroll lock)
│       │   ├── Toast.jsx       # Non-intrusive feedback notification
│       │   └── Footer.jsx      # Semantic footer & back-to-top interaction
│       ├── sections/           # Section layouts
│       │   ├── Hero.jsx        # Headline, configurable status, and action buttons
│       │   ├── About.jsx       # Narrative, technical principles & academic profile
│       │   ├── Skills.jsx      # Categorized skill badges & domain groups
│       │   ├── Education.jsx   # Degree, institution, and academic period
│       │   ├── Projects.jsx    # Filterable project showcase with case study modal
│       │   ├── Experience.jsx  # Vertical development journey timeline
│       │   ├── Services.jsx    # Technical capabilities and collaboration scope
│       │   ├── GitHubShowcase.jsx # Safe fallback & GitHub API integration
│       │   ├── Articles.jsx    # Technical writing section with empty state
│       │   └── Contact.jsx     # Native HTTP contact form with live validation
│       └── modals/
│           ├── ProjectModal.jsx# In-depth 11-field project case study view
│           └── ArticleModal.jsx# Distraction-free article reader view
└── tests/
    ├── projects.test.js        # Phase 04 Featured Projects integrity tests
    ├── journey.test.js         # Phase 05 Journey & Services data integrity tests
    ├── phase06.test.js         # Phase 06 Articles & Validation tests
    └── server.test.js          # Native HTTP backend endpoint & static serving tests
```

---

## Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Run in Development Mode
Start the native Node.js backend:
```bash
npm run server
```
In another terminal, start the Vite development server:
```bash
npm run dev
```

### 3. Build & Run for Production
```bash
npm run build
npm run start
```
The native Node.js HTTP server will serve both the compiled frontend single-page application and the `/api` endpoints simultaneously on `http://localhost:5050`.

### 4. Run Automated Tests
```bash
npm test
```
"# portfolio" 
