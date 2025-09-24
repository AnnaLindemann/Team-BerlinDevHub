This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

##Run the Project with Docker (Development Mode)### 1. Build and start

docker compose up --build

2. Stop containers

docker compose down

3. Show logs

docker compose logs -f

4. Rebuild without cache (e.g. after dependency changes)

docker compose build --no-cache

Hot Reload
The project folder is mounted into the container (./:/app).
When you change files locally, the container instantly sees the updates.
Next.js with Turbopack automatically refreshes the browser.

Check it:

Edit text inside src/app/page.tsx.
Save the file.
Open http://localhost:3000 — the change will appear without restarting the container.

Useful Commands
Remove containers and anonymous volumes:

docker compose down -v

Start in detached mode:

docker compose up -d

Notes

Package manager: pnpm (enabled via Corepack).
Next.js telemetry is disabled (NEXT_TELEMETRY_DISABLED=1).
An anonymous volume is used for /app/node_modules so dependencies are stored inside the container and not overwritten by the host.
