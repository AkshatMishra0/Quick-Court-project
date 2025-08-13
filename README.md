QuickCourt
A full-stack sports facility booking platform with real-time dashboards, analytics, and robust admin/owner/user flows. Built with Next.js, SQLite, and a modern React component library.

🚀 Features Overview
1. Authentication & User Management
Signup/Login: Secure registration and login for users, owners, and admins.
Password Reset: Email-based password reset with secure token flow.
Profile Management: Update profile, change password, upload avatar, and delete account.
2. Booking System
Venue & Court Booking: Users can browse venues, filter by sport/location/price/rating, and book courts with real-time availability.
Booking Lifecycle: Create, view, and cancel bookings. Bookings are saved in SQLite and localStorage (for backward compatibility).
Booking Status: Upcoming, completed, and cancelled bookings are categorized for both users and owners.
3. Owner Panel
Dashboard: Real-time stats (bookings, earnings, occupancy, etc.), interactive charts (trends, peak hours), and recent bookings.
Bookings Management: Filter bookings by status/date, view customer details, track payments, and paginate large datasets.
Venues & Courts: Manage venues and courts, view analytics, and monitor real-time availability.
4. Admin Panel
Dashboard: Platform-wide stats, user registration trends, sport popularity charts, and recent activity logs.
User Management: View and manage all users, including owners and regular users.
5. API & Database
SQLite Integration: All data (users, venues, courts, bookings, reviews) is stored in a local SQLite database (quickcourt.db).
RESTful API: Endpoints for bookings, users, venues, courts, stats, trends, authentication, and more.
Auto-Initialization: Database and tables are auto-created with sample data on first run.
6. Analytics & Reporting
Charts: Booking trends, peak hours, user registrations, and sport popularity visualized with interactive charts.
Export: Export analytics data for reporting.
7. Testing & Demo
Test Pages: /database-test and /booking-test for API/database integration and booking flow testing.
Demo Users: Pre-seeded owners and users for instant demo.
8. UI/UX
Modern Design: Responsive, accessible, and visually appealing UI.
Reusable Components: Buttons, cards, dialogs, toasts, resizable panels, and more.
Mobile Friendly: Optimized for all devices.
🗂️ Main Pages & Routes
/login — User/admin/owner login
/signup — User registration
/forgot-password — Request password reset
/reset-password — Reset password with token
/profile — User profile management
/venues — Browse and filter venues
/venues/[id]/book — Book a court at a venue
/my-bookings — User's bookings (view/cancel/review)
/owner/dashboard — Owner dashboard (stats, analytics)
/owner/bookings — Owner's booking management
/owner/facilities — Manage venues and courts
/admin/dashboard — Admin dashboard (platform analytics)
/booking-test — Booking API test interface
/database-test — Database integration test
🛠️ Tech Stack
Frontend: Next.js, React, TypeScript, Tailwind CSS
Backend: Next.js API routes, SQLite (better-sqlite3)
Auth: Custom context, JWT/session, secure password hashing
Email: Password reset via email (mocked for demo)
Charts: Custom chart components for analytics
📦 Database Schema
users: id, email, full_name, role, password_hash, is_verified, avatar_url, is_active
venues: id, name, location, owner_id, is_active
courts: id, venue_id, name, sport, is_active
bookings: id, user_id, venue_id, court_id, booking_date, start_time, end_time, duration_hours, total_amount, status, payment_status, created_at, updated_at
reviews: id, user_id, venue_id, rating, comment, created_at
password_reset_tokens: id, user_id, token, expires_at, used
🧪 Testing
Use /booking-test and /database-test to verify API/database functionality.
Demo users and owners are pre-seeded for instant access.
📈 Analytics & Real-Time Data
Real-time stats and analytics for owners and admins.
Charts for trends, peak hours, and user activity.
📋 Scripts
SQL scripts for table creation and seeding (scripts)
Node.js scripts for DB initialization and test data
🏆 Result
Real-time, database-driven booking and management for sports facilities
Full admin, owner, and user flows
Modern, testable, and extensible codebase
