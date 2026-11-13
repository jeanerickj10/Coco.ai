# COCO.AI — Personal AI Creative Studio

> Your creative world, powered by AI. Generate images and videos from one personal workspace.

COCO.AI is currently a personal project. There are no public accounts, subscriptions, credit plans, or commercial services at this stage.

## Current capabilities

- One composer for image and video generation.
- A catalog of 38 models (8 image and 30 video).
- Model-specific settings for aspect ratio, resolution, duration, audio, batch size and more.
- Reference images, start/end frames, video and audio inputs where supported by a model.
- Uploads and an asset picker.
- Generation status polling and a personal gallery.
- Favorites, downloads, history, reuse and batch actions.
- Local browser history stored in IndexedDB.
- Generation API credentials stored server-side in an httpOnly cookie.

## Tech stack

- Next.js 16 App Router
- React 19
- TypeScript
- Zustand
- pnpm
- Vercel Blob for uploads

## Run locally

```bash
pnpm install
pnpm dev
```

Open http://localhost:3000, choose **Add key**, and enter your generation platform credential in the expected `id:secret` format.

## Environment

```bash
HF_API_BASE_URL=                 # generation API origin, server only
OPEN_HIGGSFIELD_READ_WRITE_TOKEN= # Vercel Blob read-write token
NEXT_PUBLIC_SITE_URL=            # optional canonical site URL
```

Never commit API credentials or secrets.

## Project layout

```
src/
  app/             Next.js routes and global styles
  generation/      API actions, model catalog, polling and state
  openhiggsfield/  Studio UI, composer, model picker and gallery
  site.ts          COCO.AI site identity and metadata
```

## Project direction

This branch is the personal COCO.AI development track. The immediate priorities are a clear COCO.AI identity, reliable personal image/video generation, and a stable local deployment. Authentication, subscriptions, billing and public multi-user infrastructure are intentionally out of scope for now.
