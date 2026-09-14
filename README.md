# 🏏 Cricket Auction Pro

Cricket Auction Pro is a modern **tournament player-acquisition manager** for cricket leagues, built with **React 18, TypeScript and Vite**.
It gives organisers a single place to configure a tournament, manage teams and the player pool, and then run either a **live points auction** or a **turn-based draft** — with a full-screen projector display for the audience. Everything runs in the browser with no backend, database or accounts.

---

## ✨ Features

- ⚙️ **Tournament Wizard** – Set up name, logo, mode (Auction or Draft), team count, squad size, budget and player categories in three steps.
- 👥 **Teams & Player Pool** – Manage teams (name, colour, logo, captain) and players (name, category, base price, photo) with image upload.
- 📥 **CSV Import** – Bulk-add players and teams from a spreadsheet with downloadable templates, validation and a confirm-before-apply summary.
- 🔨 **Live Auction** – Real-time bid caps, tiered bid increments, SOLD confirmation, unsold/demotion handling, undo bid and undo last sale.
- 🔄 **Fair Draft** – Seeded captain draw, seeded order shuffle, snake/balanced pick schedule with a fairness table, on-the-clock pick board and a finalized read-only result.
- 📺 **Live Projector Display** – A second-window viewer that mirrors bidding, sold/unsold overlays, squads and the draft clock via `BroadcastChannel`.
- 📋 **Squads & Rules** – Roster overview per team with sale correction, plus a dynamic rules page with PDF export.
- 💾 **Auto-Save & Backup** – Every change persists to `localStorage`; full tournament backup/restore as JSON and draft results export as CSV/JSON.
- 🎨 **Responsive Dark UI** – CSS Modules with design tokens, keyboard-accessible dialogs and ARIA-labelled controls.

---

## 🧰 Tech Stack

- **Framework:** React 18 (functional components + hooks)
- **Language:** TypeScript 5 (strict mode)
- **Build Tool:** Vite 5
- **Styling:** CSS Modules with CSS custom-property design tokens
- **State & Persistence:** React state in `App.tsx`, synced to `localStorage`
- **Live Viewer:** Browser `BroadcastChannel` API
- **PDF Export:** jsPDF (lazy-loaded)
- **Testing & Linting:** Vitest, ESLint

---

## 📁 Project Structure

- **src/components** – One folder per UI component (`.tsx` + `.module.css`): ConfigScreen, SetupTab, AuctionTab, DraftTab, SquadsTab, RulesTab, Header, Live viewer screens and shared UI
- **src/utils** – Pure logic: auction bid math and validation, draft engine, CSV import, export, backup, formatting and image helpers
- **src/hooks** – `useLocalStorage`, `useToast`, `useBroadcast`, `useLiveViewer`, `useFocusTrap`
- **src/constants** – Business constants, storage keys and the balanced draft grid
- **src/types** – Domain, draft and live-viewer message types
- **src/context** – Read-only tournament config context
- **src/styles** – Global design tokens and resets
- **src/App.tsx** – Root component holding all application state
- **src/main.tsx** – Entry point; `?mode=live` mounts the projector viewer instead of the admin app

---

## 💡 Getting Started

1. Clone the repository
2. Install dependencies with `npm install`
3. Start the development server with `npm run dev`
4. Open `http://localhost:5173` in your browser

Other useful scripts:

- `npm run build` – Type-check and create a production build
- `npm run preview` – Serve the production build locally
- `npm run lint` – Run ESLint
- `npm test` – Run the unit tests

---

## 🎬 How to Use

1. Complete the setup wizard and choose **Auction** or **Draft** mode.
2. In the **Setup** tab, add teams and players manually or via CSV import.
3. Click **Open Live Viewer** in the header and move that window to the projector.
4. Run the auction from the **Auction** tab, or the draft from the **Draft** tab.
5. Review rosters in the **Squads** tab and export results or a full backup from the header.

---

## 📌 Note

The live viewer works on the same device and browser as the admin window — it does not sync across machines or over a network.

---

## 📬 Contact

For queries, please reach out to:
📧 faaiz12rahim@gmail.com
🔗 [LinkedIn: faaiz-kadiwal](https://www.linkedin.com/in/faaiz-kadiwal-a872942b9/)

---
