# vercel-cloudinary

Subida de imágenes a Cloudinary con un backend en Express, desplegable en Vercel.

## Estructura

- `api/index.js` — función serverless de Vercel (endpoints `/api/health` y `/api/upload`).
- `server.js` — servidor Express para desarrollo local (`npm run dev`).
- `public/index.html` — frontend.
- `vercel.json` — reglas de rewrite para Vercel.

## Desarrollo local

```bash
npm install
npm run dev
```

Crea un archivo `.env.local` (no se sube al repo) con tus credenciales de Cloudinary:

```
CLOUDINARY_CLOUD_NAME=tu_cloud_name
CLOUDINARY_API_KEY=tu_api_key
CLOUDINARY_API_SECRET=tu_api_secret
```

## Despliegue en Vercel

Importa el repo en Vercel y configura estas variables de entorno en el dashboard
(Project Settings → Environment Variables):

- `CLOUDINARY_CLOUD_NAME`
- `CLOUDINARY_API_KEY`
- `CLOUDINARY_API_SECRET`
