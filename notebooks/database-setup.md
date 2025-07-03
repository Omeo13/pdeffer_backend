# PostgreSQL Database Setup for PDEffer

## Objective
Set up a PostgreSQL database locally (or in Docker) for development, and prepare it for deployment (e.g., on Railway).

---

## Steps to Setup PostgreSQL Database

### 1. Install PostgreSQL
- **Option A:** Install PostgreSQL locally on your machine.
- **Option B:** Use a PostgreSQL Docker container for isolation and easy management.

### 2. Create a Docker Container for PostgreSQL (recommended)
- Pull the official PostgreSQL Docker image.
- Run the container with environment variables for:
  - `POSTGRES_USER`
  - `POSTGRES_PASSWORD`
  - `POSTGRES_DB` (your database name)

Example:
```bash
docker run --name pdeffer-postgres -e POSTGRES_USER=pdeffer -e POSTGRES_PASSWORD=yourpassword -e POSTGRES_DB=pdefferdb -p 5432:5432 -d postgres
