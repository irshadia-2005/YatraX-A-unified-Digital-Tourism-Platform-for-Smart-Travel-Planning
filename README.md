# YatraX — Frontend

> A modern, responsive web frontend for **YatraX**, a full-stack travel discovery platform for India.

Built with **vanilla HTML, CSS, and JavaScript** — no frameworks, no build step. Consumes the YatraX Spring Boot REST API for live destination data.

**Backend repo:** [github.com/mdatyabnadim-sys/YatraX-backend](https://github.com/mdatyabnadim-sys/YatraX-backend)

**Live demo:** [yatrax-eight.vercel.app](https://yatrax-eight.vercel.app)

---

## ✨ Features

- **Destination catalog** — 6 major Indian destinations with detailed sub-locations
- **Live API integration** — destinations fetched from Spring Boot REST API
- **User authentication** — register, login, and persistent sessions
- **Reviews & comments** — post reviews, like, dislike, and reply (backend-persisted)
- **Wishlist** — save destinations with a heart button
- **Hand-drawn offline maps** — custom SVG maps that work without internet
- **Budget planner** — estimate trip costs by departure city
- **Booking links** — curated hotels, bike rentals, car rentals, and tour packages

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 |
| Styling | CSS3 (Grid, Flexbox) |
| Scripting | Vanilla JavaScript (ES6+) |
| API calls | Fetch API |
| Fonts | Google Fonts (DM Sans, Playfair Display) |
| Hosting | Vercel |

**No frameworks. No build tools. No `node_modules`.**

---

## 📁 File Structure

```text
yatrax-frontend/
├── index.html            # Home page
├── index.css             # Home page styles
├── index.js              # Home page logic
├── destination.html      # Generic destination page (Agra, Jaipur, Kerala, Ladakh)
├── destination.css
├── destination.js
├── goa.html              # Custom Goa page
├── goa.css
├── goa.js
├── kashmir.html          # Custom Kashmir page
├── kashmir.css
├── kashmir.js
├── location.html         # Generic sub-location page
├── location.css
├── location.js
├── auth.html             # Login / Signup
├── auth.css
├── auth.js
├── wishlist.html         # Saved destinations
├── wishlist.css
├── wishlist.js
├── common.css            # Shared styles
├── common.js             # Shared auth + API base
├── reviews.css           # Reviews styles
└── reviews.js            # Reviews logic

## 🔗 API Integration

```javascript
const API_BASE = "https://yatrax-backend-production.up.railway.app/api";

fetch(API_BASE + "/destinations")
  .then(r => r.json())
  .then(data => renderDestinations(data));

## 🎨 Design

- Dark forest-green theme with mint accents
- Playfair Display + DM Sans typography
- Card-first layout with subtle hover animations
- Fully responsive (desktop, tablet, mobile)

📄 License
MIT
