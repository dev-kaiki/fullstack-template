# Fullstack Template (Next.js + NestJS + Postgres)

Template profissional para criar **demos fullstack** com padrão de produção.
Ideal para você clicar em **Use this template** e gerar repos separados (authkit, filevault, etc).

## Requisitos (Windows)
- Node.js 20+
- Docker Desktop (WSL2)
- Git
- VS Code

Habilite pnpm:
```powershell
corepack enable
corepack prepare pnpm@latest --activate
```

## Rodar local (primeira vez)
```powershell
pnpm install
docker compose up -d
```

### API (NestJS)
Crie `apps/api/.env`:
```env
PORT=3001
DATABASE_URL=postgresql://app:app@localhost:5432/app?schema=public
```

Depois:
```powershell
pnpm --filter api prisma:generate
pnpm --filter api prisma:migrate
pnpm --filter api dev
```

Swagger:
- http://localhost:3001/docs

### WEB (Next.js)
Crie `apps/web/.env.local`:
```env
NEXT_PUBLIC_API_URL=http://localhost:3001
```

Depois:
```powershell
pnpm --filter web dev
```

Web:
- http://localhost:3000

## Contato (portfólio)
- Email: kaikiiquadros091o@gmail.com
- WhatsApp: https://wa.me/5516991666951
