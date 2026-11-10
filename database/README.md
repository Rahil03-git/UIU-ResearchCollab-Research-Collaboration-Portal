# Database

Database name: **`uiu_researchcollab`** (MariaDB 10.4 / MySQL, `utf8mb4`, InnoDB) - **57 tables**.

The database is built from one schema file, six migrations and a seed file. **Import them in exactly this order**
(phpMyAdmin, *Import* tab, one file at a time - or all with the `mysql` command line):

| # | File | Adds |
|---|---|---|
| 1 | `schema.sql` | Base schema (35 tables) |
| 2 | `migrations.sql` | Repository, saved resources |
| 3 | `migrations_002_landing.sql` | Password-reset tokens, contact messages |
| 4 | `migrations_003_profile_extended.sql` | Extended student profile |
| 5 | `migrations_004_communities.sql` | Extra columns for communities |
| 6 | `migrations_005_faculty_portal.sql` | Faculty portal tables, advisor workflow, connections and chat (14 tables) |
| 7 | `migrations_006_admin_portal.sql` | Faculty verifications, platform settings and moderation flags |
| 8 | `seed.sql` | Demo data (15 users, domains, skills, opportunities, teams ...) - **run once on a fresh database** |

## Steps (XAMPP + phpMyAdmin)

1. Start **Apache** and **MySQL** in XAMPP and open <http://localhost/phpmyadmin>.
2. Click **New**, create the database `uiu_researchcollab` with collation `utf8mb4_unicode_ci`.
3. Select it and import the 8 files above, in order.

> The seed users are **demo accounts for local development only**. Never use them on a public server.
