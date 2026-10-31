# Universal Education V16 — GitHub Source Package

This package consolidates the latest available V16 Frontend Foundation 0.2, the eight V16 Edge Function source folders, shared helpers, and SQL source backups.

## GitHub repository root
Upload the CONTENTS of this folder to the repository root (so `index.html`, `app.js`, `config.js`, and `style.css` are at the root).

## Frontend configuration required
Open `config.js` and replace the two placeholders with the V16 Supabase Project URL and Publishable Key. Never put a service-role key or any secret in frontend files.

## Important release status
This is a consolidated development/source package, NOT a verified production release. The frontend README lists unfinished integration items. In particular, the current frontend calls `submit-practice-attempt`, but that function is not among the eight deployed functions/source folders here. Username/Student ID login is not fully wired to `identifier-login`. Do not enable public GitHub Pages or use real student data until these integrations and role-based tests are completed.

## Edge Function source
The `supabase/functions/` directory contains the eight function source folders and `_shared` helpers. The eight functions reported deployed in Supabase are: practice-save-answer, practice-submit, mock-save-answer, mock-submit, student-admin, staff-admin, identifier-login, bootstrap-admin. Source inclusion is not proof of successful compile or live integration.

## SQL
`supabase/sql/` contains source backups of the database, storage, and security patch SQL. These are included for version control only. Do not run them again against a database that already has these changes.
