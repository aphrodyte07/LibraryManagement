# Project Statement: Library Management System

## 1. Problem Statement
Traditional library operations often struggle with manual tracking of book inventories, member registrations, and circulation records. Physical logbooks or fragmented spreadsheet records lead to frequent data inaccuracies, misplaced books, unvalidated stock quantities during checkouts, and missed due dates for returned materials. Furthermore, deploying modern library solutions on serverless web platforms (like Vercel) poses data persistence challenges due to ephemeral filesystems, requiring a robust architecture backed by cloud database instances.

## 2. Scope of the Project
The **Library Management System (Bibliotheca)** provides a full-stack, cloud-deployable web application to automate and streamline core library operations. 

### In Scope:
- **Digital Catalog Management**: Full CRUD (Create, Read, Update, Delete) operations for books with real-time stock and copy management.
- **Member Directory**: Patron registration, unique membership code generation, contact tracking, and active loan monitoring per member.
- **Circulation Management**: Borrow and return workflows with real-time stock validation, custom checkout periods, and duplicate loan prevention.
- **Automated Overdue Tracking**: Dynamic status evaluation for overdue books past their designated return due dates.
- **Dashboard & Analytics**: Live stats monitoring total titles, available inventory, active borrowing patrons, and overdue alerts.
- **Cloud & Serverless Deployment**: Full compatibility with Vercel serverless functions (`@vercel/python`) backed by PostgreSQL cloud databases (Supabase, Neon, Railway) and zero-config local SQLite fallback.

### Out of Scope:
- Online monetary fine payment gateway processing (fines tracking can be extended in future iterations).
- RFID / Barcode hardware scanner driver integrations.

## 3. Target Users
- **Head Librarians & Library Administrators**: To manage master catalog inventories, oversee member databases, monitor operational stats, and streamline returns.
- **Library Assistants & Staff**: To handle daily checkout/check-in workflows, answer stock availability queries, and register new patrons.
- **Library Members & Patrons**: To browse available titles, check book availability, and review current loan statuses.

## 4. High-Level Features
- 📊 **Real-time Analytics Dashboard**: Instant visibility into library performance, total inventory, available copies, active loans, and overdue counts.
- 📚 **Smart Book Catalog**: Searchable and filterable catalog by title, author, ISBN, or genre with visual cover image previews.
- 👥 **Patron Management**: Centralized member directory tracking active borrowings and member standing.
- 🔄 **Stock-Aware Borrowing Workflow**: Prevents checkouts when stock is zero or when a member already holds an active loan for the same title.
- 1️⃣ **One-Click Book Returns**: Instant inventory replenishment upon return verification.
- ☁️ **Serverless & Multi-DB Architecture**: Built on FastAPI, SQLAlchemy, and Vercel serverless runtime.
