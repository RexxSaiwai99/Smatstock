# Product Requirements Document (PRD)

## Project Context & Overview
* **What:** The **RAI Inventory & Borrowing Management Portal** is a single-page web application designed for robotics and AI department labs.
* **Why:** To eliminate manual Google Sheet updates, track high-demand equipment, provide role-based access for students and admins, and streamline tool check-outs/returns.
* **Who:**
  * **Students (Users):** Mechatronics, Robotics, and AI students across Batches 67, 68, 69, etc.
  * **Admin (Lab Staff):** Lab managers needing full control over stock, active loans, and system analytics.

---

## Key Features & Requirements

### 1. Authentication & Role-Based Access Control (RBAC)
* **Student Sign-Up:** Collects Full Name, Student ID, Line ID, Batch Number (67, 68, 69+), and Major (Mechatronics, Robotics, AI).
* **Student/Admin Login:** Unified login view with role toggling (Student view vs Admin view).
* **Admin Access:** Admins have full access to manage stock, execute force returns, view all student contact info, and export reports.

### 2. Advanced Analytics Dashboard (10+ Insights & Features)
1. **KPI Summary Cards:** Total Stock, Active Checkouts, Low Stock Alerts, Overdue Returns count.
2. **Top 10 Most Borrowed Items:** Visual leaderboard / horizontal progress chart.
3. **Category Breakdown:** Stock & borrow distribution across Measurement, Microcontrollers, Robotics Arms, Sensors, Tools, etc.
4. **Batch & Major Utilization:** Distribution of active loans by Student Major and Batch (67, 68, 69).
5. **Inventory Health Ratio:** Real-time stock availability percentage indicator.
6. **Low Stock Alert Center:** Quick list of items with $\le 2$ items remaining.
7. **Overdue Risk Monitor:** Live list of students with overdue equipment and quick Line ID notification tags.
8. **Peak Borrowing Hours / Activity Feed:** Log of recent check-out and return activities.
9. **Equipment Condition & Location Tracker:** Quick lookup for shelf/cabinet locations and physical condition.
10. **Interactive Filter & Search Engine:** Live filtering by name, ID, category, location, and stock status.

### 3. Dedicated Borrow & Return System Page
* **Tab / Navigation Switcher:** Seamless navigation between Dashboard, Inventory Catalog, Borrow/Return Desk, and Student Profile.
* **Borrow Interface:**
  * Quick-scan or dropdown selection for Equipment ID.
  * Auto-filled student profile data upon login.
  * Return due-date calculator (default 7 days).
  * One-click "Confirm Checkout" button.
* **Return Interface:**
  * List of active checkouts for logged-in student or full searchable list for Admin.
  * One-click "Return Item" with condition status selection (Good / Needs Repair).
  * Overdue indicator with calculated days overdue.

---

## Out of Scope (Phase 1)
* Hardware RFID/Barcode physical scanner integration (simulated via dropdowns/inputs).
* Backend database servers (all state is stored client-side in `localStorage` & pre-seeded arrays).