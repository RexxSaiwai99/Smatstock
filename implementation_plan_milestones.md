# Streamlined Implementation Plan & Milestones (M0 - M6)

All milestones follow strict incremental construction to build an enterprise-grade RAI Lab Inventory Management System without unnecessary complexity.

---

### Milestone M0: High-Tech UI Layout, Theme Engine & Router Framework
* **Goal:** Establish a modern sci-fi/industrial dark theme UI with a sidebar navigation system, single-page tab router, toast notification system, and modal handlers.

### Milestone M1: Dual-Role Authentication & Student Registration
* **Goal:** Implement registration for students (Name, Student ID, Line ID, Batches 67–70, Major) and password-protected Admin login with quick-switch dev role shortcuts.

### Milestone M2: Master Lab Inventory Database & Pre-Seeding
* **Goal:** Load 30+ default robotics & AI lab items (oscilloscopes, NVIDIA Jetson modules, Raspberry Pis, motor drivers, multimeters) with location badges (Cabinet A1, Shelf B2, etc.) and real-time search/tag filters.

### Milestone M3: Advanced Analytics Command Center (10+ Insights)
* **Goal:** Build the primary dashboard featuring:
  1. Top 10 Most Borrowed Equipment Leaderboard
  2. Category Breakdown Chart & Stock Allocation
  3. Batch & Major Utilization Analytics (Batches 67, 68, 69, 70)
  4. Real-time Inventory Health & Availability Index Gauge
  5. Low Stock Emergency Center (Stock $\le 2$)
  6. Active Borrowers Overdue Risk Table (with direct Line ID tag copy)
  7. Peak Hours / Recent Activity Live Feed
  8. Equipment Location & Shelf Map Quick Finder
  9. Health & Damage Condition Ratio Metrics
  10. Fast Search & Multi-Tag Global Filter

### Milestone M4: Interactive Dedicated Borrow & Check-Out Desk
* **Goal:** Build a dedicated check-out workspace with an interactive item scanner/picker, auto-filled student credential cards, loan duration options (1 to 14 days), due date calculators, and quick stock reservation logic.

### Milestone M5: Interactive Dedicated Return Desk & Item Inspection
* **Goal:** Build a return portal allowing students or admins to search active checkouts, view countdown timers for due dates, flag returned items as "Good" or "Needs Repair/Maintenance," and calculate overdue penalty warnings.

### Milestone M6: LocalStorage Persistence Engine & Dynamic Demo Reset
* **Goal:** Connect all core modules (Users, Inventory, Loans) to browser `localStorage` with state hydration and a 1-click "Reset Seed Data" button for smooth live presentations.