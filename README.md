# DOZEN

Base + Farcaster mini app scaffold (technical base from the numbered projects stack).

## Stack

- Next.js 16 (App Router) + React 19 + Tailwind CSS v
- wagmi + viem on Base
- Farcaster mini app SDK
- Foundry (contracts scaffold)

## Setup

```bash
npm install
git submodule update --init --recursive
cp .env.example .env.local
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Configure

1. `src/config/app.ts` — name, slug, Base App ID, builder code, production URL
2. `src/config/manifest.ts` — Farcaster domain verification
3. `public/icon.svg` (1:1) + `public/app-thumbnail.svg` (1.91:1) — then `npm run brand`
4. `src/app/globals.css` — retheme colors
5. `src/config/contract.ts` and `src/config/badgeContract.ts` — after deploy

## Contracts

```bash
npm run compile
npm run test:contracts
npm run deploy:sepolia
npm run deploy:base
```

## Deploy

- Frontend: Vercel (or any host)
- Set `NEXT_PUBLIC_SITE_URL` in production env
- Register Base mini app + Farcaster manifest after first deploy
