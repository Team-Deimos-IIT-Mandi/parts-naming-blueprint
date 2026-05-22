

https://github.com/user-attachments/assets/abf3ce57-84cf-4173-883b-87dcbd7861e0



# 🚀 Team Deimos: Rover Naming Blueprint

**A Telemetry-Driven Dynamic Name Hierarchy Manager for IIT Mandi's Mars Rover Team.**

This tool solves a critical problem in collaborative CAD design: **SolidWorks file name clashing and structural ambiguity**. By generating unique, standardized prefix codes based on a part's exact assembly hierarchy, this tool ensures every file, folder, and part in the Mars Rover is instantly identifiable and conflict-free.

---

### 🟢 Live Dashboard
Access the live naming tool here:  
👉 **[team-deimos-iit-mandi.github.io/parts-naming-blueprint](https://team-deimos-iit-mandi.github.io/parts-naming-blueprint/)**

---

## ✨ Key Features

* **Real-Time Cloud Sync:** Powered by Firebase Realtime Database. When one team member updates the blueprint, it instantly updates for everyone else viewing the page.
* **Smart Code Generation:** Automatically generates 2-4 character acronyms based on part names and builds a complete, dash-separated prefix (e.g., `MR-ARM-L1-BPLT`).
* **SolidWorks Ready:** Gives you the exact prefix to prepend to your `.SLDPRT` and `.SLDASM` files before merging them into the master assembly.
* **JSON Export & Import:** Download the entire structural layout as a backup file, or restore the database instantly if needed.
* **Admin Gatekeeper:** Read-only access for general viewers to prevent accidental deletions, with a password-protected edit mode for subsystem leads.
* **Aerospace UI:** A custom, dark-mode dashboard with telemetry-style visuals, color-coded hierarchy levels, and full keyboard shortcut support.

## 🛠️ How to Use

### For General Team Members (Read-Only)
1. Open the **[Live Link](https://team-deimos-iit-mandi.github.io/parts-naming-blueprint/)**.
2. Click through the tree on the left to find your specific subassembly or part.
3. Look at the **Generated Unique Identifier** on the right.
4. Click **Copy Prefix Code** and paste it at the start of your SolidWorks filename (e.g., `MR-WMH-WHL_OuterRim.SLDPRT`).

### For Admins & Subsystem Leads (Editing)
To add new branches, configure acronyms, or delete outdated parts:
1. Enter the admin password in the top right corner.
2. Select any node in the tree.
3. Use the **+ Add Sub-Element Node** or **✎ Configure Node Settings** buttons.
4. The database will automatically save and sync your changes to the cloud.

## 📂 Hierarchy Legend

| Level | Designation | Color Indicator | Example |
| :--- | :--- | :--- | :--- |
| **0** | Core System | Cyan | Mars Rover (`MR`) |
| **1** | Primary Subassembly | Orange | Robotic Arm (`ARM`) |
| **2** | Sub-Subassembly | Green | Link 1 (`L1`) |
| **3+** | Terminal Component | Purple | Base Plate (`BPLT`) |

## 💻 Tech Stack
* **Frontend:** Vanilla HTML5, CSS3, JavaScript (ES6 Modules)
* **Backend:** Firebase Realtime Database (BaaS)
* **Hosting:** GitHub Pages

---
*Built for Team Deimos, IIT Mandi.*
