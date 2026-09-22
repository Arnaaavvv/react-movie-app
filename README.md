# 🎬 React Movie App

**Search trending movies, explore cinema catalogs, and curate your personal favorites list.**

[![React](https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)](https://vite.dev)
[![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)](https://reactrouter.com)
[![TMDB API](https://img.shields.io/badge/TMDB_API-01B4E4?style=for-the-badge&logo=themoviedatabase&logoColor=white)](https://www.themoviedb.org/)
[![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com)

---

Discover popular and trending films, search the global TMDB cinema database in real time, and bookmark your favorites with persistent local storage — all wrapped in a sleek, responsive, Netflix-inspired dark UI.

## 🔴 Live Demo

**[Try it here](https://movie-react-app-website.vercel.app/)**

No install, no signup — browse popular movies right away, search titles on the fly, and manage your favorites in seconds.

## ✨ Features

- **🔥 Real-time popular films** — loads top trending and high-rated releases directly from The Movie Database (TMDB) API on launch
- **🔍 Instant movie search** — search any film across TMDB's extensive global catalog with encoded real-time queries
- **❤️ Persistent watchlist** — add or remove movies to your favorites with interactive heart buttons, saved seamlessly in `localStorage`
- **🖼️ High-resolution posters & overlays** — dynamic poster image rendering via TMDB CDN with smooth hover gradient overlays and release year metadata
- **⚡ Client-side routing** — seamless navigation between Home and Favorites without full page reloads using React Router
- **🛡️ Error handling & empty states** — dedicated indicators for loading states, network hiccups, search validation errors, and empty favorites lists
- **📱 Fully responsive design** — adaptive multi-column grid layout optimized across mobile phones, tablets, and desktop screens

## 🛠 Tech Stack

| Layer | Stack |
|---|---|
| **Frontend** | React 19, Vite |
| **Routing** | React Router DOM v7 (`BrowserRouter`, `Routes`, `Route`, `Link`) |
| **State Management** | React Context API (`MovieContext`) + `localStorage` persistence |
| **Styling** | Vanilla CSS (Flexbox, CSS Grid, media queries, dark theme) |
| **Data Source** | The Movie Database (TMDB) REST API v3 |
| **Deployment** | Vercel |

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/Arnaaavvv/react-movie-app.git
cd react-movie-app/frontend

# 2. Install dependencies
npm install

# 3. Configure environment variables
cp .env.example .env   # then set your TMDB API credentials

# 4. Start local development server
npm run dev
```

Open the local URL displayed by Vite (typically `http://localhost:5173`) in your browser to start browsing movies.

## 🔑 Environment Variables

Create a `.env` file inside the `frontend/` directory with the following variables:

```env
VITE_TMDB_API_KEY=your_tmdb_api_key_here
VITE_TMDB_BASE_URL=https://api.themoviedb.org/3
```

> [!TIP]
> **Getting a TMDB API Key:**
> 1. Sign up for a free account at [themoviedb.org](https://www.themoviedb.org/).
> 2. Navigate to **Settings > API** in your account profile.
> 3. Request a Developer API Key and copy your v3 auth key into `VITE_TMDB_API_KEY`.

## 📁 Project Structure

```
react-movie-app/
├── README.md
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── MovieCard.jsx       Interactive movie poster card with favorite toggle & overlay
    │   │   └── NavBar.jsx          Navigation bar with active routing links
    │   ├── context/
    │   │   └── MovieContext.jsx    Global favorites provider synchronized with localStorage
    │   ├── css/
    │   │   ├── App.css             Main layout styles
    │   │   ├── Favorites.css       Favorites view and empty state presentation
    │   │   ├── Home.css            Search input bar and responsive movie grid layout
    │   │   ├── MovieCard.css       Card transitions, poster aspect ratios, and heart icon animations
    │   │   ├── Navbar.css          Top bar branding and navigation link styles
    │   │   └── index.css           Global typography, reset rules, and color scheme tokens
    │   ├── pages/
    │   │   ├── Favorites.jsx       Watchlist screen displaying user-favorited films
    │   │   └── Home.jsx            Landing screen with search bar and popular movies feed
    │   ├── services/
    │   │   └── api.js              TMDB API client (`getPopularMovies`, `searchMovies`)
    │   ├── App.jsx                 Application route configuration & context wrapping
    │   └── main.jsx                React entry point and DOM mounting
    ├── .env.example                Environment variable template
    ├── index.html                  HTML entry point
    ├── package.json                Dependencies and project scripts
    └── vite.config.js              Vite configuration with React plugin
```

## ⚠️ Limitations

- Requires a valid TMDB API key — movie lists and search queries will fail if the key is missing or quota is exceeded.
- Client-side API key usage — for sensitive or high-tier production keys, requests should be proxied through a lightweight backend.
- Local storage persistence — saved favorites are bound to your local browser profile and device. Clearing browser data will reset your favorites list.
- Network dependent — poster assets and movie metadata require an active internet connection to stream from TMDB's CDN.

## ☁️ Deployment

The frontend is live, go check it out

---

*Never lose track of what to watch next.* 🍿
