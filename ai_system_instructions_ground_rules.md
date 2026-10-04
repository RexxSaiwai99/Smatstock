# AGENTS.md — Standing Orders for AI Studio

## Technical Constraints & Guidelines
1. **Single-File Architecture:** Deliver ALL functionality in a single `index.html` file (HTML5 + Tailwind CSS CDN + Alpine.js / Vanilla JS). No npm, build steps, or external backend.
2. **Persistence:** Use browser `localStorage` to save registered students, active loans, and modified inventory stock levels.
3. **Design Standard:** Clean, modern, high-contrast UI (dark slate / indigo theme) appropriate for an advanced robotics lab dashboard.

## Multi-Page Navigation Simulation
* Implement smooth single-page tab switching between:
  1. `Auth / Sign-Up / Login`
  2. `Analytics Dashboard`
  3. `Master Inventory Catalog`
  4. `Borrow & Return Desk`
  5. `Student / Admin Profile`