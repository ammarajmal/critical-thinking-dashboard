# Critical Thinking Evaluation Dashboard

### ⚖️ A Peer-Review & Evaluation Platform

**Status:** V1.0 (Production Ready)

## 📖 Project Overview

The **Critical Thinking Evaluation Dashboard** is a web-based application designed to digitize the academic peer-review workflow. It replaces manual spreadsheet tracking with a real-time, cloud-synced dashboard that enforces structured argumentation and fair evaluation.

The platform guides students to draft arguments using the **PEEL (Point, Evidence, Explanation, Link)** framework and provides a robust, quantitative grading system for peer assessment.

## 🛠 Tech Stack

* **Frontend:** React.js (v18), Tailwind CSS.
* **Backend:** Firebase Firestore (NoSQL Database), Firebase Authentication.
* **Data Processing:** SheetJS (XLSX) for Excel Import/Export.
* **Architecture:** Single-File Component Architecture (SFCA) for portability.

## ✨ Key Features

### 1. Structured Drafting (PEEL Method)
To ensure academic rigor, the application enforces the **PEEL structure** for all submissions. The interface intelligently switches between "Draft Mode" (for new work) and "Edit Mode" (for revisions).

### 2. "Fair Play" Logic Engine
A core requirement was to solve the issue of unfair grading or "freeloading." The system implements strict logic gates:
* **"Give-to-Get" Policy:** Access to the evaluation tools is locked until the user contributes their own argument.
* **Anti-Self-Vote:** Users are programmatically blocked from evaluating their own profile.
* **Locking Mechanism:** Once a student receives an evaluation, their draft is **LOCKED** immediately. This prevents retrospective editing to "fix" answers based on feedback.

### 3. Quantitative Scoring System
* **Primary Metrics (0-100):** Visual sliders for Point, Evidence, Explanation, and Link.
* **Secondary Metrics (0-10):** Additional ratings for Logic, Clarity, and Fairness.
* **Dynamic Updates:** If an evaluator updates their score, the system intelligently replaces the old record to maintain data accuracy.

### 4. Admin Administration Panel
* **Excel Integration:** Admins can bulk-import students or export grades using standard `.xlsx` files.
* **Template Generator:** Built-in tool to generate the correct Excel format for data entry.
* **Hard Reset:** One-click system wipe for initializing new student batches.

## 🧠 Technical Highlights

| Challenge | Solution |
| :--- | :--- |
| **Workflow Integrity** | Implemented complex state management to physically disable the "Rate" tab until specific database conditions (submission existence) were met. |
| **Data Persistence** | Integrated Firebase listeners to ensure that if Student A grades Student B, Student B sees the result instantly without refreshing. |
| **Portability** | Designed the entire application to run from a single `index.html` file without a build step (Create-React-App/Vite), allowing for easy distribution to non-technical users. |

## 🚀 How to Run

1.  **Clone or Download:** Get the `index.html` file from this repository.
2.  **Open:** Simply double-click `index.html` to open it in Chrome, Edge, or Safari.
3.  **Setup:** On the first run, the app will connect to the configured Firebase instance automatically.

## 📸 Screenshots

*(Placeholder for Dashboard View)*
*(Placeholder for Evaluation Form)*

## 📄 License

Distributed under the MIT License.

---

**Developed by [Your Name Here]**
