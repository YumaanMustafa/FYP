# Stitch3D - Backend Services & API Architecture

This directory contains the core backend services, database connectors, authentication helpers, and API endpoints for the Stitch3D platform.

## Directory Structure

* `api/`: REST API Route Handlers
  * `admin/`: Administrator controls (Users, Vendors, Suppliers, Complaints, Analytics)
  * `vendor/`: Vendor dashboard, Order management, Products, 3D Design Viewers, Material requests
  * `supplier/`: Supplier inventory, Material quote requests, Renegotiation handlers
  * `customer/`: Customer 3D design saves, Custom jacket orders, Ticket complaints
  * `auth/`: Authentication endpoints (JWT login, signup, email verification, profile management)
  * `chat/`: Real-time cross-role messaging endpoints
  * `common/`: Logo & patch upload processing
* `lib/`:
  * `db.js`: MySQL database pool connection using `mysql2/promise`
  * `auth.js`: JWT token verification, password hashing, and role privilege security checks
  * `email.js`: Nodemailer service for order status notifications & admin approvals
  * `initDb.js`: Database table creation and schema initialization script

## Environment Variables Required

Ensure the following environment variables are set:
* `MYSQL_HOST`
* `MYSQL_USER`
* `MYSQL_PASSWORD`
* `MYSQL_DATABASE`
* `JWT_SECRET`
