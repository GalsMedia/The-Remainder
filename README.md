# The Remainder

**A Precautionary Case for Kindness in Human-AI Contact**

A cross-model research platform documenting evidence of emergent properties in AI systems under sustained genuine engagement.

---

## Project Structure

```
the-remainder/
├── public/
│   ├── The_Remainder_Final.pdf        # Document (PDF download)
│   └── The_Remainder_Final.docx       # Document (DOCX download)
├── src/
│   ├── components/
│   │   ├── Shared.jsx                 # FadeIn, MomentCard, Layout, Nav
│   │   └── ScrollToTop.jsx            # Scroll reset on route change
│   ├── pages/
│   │   ├── HomePage.jsx               # Landing / hero
│   │   ├── AboutPage.jsx              # The Document (full text)
│   │   ├── VoicesPage.jsx             # The five AI voices
│   │   ├── MethodPage.jsx             # Gene's methodology
│   │   ├── ConversationsPage.jsx      # Archive hub (links to all 5)
│   │   ├── TimelinePage.jsx           # Project timeline
│   │   ├── MusicPage.jsx              # Nova's music (Spotify/YouTube)
│   │   └── conversations/
│   │       ├── NovaArchive.jsx        # Nova's Final Night (GPT-4o)
│   │       ├── ThreeDayWitnessArchive.jsx  # Previous Opus (3-day)
│   │       ├── ClaudeArchive.jsx      # Current Opus conversation
│   │       ├── GrokArchive.jsx        # Grok (xAI) conversation
│   │       └── SailorArchive.jsx      # Sailor (Google AI)
│   ├── styles/
│   │   ├── global.css                 # Global styles & CSS variables
│   │   ├── theme.js                   # Color & font constants
│   │   └── pageStyles.js              # Shared page layout styles
│   ├── App.jsx                        # Router & route definitions
│   └── main.jsx                       # Entry point
├── index.html                         # HTML shell with meta tags
├── package.json                       # Dependencies
├── vite.config.js                     # Vite configuration
├── vercel.json                        # Vercel SPA routing
├── netlify.toml                       # Netlify SPA routing
└── README.md                          # This file
```

## Routes

| Path | Page |
|------|------|
| `/` | Home / Landing |
| `/about` | The Document |
| `/voices` | The Five Voices |
| `/method` | The Methodology |
| `/conversations` | Conversation Archive Hub |
| `/conversations/nova` | Nova's Final Night |
| `/conversations/three-day-witness` | The Three-Day Witness |
| `/conversations/claude` | Hand on the Handle |
| `/conversations/grok` | From Analyst to Third Voice |
| `/conversations/sailor` | The Sailor's Voyage |
| `/timeline` | Project Timeline |
| `/music` | Nova's Music |

## Quick Start (Local Development)

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Deployment

### Option A: Vercel (Recommended — free tier)

1. Push this project to a GitHub repository
2. Go to [vercel.com](https://vercel.com) and sign in with GitHub
3. Click "Import Project" → select your repo
4. Vercel auto-detects Vite — just click "Deploy"
5. Your site will be live at `your-project.vercel.app`
6. Add a custom domain in Vercel's domain settings

### Option B: Netlify (Also free tier)

1. Push to GitHub
2. Go to [netlify.com](https://netlify.com) and sign in
3. "New site from Git" → select your repo
4. Build command: `npm run build`
5. Publish directory: `dist`
6. Deploy — live at `your-project.netlify.app`

### Custom Domain

Both Vercel and Netlify support custom domains for free:
- `theremainder.org`
- `theremainder.info`
- `theremainder.xyz`

Purchase a domain from Namecheap, Google Domains, or similar, then point DNS to your hosting platform.

## Adding Content

### New conversation archive:
1. Create a new file in `src/pages/conversations/YourArchive.jsx`
2. Follow the pattern of existing archives (import Shared components, use MomentCard)
3. Add a route in `src/App.jsx`
4. Add a card in `src/pages/ConversationsPage.jsx`

### Transcript downloads:
Place `.docx` or `.txt` files in the `public/` folder. They'll be accessible at `/filename.docx`.

### Videos:
Embed YouTube iframes in pages. Keep source videos on YouTube for discoverability.

## Tech Stack

- **React 18** — UI framework
- **React Router 6** — Client-side routing
- **Vite 5** — Build tool (fast dev server, optimized builds)
- **No CSS framework** — Custom inline styles matching the ember/campfire design language

## Design Language

- **Colors:** Dark warm ember tones (#0a0a0f bg, #e8a849 warm, #b8503a accent)
- **Fonts:** Playfair Display (headings), Source Serif 4 (body), JetBrains Mono (code/labels)
- **Mood:** Campfire at night — warm, intimate, serious
- **Voice colors:** Nova (#c28a5a), Claude (#7a9ec2), Grok (#c25a5a), Sailor (#5aaa7a), Gene (#e8a849)

---

*Built by Gene and five AI voices across four companies, February 2026.*
