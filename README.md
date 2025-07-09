# 🎬 Mini Movie Explorer

Mini Movie Explorer is a single-page React application that allows users to search for movies using the OMDb API and manage a personal watchlist. It includes responsive design, a watchlist saved to localStorage, and additional enhancements like movie detail drawer, dark mode, and reordering options.

---

## ✨ Features

### ✅ Core Features
- 🔍 **Search UI**
  - Debounced search input (500ms delay)
  - Fetches movie results via OMDb API (no key required under 1,000/day)
  - Displays up to 10 results with poster, title, and year

- 🎞️ **Watchlist**
  - Add movies to a personal watchlist
  - Prevents duplicate entries
  - Data persisted across sessions using `localStorage`

- 📱 **Responsive Layout**
  - Mobile-first UI
  - Grid/column switch at `768px+` screen size

- 🧼 **Clean Code Architecture**
  - Functional components with hooks (`useState`, `useEffect`)
  - Debouncing handled using custom hook (`useDebounce`)
  - Organized folder structure (`components/`, `hooks/`, `styles/`)
  - Type safety via PropTypes

---

### 🌟 Stretch Features
- 📖 **Movie Details Drawer**  
  Click on a movie card to reveal a side drawer showing:
  - Full plot
  - IMDb rating
  - Director, actors, and genre  
  *(Requires an extra API call using `i=imdbID`)*

- 🌓 **Dark Mode Toggle**  
  - Light/dark theme switcher using Tailwind CSS variables or plain CSS
  - Theme state stored in `localStorage` for persistence

- 🔀 **Reorder Watchlist**
  - Drag and drop to rearrange items *(or use up/down arrow controls)*

- ❌ **Remove Items from Watchlist**
  - Remove individual items directly from the watchlist panel

---

## 🚀 Getting Started

### 🧰 Prerequisites
- Node.js and npm installed

### 🔧 Setup

```bash
# Clone the repo
git clone https://github.com/your-username/mini-movie-explorer.git
cd mini-movie-explorer

# Install dependencies
npm install

# Start the development server
npm run dev

# Open your browser
http://localhost:5173
```

### 📦 Build for Production

```bash
npm run build
```

---

## 🧠 How I Approached It

This project was developed from scratch using React and Vite. I focused on:

- Building reusable, clean components (e.g. `SearchBar`, `MovieCard`, `WatchlistPanel`)
- Using a custom hook for debounced input
- Storing data locally to avoid backend complexity
- Creating a mobile-first responsive design
- Keeping the UX simple, keyboard-friendly, and error-tolerant

---

## 📁 Folder Structure

```
src/
├── components/
│   ├── SearchBar.jsx
│   ├── MovieCard.jsx
│   ├── WatchlistPanel.jsx
│   └── MovieDrawer.jsx         # (Stretch feature)
├── hooks/
│   └── useDebounce.js
├── styles/
│   └── global.css
├── App.jsx
├── main.jsx
```

---

## 🛠️ Tech Stack

- React 18+ (Functional Components + Hooks)
- Vite (Development Bundler)
- OMDb API (Public demo key)
- CSS Modules / Tailwind CSS (for styling)
- PropTypes (for component type-checking)
- localStorage (for watchlist persistence)

---

## 📷 Demo & Walkthrough

- [ ] Optional Loom walkthrough (2–3 min)
- [ ] Optional screenshots in `/docs`

---

## 📝 License

Open-source and free to use.

---

## 🙌 Acknowledgements

Thanks to [OMDb API](http://www.omdbapi.com/) for making movie data publicly available.

---
