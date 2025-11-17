# AIBA Sylhet - Hall of Fame

A dynamic, single-file website powered by Tailwind CSS (CDN) and Alpine.js. It includes search, filters, sorting, dark mode, a modal detail view, and a rich demo dataset.

## Features

- Responsive UI with a clean hero section and brand accents
- AIBA-style green→blue theme (emerald/blue) with gradient highlights
- Live search across title, team/authors, and tags
- Filters: category chips and year dropdown
- Sorting: newest/oldest and title A→Z/Z→A
- Pagination: Load more
- Detail modal with full description and meta
- Dark mode toggle (persists in localStorage)
- Stats summary (total, categories, latest year, people involved)

## Structure

- `index.html` — Entire app (no build step). Demo data is embedded with remote placeholder images.

## Quick start (Windows / PowerShell)

Open the file in your default browser:

```powershell
Start-Process .\index.html
```

## Customizing data

Edit the `seed()` function near the bottom of `index.html`. Each achievement object supports:

```js
{
  id: Number,
  title: String,
  team: String,         // team/authors (preferred)
  subtitle: String,     // optional legacy field; shown if team is missing
  date: 'YYYY-MM-DD',   // sortable ISO-like date
  category: 'Competition' | 'Research' | 'Event' | 'Sports' | 'Community',
  location: String,
  tags: String[],
  image: String,        // URL or relative path
  description: String,
}
```

To use local images, place them next to `index.html` (e.g., in an `images/` folder) and update the `image` field to relative paths like `images/achievement-1.jpg`.

## Notes

- Tailwind and Inter font are loaded via CDN; Alpine.js provides the interactivity.
- No external CSS or build tooling required. Everything is in a single HTML file.

