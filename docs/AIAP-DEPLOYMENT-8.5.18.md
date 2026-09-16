# AIAP Platform v8.5.18 — Deployment Notes

This repository branch is prepared for online testing. The AIAP application is a Vite/React client + Express/Prisma server and requires PostgreSQL at runtime.

## Local validation
- Frontend: `npm run dev` / Vite on port 5173
- Backend: Express on port 5000
- Database: PostgreSQL + Prisma migrations

## Online deployment architecture
- Frontend: Vercel or Netlify
- Backend: Render, Railway, or similar Node service
- PostgreSQL: managed PostgreSQL provider
- File/media storage: object storage or managed media service

## Required production environment variables
- `DATABASE_URL`
- `JWT_SECRET`
- `CORS_ORIGIN`
- upload/media storage variables as required by the selected provider

## Security
Do not commit `.env`, database credentials, JWT secrets, seed passwords, uploaded media, or local PostgreSQL data to GitHub.

The development database currently used locally must not be exposed directly to the public internet.
