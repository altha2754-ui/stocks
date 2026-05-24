# AL QWAS AL ZAHABAI — Premium Mobile Showroom ERP (Website Only)

Single **Next.js 15** website with built-in API routes — no separate Express server required.

## Quick Start

### 1. Environment

Copy `.env.example` to `.env` in the project root:

```env
DATABASE_URL=postgresql://...
JWT_ACCESS_SECRET=your-secret-min-32-chars
JWT_REFRESH_SECRET=your-refresh-secret-min-32-chars
```

### 2. Database

```bash
npm run db:push
npm run db:seed
```

### 3. Run website

```bash
npm run dev
```

Open **http://localhost:3000**

| Role  | Email             | Password   |
|-------|-------------------|------------|
| Admin | admin@alqwas.ae   | Admin@123  |
| Staff | staff@alqwas.ae   | Staff@123  |

## Production

Deploy **only** the Next.js app (`apps/web`) to Vercel:

- Set `DATABASE_URL`, `JWT_ACCESS_SECRET`, `JWT_REFRESH_SECRET`
- API lives at `/api/v1/*` on the same domain

## Structure

```
apps/web/           → Full website (UI + API)
packages/shared/    → Shared validators & permissions
prisma/             → Database schema
```

The legacy `apps/api` folder is no longer needed for development.
